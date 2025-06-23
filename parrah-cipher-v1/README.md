def shift_char(c, shift):
    if c.isalpha():
        base = ord('A') if c.isupper() else ord('a')
        return chr((ord(c) - base + shift) % 26 + base)
    return c

swap_table = {
    'A': '@', 'E': '3', 'I': '!', 'O': '0', 'S': '$', 'T': '+',
    'a': '@', 'e': '3', 'i': '!', 'o': '0', 's': '$', 't': '+'
}
reverse_table = {v: k for k, v in swap_table.items()}

def encrypt(raw):
    shifted = ''.join(shift_char(c, 7) for c in raw)
    swapped = ''.join(swap_table.get(c, c) for c in shifted)
    return f"XZ-{swapped}-P7"

def decrypt(code):
    if code.startswith("XZ-") and code.endswith("-P7"):
        core = code[3:-3]
        unswapped = ''.join(reverse_table.get(c, c) for c in core)
        unshifted = ''.join(shift_char(c, -7) for c in unswapped)
        return unshifted
    return "Invalid format."


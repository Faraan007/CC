import keyword

def classify_token(token):
    operators = {'+', '-', '*', '/', '%', '==', '!=', '>', '<', '>=', '<=', '&&', '||', '!', '&', '|', '^', '<<', '>>', '=', '+=', '-=', '*=', '/=', '%='}
    if token in operators:
        return "Operator"
    elif token.isidentifier() and token not in keyword.kwlist:
        return "Identifier"
    return "Neither"

# User input
token = input("Enter a token: ")
print(f"'{token}' is an {classify_token(token)}.")

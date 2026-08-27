# sons.io
def rotate_word(text):
  if text == " ":
    return "Please input the text again."
  else:
    return text[1:] + text[0]

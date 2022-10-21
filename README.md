# Phonemizers
## Basics
### What is a phonemizer?
### DEFAULT Mode
No phonemization is applied. Use this mode if you wish to input lyrics like ou would in Utau.
### Basics of lyric input
Use `+` to extend the previous lyric over multiple notes.
You can use phonetic hints `[l ih v]` to tweak the pronunciation.
In syllable based phonemizers, you can extend a syllable over multiple notes with `+~` or `+*`.

## Japanese
### DEFAULT (Japanese CV)
| Input | Reclist |
| ------------- | ------------- |
| Hiragana or romaji | Any CV reclist |

You can use romaji or hiragana.

### JA CVVC (Japanese CVVC)
| Input | Reclist |
| ------------- | ------------- |
| Hiragana | Any CVVC reclist |

Lyrics should be written in **hiragana**. If your lyrics are written in romaji, you can convert it to hiragana using the Romaji to Hiragana transformer.
roma to hira

The phonemizer will insert VCs and convert vowels to VV. The default VC length is the preutterance of the following CV. `presamp.ini` settings from the voicebank are not supported yet.

### JA VCV (Japanese VCV)
| Input | Reclist |
| ------------- | ------------- |
| Hiragana | Any VCV reclist |

Lyrics should be written in hiragana. If your lyrics are written in romaji, you can convert it to hiragana using the Romaji to Hiragana transformer.
roma to hira

The phonemizer will automatically convert CV to VCV. If a VCV sample isn't available in the voicebank, it will fall back on CV. presamp.ini settings from the voicebank are not supported yet.
ja vcv

## English
### EN ARPA
| Input | Reclist | Additional dictionary |
| ------------- | ------------- | ------------- |
| Arpabet | Any arpasing reclist | Plugins/arpasing.yaml |

#### Auxiliary dictionary files:
You can find an example arpasing.yaml file in Plugins folder. You can add new entries to it.
A copy of arpasing.yaml file can be added to singer folder for a specific singer. You can even distribute an arpasing.yaml file with your voicebank.
The lookup order is plugin dictionary -> singer dictionary -> default dictionary.




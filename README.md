# Phonemizers
## Basics
### What is a phonemizer?
### DEFAULT Mode
No phonemization is applied. Use this mode if you wish to input lyrics like ou would in Utau.
### Basics of lyric input
Use `+` to extend the previous lyric over multiple notes.
You can use phonetic hints `[l ih v]` to tweak the pronunciation.
In syllable based phonemizers, you can extend a syllable over multiple notes with `+~` or `+*`.
Manual input with `?` turns off the phonemization.

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
### EN ARPA (Arpasing)
| Input | Reclist | Additional dictionary |
| ------------- | ------------- | ------------- |
| Arpabet | Any arpasing reclist | Plugins/arpasing.yaml |

#### Auxiliary dictionary files:
You can find an example arpasing.yaml file in Plugins folder. You can add new entries to it.
A copy of arpasing.yaml file can be added to singer folder for a specific singer. You can even distribute an arpasing.yaml file with your voicebank.
The lookup order is plugin dictionary -> singer dictionary -> default dictionary.

### EN Teto (Teto English)

| Input | Reclist | 
| ------------- | ------------- |
| X-SAMPA | [Delta list #3](https://tl.tubs.wtf/2020/11/09/delta-eng) (partially) |

This phonemizer is not complete. Voicebanks that follow Kasane Teto's English voicebank's aliasing should work without issues (including banks recorded with Delta list #3.) Other Delta English lists will need extra phoneme editing to work. A phonemizer that properly supports every Delta list is planned. You can input lyrics the following ways:

### EN VCCV (Cz's VCCV English)
| Input | Reclist | Additional dictionary |
| ------------- | ------------- | ------------- |
| X-SAMPA | [Cz's VCCV](http://utaulanguageresources.weebly.com/czs-vccv.html) | [Plugins/envccv.yaml](https://github.com/mmemim/OU-EN-VCCV-Custom-Dictionary) |

You can input lyrics in plain English love, plain English + phonetic hint love [l u v] or phonetic hint only [l u v].

You can then use + to break words into syllables, and +*or +~ to extend a sound.

### EN to JA (English to Japanese/"Engrish")

| Input | Reclist | 
| ------------- | ------------- |
| Romaji | Japanese CV, CVVC or VCV |

```
Consonants: b by ch d dh f g gy h hy j k ky l ly m my n ny ng p py r ry s sh t th v w y z zh
Vowels: a i u e o ay ey oy ow aw
```
This phonemizer converts English lyrics to phonemes for Japanese voicebanks. It will automatically adapt to CV, VCV, and CVVC voicebanks.
You can input lyrics in plain English love, plain English + phonetic hint love [l u v] or phonetic hint only [l u v].
You can then use + to break words into syllables, and `+*` or `+~` to extend a sound.

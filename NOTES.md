# Development Notes

## Squelch Threshold Behavior

The squelch slider (0-100) controls the signal level threshold for CW tone detection. The threshold value is calculated as `squelchValue / 2000`, mapping to a range of 0.0 to 0.05 RMS.

**Important:** Setting squelch to 0 will cause decoding to fail. With a threshold of 0, ambient microphone noise keeps the decoder permanently in "tone on" state. Since the signal never drops "below threshold," tone endings are never detected and no Morse symbols get decoded.

The default value of 5 provides a small threshold above typical ambient noise while still being sensitive enough for most use cases.

#### How to use EasyEffects for microphone improvement
 - __Launch EasyEffects__

- From:
    - App launcher → EasyEffects
    - or terminal:

```easyeffects```

- The app has two tabs at the top:
    - Output (headphones/speakers)
    - Input (microphone)
- Click Input (this is where mic processing happens).

#### Select your microphone
- Top‑right device dropdown:
    - Choose your actual mic  
    - Not “Monitor”, not virtual devices

- You should see:
    - Live input meter moving when you speak

- If you don’t:
    - Check KDE → Audio → Input Device
    - Confirm PipeWire is active


#### Enable effects (order matters)
- EasyEffects works as a chain — effects are processed top to bottom.

- Click “Add Effect” and enable these:

- Recommended order for voice:
    1. High‑Pass Filter
    2. Noise Reduction
    3. Compressor
    4. Limiter
    5. (Optional) Equalizer

You can toggle effects on/off individually.

#### Starter mic preset (gaming / Discord / streaming)
- This is a safe, clean baseline that works for most mics.

#### High‑Pass Filter (removes rumble)

- Cutoff: 80–100 Hz
- Slope: Default

**Removes desk noise, mic stand vibration, breath thumps**

#### Noise Reduction
- Use RNNoise if available:
    - Threshold: Default
    - Strength: Start low

__Removes keyboard and room noise__
__Too strong = robotic voice__

#### Compressor (the biggest quality boost)
- Suggested starting values:

    - Ratio: 3:1
    - Threshold: ‑18 dB
    - Attack: 10 ms
    - Release: 100 ms
    - Makeup gain: Enable

__Makes your voice consistent and “radio‑like”__

#### Limiter (prevents clipping)

- Ceiling: ‑1 dB
- Lookahead: Enabled

__Prevents Discord clipping when you shout__

#### Optional: Equalizer (clarity)
Only if you want extra polish:

- Slight boost around 2–4 kHz
- Slight cut < 150 Hz

Keep EQ subtle.

#### Using it with Discord (important)
Discord sometimes:

- Applies its own noise suppression
- Fights your processing

__Recommended Discord settings:__

- Input device: Your real mic
- Disable:
    - Noise suppression
    - Echo cancellation
    - Automatic gain control

__Let EasyEffects handle all processing.__

#### Saving & auto‑starting
- Save your preset

- Top‑right → Presets → Save
- Give it a name like:

```Mic – Gaming Clean```

#### Auto‑start EasyEffects

- In KDE:
    - System Settings → Autostart
    - Add EasyEffects

__Effects apply automatically on login.__
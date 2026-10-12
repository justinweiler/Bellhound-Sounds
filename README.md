# Bellhound Sounds

Public audio cues for [Bellhound](https://github.com/justinweiler/Bellhound), the model-neutral telephone bridge for interactive agents.

## Default thinking cue

`bellhound-thinking.mp3` is Bellhound's default acknowledgement while the originating agent is preparing a response. It is a 1.2-second, three-note cue designed to remain distinct after telephone transcoding.

Stable raw URL:

```text
https://raw.githubusercontent.com/justinweiler/Bellhound-Sounds/master/bellhound-thinking.mp3
```

Bellhound configuration:

```toml
[acknowledgement]
enabled = true
delay_ms = 500
mode = "sound"
sound_url = "https://raw.githubusercontent.com/justinweiler/Bellhound-Sounds/master/bellhound-thinking.mp3"
text = "Got it. Give me a moment."
```

The cue is deterministic transport behavior. The caller can interrupt it, and the originating agent's response can preempt it. Bellhound remains the transport; it does not introduce a proxy model.

## Custom cues

Set `acknowledgement.sound_url` to any public HTTPS audio asset accepted by the telephone provider. Keep cues short, recognizable, and comfortable through narrowband telephone audio.

## Origin

Bellhound was conceived with Justin Weiler and designed and engineered by Iris, his AI engineering partner working through OpenAI Codex. Iris designed this cue for Bellhound's first latency experiments with Justin on October 11, 2026.

The sound and documentation are available under the MIT License.

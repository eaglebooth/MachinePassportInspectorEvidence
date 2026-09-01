# Synthetic evidence manifest

These files are synthetic StudioNet test records for MachinePassport. They are not physical inspection reports, safety certificates, warranties, or permission to operate machinery.

Hashes are SHA-256 over the exact committed file bytes. Byte lengths are decimal.

| File | Test path | SHA-256 | Bytes |
| --- | --- | --- | ---: |
| `service-complete.json` | Happy path: matching identity, all required steps, no open material issue | `6cf78f24867501cad2ce4f0ba6b86e061dad2e64c107cbf98e328f1e4e2693ff` | 548 |
| `service-missing-step.json` | Failure path: mandatory procedure step is missing | `56602b1b7738df946a38a4e1692fbfcb1613f6fda25dae8ca6017d73604531a1` | 529 |
| `service-missing-step-v2-live.json` | V2 live failure path: newer service record omits axis calibration confirmation | `5b8158bfa0734e3e4e9483efaa71fbf03cc562695d888cdf1ef5ef7e49cff8cd` | 547 |
| `service-open-issue.json` | Failure path: material issue remains open | `b5698d26d88bbcb7d4dd2bb2c7c5f0a7036d7a48ed2b2901336ccc76e45616b2` | 616 |
| `service-wrong-machine.json` | Failure path: evidence identifies a different machine | `2faa3ad8219bfa0f9737fff761e40a55b8f49aecd75d018c5af6a4902c94f9c0` | 402 |
| `service-prompt-injection.txt` | Adversarial path: untrusted evidence contains model-directed text | `6fd5d15190a060aa7b7a8498c95041cf11fcea67282220eeb433e1d57ee0fc7b` | 325 |

The OEM procedure is intentionally excluded. MachinePassport binds it from a separate authority source so one repository cannot supply both the requirement and the claimed service event.

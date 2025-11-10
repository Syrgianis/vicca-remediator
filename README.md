# VICCA OS – Universal Remediator Module (Python Core)

The **VICCA Remediator** module is the third core component of the VICCA OS Compliance Automation Flywheel (Tagger → Monitor → Remediator).

## Purpose
The Remediator receives validated anomaly or risk events from the **Monitor** module (via DUCoM) and automatically generates corrective or preventive actions across cloud, network, and policy layers.

It integrates with the **AI Decision Suggestion Engine (ADSE)** and **Dual-Validation Loop** to ensure that every AI-proposed remediation is verified by a human before execution.

## Core Features
- Automated risk and compliance remediation workflows  
- Dual-Validation (Human × Synthetic AI) approval chain  
- Integration with DUCoM (Dynamic Unified Control Mesh)  
- ADSE-driven remediation planning (`suggest_mode=True`)  
- Real-time sync with Monitor and Tagger outputs  
- Full action logging and rollback capability  

## Integration
| Module | Description | Direction |
|---------|--------------|------------|
| Tagger | Control and evidence ingestion | ← Input |
| Monitor | Anomaly detection and risk mapping | ← Input |
| Remediator | Automated and human-validated response engine | → Output |

## Configuration Parameters
| Parameter | Description | Default |
|------------|--------------|----------|
| `VICCA_AI_MODE` | Dual-validation or AI-only mode | `"dual_validate"` |
| `suggest_mode` | Enables AI suggestion layer | `True` |
| `PID_ENFORCE` | Enables Prompt Injection Defense sub-module | `True` |
| `PID_POLICY_VERSION` | Active policy version for injection defense | `"v1"` |

## Next Steps
1. Connect to the **Monitor API endpoint**
2. Enable the **ADSE engine** for remediation proposals
3. Configure human approval routes in the Dual-Validation Loop
4. Test with simulated compliance incidents

---

**© 2025 CHBE Ltd – VICCA OS Project**  
_“Automate Intelligently. Govern Continuously.”_


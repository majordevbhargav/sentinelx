# SentinelX

A research-oriented network anomaly detection sandbox for comparing **traffic-only, context-aware, and risk-informed** detection approaches on a simulated enterprise network.

## The Question

Can network anomaly detection become more useful when traffic behaviour is combined with context such as device identity, VLAN, role, destination familiarity, and asset criticality?

SentinelX is built to explore that question.

## Detection Engines

| Approach | Signals | Main purpose |
|---|---|---|
| Traffic-Only | Network traffic features | Detect statistical anomalies |
| Context-Aware | Traffic + network context | Detect policy and behavioural anomalies |
| Risk-Informed | Traffic + context + criticality | Prioritize operational response |

## Features

- Simulated enterprise network topology
- Multiple VLANs and device roles
- Shared flows for model comparison
- DoS and port-scan scenarios
- Rogue-IoT and exfiltration scenarios
- Flow inspection and explanations
- Precision, recall, F1 and false-positive metrics
- Research Mode for comparative experiments

## Technology

- Python
- Flask
- scikit-learn
- HTML / CSS / JavaScript
- Chart.js

## Run Locally

```bash
git clone https://github.com/majordevbhargav/sentinelx.git
cd sentinelx
pip install -r requirements.txt
python3 app.py
```

Open `http://127.0.0.1:5000`.

## Research Note

The traffic and attack data are simulated. The metrics are useful for comparing behaviour inside the simulator but should not be interpreted as evidence of real-world detection accuracy.

## Learning Path

SentinelX helped me move from:

**Network concepts → Python → machine learning → security context → measurable detection experiments**

It also became the conceptual foundation for later projects such as FlowWatch and Cisco-XDR.

## Future Direction

- Real NetFlow / IPFIX ingestion
- Persistent telemetry
- More realistic network baselines
- Explainable scoring reports
- Integration with FlowWatch
- Controlled response workflows

## Author

**Dev Bhargav**

[GitHub](https://github.com/majordevbhargav) · [LinkedIn](https://www.linkedin.com/in/devbhargav100)

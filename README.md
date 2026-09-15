# SentinelX

A research sandbox for comparing three network anomaly-detection approaches on a simulated corporate network: traffic-only, context-aware, and risk-informed detection.

## Why SentinelX Exists

The project tests a practical hypothesis: raw traffic statistics are useful for obvious volumetric attacks, but identity, VLAN segmentation, destination familiarity, behavioral history, and asset criticality can expose threats that look normal at the packet level.

## Features

- Live simulated network topology
- Multiple VLANs and device roles
- Three detection engines running against the same flow
- DoS, port-scan, privilege-abuse, rogue-IoT, and exfiltration scenarios
- Flow inspector with feature and policy explanations
- Precision, recall, F1, false-positive, and workload metrics
- Research Mode for comparing engines over time

## Detection Engines

| Engine | Main signal | Strength |
|---|---|---|
| Traffic-Only | Isolation Forest on traffic features | Volumetric anomalies |
| Context-Aware | Traffic + device/network context | Policy and behavioral anomalies |
| Risk-Informed | Traffic + context + criticality | Operational prioritization |

## Technology

- Python 3.10+
- Flask
- scikit-learn
- HTML/CSS/JavaScript
- Chart.js for dashboard visualizations

## Getting Started

```bash
git clone https://github.com/majordevbhargav/sentinelx.git
cd sentinelx
pip install -r requirements.txt
python3 app.py
```

Open `http://127.0.0.1:5000`.

## Project Structure

```text
app.py
requirements.txt
static/
├── index.html
├── styles.css
└── app.js
```

## API

| Endpoint | Method | Purpose |
|---|---|---|
| `/api/status` | GET | Current simulation state |
| `/api/config` | POST | Update simulation settings |
| `/api/flows` | GET | Recent scored flows |
| `/api/devices` | GET | Simulated devices and risk |
| `/api/metrics` | GET | Detection performance metrics |

## Research Notes

The dataset is simulated and the models are prototypes. Performance metrics demonstrate comparative behavior within the simulator and should not be treated as evidence of real-world detection accuracy.

## Future Direction

- Real NetFlow/IPFIX ingestion
- Persistent telemetry
- More attack and policy scenarios
- Explainable scoring reports
- Integration with FlowWatch
- Controlled response workflows

## License

MIT

## Author

**Dev Bhargav**

- GitHub: https://github.com/majordevbhargav
- LinkedIn: https://www.linkedin.com/in/devbhargav100

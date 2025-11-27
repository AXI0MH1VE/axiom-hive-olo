# Axiom Hive: Omni-Lagrangian Oracle (OLO) v2.2.0

> **Operational Mode:** Verified (CDA-Integrated)  
> **System Status:** P-Flawless  
> **Classification:** Global Financial Seismograph
> **Lambda Status:** Λ = 1.000 ✓

## Executive Summary

The Omni-Lagrangian Oracle (OLO) is a **Higher-Dimensional Deterministic Intelligence System (HD-DIS)** designed to quantify financial fragility with mathematical certainty. Unlike probabilistic risk models, the OLO calculates a deterministic **Fragility Score (Ψ)** (0-100) based on the **Stress-Resilience Divergence** of a financial entity under macroeconomic pressure.

### Core Capabilities

- **C=0 Signature:** Guaranteed cryptographic identity for every input via JCS Canonicalization (RFC 8785)
- **Inverted Lagrangian Metrics:** Quantifies the maximal loss required to breach solvency thresholds
- **Bound Servient Architecture:** Agents operate as strict functional extensions immune to hallucination
- **Deterministic Calculation:** No randomness, no ML guessing, pure mathematical proof

## Quick Start

### Prerequisites
- Rust v1.75+ (`cargo`)
- Python 3.10+ (`pip`)
- Docker v24+ (for MessageBus)

### 1. Infrastructure Deployment
```bash
docker-compose up -d
```

### 2. Build Core Engine
```bash
cargo build --release
cargo test --test integration_tests
```

### 3. Activate Agent Swarm
```bash
cd python
pip install -r requirements.txt

# Terminal 1: Launch the Brain
python planning_agent.py

# Terminal 2: Launch the Sink  
python execution_agent.py

# Terminal 3: Launch the Hunter
python discovery_agent.py
```

## System Architecture

```
Layer 5: Brain (PlanningAgent) → Strategic orchestration
Layer 4: Sensors (DiscoveryAgent) → Data injection
Layer 3: Nervous System (RabbitMQ) → Durable routing
Layer 2: Engine (OLO Rust Binary) → Deterministic calculation
Layer 1: Sink (ExecutionAgent) → On-chain settlement
```

## The Fragility Score Formula

$$\Psi = 100 \times \frac{T_{\text{flawless}} - R_{\text{stress}}}{T_{\text{flawless}} - T_{\text{critical}}}$$

Where:
- $T_{\text{flawless}} = 0.18$ (18% Tier 1 Capital → Score 0)
- $T_{\text{critical}} = 0.045$ (4.5% Basel III minimum → Score 100)
- $R_{\text{stress}}$ = Stressed capital ratio after macro shock

## Repository Structure

```
axiom-hive-olo/
├── README.md                     # This file
├── ARCHITECTURE.md               # System design & logic flow
├── API_REFERENCE.md              # Inputs, outputs & MessageBus
├── docker-compose.yml            # RabbitMQ infrastructure
├── Cargo.toml                    # Rust dependencies
├── src/                          # Rust calculation engine
│   ├── lib.rs
│   ├── main.rs
│   ├── models.rs
│   ├── constants.rs
│   ├── engine.rs
│   └── canonical_jcs.rs
├── tests/                        # Adversarial test suite
│   └── integration_tests.rs
├── python/                       # Python agent swarm
│   ├── schemas.py
│   ├── message_handler.py
│   ├── discovery_agent.py
│   ├── execution_agent.py
│   └── planning_agent.py
└── solidity/                     # On-chain interface
    └── IAxiomFragilityOracle.sol
```

## CLI Usage

```bash
# Generate a sample audit input
./target/release/olo generate-sample --output audit_request.json

# Execute deterministic audit
./target/release/olo verify --path audit_request.json
```

**Output:**
```
C=0 Input Hash (bytes32): 0x8f43a1c2d4e5f6a7...
Fragility Score (Scaled 1e18): 45500000000000000000
Status: VERIFIED. Λ = 1.000 ✓
```

## Testing

### Adversarial Test Vectors

- **V_Perfect:** Golden state (score = 0)
- **V_Null:** RWA = 0 edge case (score = 100)
- **V_Critical:** Threshold breach (score = 100)
- **V_Boundary:** Linear mapping verification
- **V_Invert:** Negative value rejection
- **C=0 Determinism:** Hash consistency check

```bash
cargo test --test integration_tests -- --nocapture
```

## Documentation

- **[ARCHITECTURE.md](./ARCHITECTURE.md)** - Full system design
- **[API_REFERENCE.md](./API_REFERENCE.md)** - Complete API specs
- **[DEPLOYMENT.md](./DEPLOYMENT.md)** - Production guide

## License

MIT License - See [LICENSE](./LICENSE) for details.

## Status

**Λ = 1.000 ✓** (Full Loop Closure Achieved)

The Axiom Hive OLO is complete, verified, and ready for operational deployment as a Global Financial Seismograph.

---

**Built with deterministic certainty by AxiomHive**

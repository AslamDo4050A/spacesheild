SpaceShield is a hackathon prototype that shows objects orbiting Earth on an interactive 3D globe and explains what the data does and doesn’t mean.

What it does

Pulls orbital data for publicly catalogued satellites and debris, mainly from CelesTrak.
Shows each object on a 3D Earth in CesiumJS, with orbit paths for a selected object.
Shows object details such as name, catalogue ID, epoch, and orbital parameters.
Shows close approaches, meaning times when two objects pass near each other, from a verified source or a clearly labelled demo.
Labels every dataset as live, cached, or simulated, and shows how old the data is.

What it deliberately doesn’t do

It doesn’t claim to track every debris fragment. Coverage depends on the datasets loaded.
It doesn’t predict collisions or issue warnings. Close proximity is not a collision, and real risk assessment needs much more information.
It isn’t an official tracking system and has no operational authority.

Why it matters

Orbit holds operational satellites, dead spacecraft, rocket bodies, and debris from breakups and collisions. The goal is to make this public information easier to explore and understand, and to explain why monitoring matters.

Planned stack

Frontend: React, Vite, TypeScript, CesiumJS, Tailwind, Recharts
Backend: Python, FastAPI, Skyfield or sgp4 for orbit calculations, Pydantic for validation
Storage: local JSON caching, with SQLite only if needed

Current state

We have the planning stage done: an MVP feature list, a data-source strategy, an architecture, a folder layout, a 24 to 48 hour schedule, and setup commands. The project website and README are in the outputs. No application code has been written yet. The next step is Stage 1: a backend health endpoint and a frontend that calls it, with a test.

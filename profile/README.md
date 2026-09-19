Open Engineering Narrators

Open Engineering Narrators defines the concepts, conventions, and metadata for narrators within the Open Engineering ecosystem.

A narrator provides a reusable way to turn an Open Engineering artefact into a coherent narrative.

A narrator may narrate an Open Engineering Tour, an Architecture Decision Record, an Open Engineering Story, a model, a diagram, a text, or another narratable artefact.

Narration as an Open Engineering Capability

Open Engineering separates the thing being narrated from the way it is narrated.

                    Narrator
                       │
                       │ narrates
                       ▼
                  Narratable
                       │
          ┌────────────┼────────────┐
          │            │            │
         Tour         ADR         Story
          │            │            │
          ▼            ▼            ▼
       Narrative    Narrative    Narrative

A narrator describes the rules and characteristics of a narration.

A narratable is the source material being narrated.

A narration is the resulting interpretation or presentation of that material.

This separation allows the same artefact to be narrated in different ways, while allowing the same narrator to be applied to different types of artefacts.

Narrators

A narrator can define characteristics such as:

* Persona — who or what is speaking
* Voice — the identity and character of the narration
* Tone — educational, documentary, dramatic, conversational, technical, or other
* Audience — who the narration is intended for
* Structure — how the narrative is composed
* Emphasis — which aspects of the source should receive attention
* Context — information that should be introduced before the source material
* Narration rules — transformations applied while creating the narrative
* Output — spoken narration, screenplay, audiobook, voice-over, presentation, or other narrative form

A narrator therefore acts as a reusable narration definition, rather than being tied to one particular story or medium.

Narratable Artefacts

Narrators can operate across the Open Engineering ecosystem.

Examples include:

Artefact	Possible narration
Open Engineering Tour	Guided tour
Architecture Decision Record	Decision explanation
Open Engineering Story	Storytelling
Open Engineering Model	Model walkthrough
Open Engineering Diagram	Visual explanation
Open Engineering Text	Spoken or presented text
Open Engineering Presentation	Presentation narration
Open Engineering Motion Picture	Voice-over or character narration

The list is intentionally open-ended.

A narrator should not need to know where an artefact originates. It needs to understand the narratable contract presented to it.

From Definition to Implementation

This repository contains the definitions of narrators.

Concrete implementations belong in corresponding implementation repositories.

open-engineering-narrators
        │
        │ definitions
        ▼
open-engineering-narrator
        │
        │ implementation
        ▼
     Narration

The definition repository establishes the vocabulary, metadata, conventions, and contracts.

An implementation can then use those definitions to produce actual narrations using text generation, speech synthesis, video production, presentation systems, or other capabilities.

Narrators as Reusable Components

The same narrator can be applied to different artefacts:

                 ┌──────────────┐
                 │    Narrator  │
                 └───────┬──────┘
                         │
          ┌──────────────┼──────────────┐
          ▼              ▼              ▼
        Tour            ADR           Story
          │              │              │
          ▼              ▼              ▼
      narration      narration      narration

Likewise, one artefact can be narrated by multiple narrators:

                    Open Engineering Tour
                             │
              ┌──────────────┼──────────────┐
              ▼              ▼              ▼
          Technical       Teacher        Storyteller
           Narrator       Narrator         Narrator
              │              │              │
              ▼              ▼              ▼
          narration      narration       narration

This makes narration composable and reusable across the Open Engineering ecosystem.

Repository Structure

The repository is intended to evolve around definitions such as:

definitions/
├── narrators/
├── personas/
├── voices/
├── tones/
└── conventions/

The exact structure may evolve as the Open Engineering Narrator model develops.

Relationship to Other Open Engineering Repositories

Open Engineering Narrators is deliberately independent of the artefacts it narrates.

For example:

Open Engineering Tours
        │
        │ provides
        ▼
      Tour
        │
        │ narrated by
        ▼
Open Engineering Narrators
        │
        │ implemented by
        ▼
Open Engineering Narrator

The same relationship applies to Stories, Architecture Decision Records, Models, Diagrams, Presentations, Texts, and other Open Engineering artefacts.

Design Principle

The central principle is:

Define the narrator separately from the thing being narrated.

This allows Open Engineering to build a growing library of reusable narrators that can operate across different artefacts, audiences, and media.

Open Engineering

Open Engineering is an ecosystem for defining, implementing, composing, and presenting engineering knowledge and systems.

Open Engineering Narrators provides the definitions for the narration layer of that ecosystem.

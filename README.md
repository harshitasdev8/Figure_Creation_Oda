# Figure_Creation_Oda
The data. Every value is nTPM (normalized transcripts per million) — a measure of how much of that gene's mRNA is present in a tissue, downloaded from the Human Protein Atlas (HPA). It's a proxy for how "active" that gene is in each tissue, not a direct protein or antigen measurement.

The three colors, what each means:

Grey bars ("Below threshold") — this tissue's expression is unremarkable; nothing to flag.
Red bars ("Enhanced") — this tissue's expression is at least 4× the average nTPM across all tissues for that gene. This is HPA's own official rule for calling a tissue "enhanced" for a gene — we didn't invent this cutoff, we pulled it from HPA's published methodology and verified it against their live site.
Orange bar (liver) — liver always gets this color regardless of whether it clears the red threshold or not. This is the one tissue your PI actually cares about for safety, so it's colored to stand out from the crowd every time, whether it's high (like FGFR4) or completely unremarkable (like B7H3).

The dashed horizontal line = the actual threshold number (4 × that gene's own average nTPM). It's calculated fresh from each gene's own data — FGFR4's line is at a different height than B7H3's line, because their averages differ. That's intentional: it means the cutoff is always tied to that specific gene's real expression pattern, not an eyeballed guess.

What we've found so far, per target:

FGFR4: liver is the single highest tissue (81.5 nTPM), and clears "Enhanced" alongside lung and kidney. This is a real, known biology — FGFR4 helps regulate bile acid synthesis in the liver. Of your four targets, this is the one where liver is genuinely the most prominent.
B7-H3 (CD276): no tissue clears "Enhanced" anywhere — confirmed this matches HPA's own official call of "Low tissue specificity" for this gene. Liver sits in the middle of the pack (~12 nTPM), unremarkable. Meaningfully different story from FGFR4.
HER2: not pulled yet.
GD2: not a real gene — it's a ganglioside (a lipid), not something with its own mRNA to measure. We're using two enzyme genes required to build it (ST8SIA1, B4GALNT1) as an indirect proxy, shown as paired bars per tissue instead of one bar, since a tissue only plausibly makes GD2 if both genes are active there together.

The four charts aren't the same underlying claim strength — FGFR4/CD276/HER2 are direct gene measurements; GD2 is an indirect, two-step inference. That distinction needs to travel with the figures when you send them, not just live in your head.

# VEC Community Resource Navigator

A searchable, no-dependency index for the public Virtual Embryo Challenge community resources. It organizes links by workflow and task so participants can find a relevant starting point without scanning the full chronological list.

**Snapshot:** 14 October 2026 · **Cataloged:** 73 resources · **License:** MIT

## Use it

Open `index.html` from GitHub Pages, then search by a topic such as `submission`, `spatial`, or `agent`. Filter by workflow or by task/track. Every card links to the author's public resource.

The catalog is also available as `catalog.json`. It can be read directly by scripts and other community tools.

## Scope and attribution

The titles, public URLs, resource kinds, and review states were transcribed from the official [VEC community resources page](https://virtualembryo.ai/challenge/resources) on 14 October 2026. The first snapshot contained 71 existing resources; after filing the navigator and Slurm starter, the catalog was updated to include both, for 73 total. The workflow and task labels are navigation tags added for this index; they are not organiser categories, validation claims, or endorsements. Follow each link to read the author's own description and limitations. “Filed · not yet reviewed” means the official page had not marked that entry reviewed at snapshot time; filing alone is not acceptance.

This is a snapshot, not a replacement for the official live page. New resources, changed links, and updated review states may appear there first.

## Update the index

1. Compare the live community page with `catalog.tsv`.
2. Add or update one tab-separated row with `kind`, `category`, `tasks`, `title`, and `url`.
3. Keep accepted entries first and filed, not-yet-reviewed entries after them; the generator uses that ordering to set the snapshot status.
4. Run `python3 tools/build_catalog.py` to regenerate `catalog.json`.
5. Update the snapshot date and count in `index.html` and this README.

The generator uses only Python's standard library and refuses duplicate URLs or incomplete rows.

## Contributing

Fix an incorrect title or link, suggest a useful category, or add a newly listed public resource by editing `catalog.tsv`. Keep task labels conservative: use `General` when the resource's own scope is not clear.

## License

MIT. Resource creators retain ownership of their linked work; this index republishes only titles, links, and short navigation metadata.

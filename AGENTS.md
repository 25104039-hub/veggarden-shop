<!-- LOVABLE:BEGIN -->
> [!IMPORTANT]
> This project is connected to [Lovable](https://lovable.dev). Avoid rewriting
> published git history — force pushing, or rebasing/amending/squashing commits
> that are already pushed — as it rewrites history on Lovable's side and the
> user will likely lose their project history.
>
> Commits you push to the connected branch sync back to Lovable and show up in
> the editor, so keep the branch in a working state.
<!-- LOVABLE:END -->

## Structure

- Product data lives in `src/data/vegetables.ts` (single source for catalogue, categories, price helpers). Why: cards, search, deal banner and basket all read the same shape, so adding a vegetable is one edit.
- Basket/order state lives in `src/lib/shop.tsx` as a React context backed by localStorage. Why: no backend yet and the state is shared by header, floating bar, basket and profile.
- All iconography is hand-authored inline SVG in `src/components/Icons.tsx`. Why: emoji render as empty boxes on machines without an emoji font, so they are not used in the UI.
- Tamil script requires "Baloo Thambi 2" in the `--font-display`/`--font-body` stacks in `src/styles.css`. Why: Fredoka and Nunito carry no Tamil glyphs and the names show as tofu.

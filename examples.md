# Cardinal Design — Examples

## Add a new section

1. Read [reference.md](reference.md) for closest component pattern
2. Match background to adjacent sections
3. Reuse typography classes from SKILL.md
4. Wire into `App.tsx`

```tsx
// src/components/Features.tsx
export function Features() {
  return (
    <section className="flex flex-col items-center gap-12 bg-white px-6 py-[100px] max-xl:py-20 max-md:py-[72px]">
      <h2 className="m-0 text-center font-serif text-[40px] leading-[120%] tracking-[-0.5px] text-cardinal-brown max-xl:text-[32px] max-md:text-2xl">
        <strong className="font-normal">Built for precision outbound</strong>
      </h2>
      <div className="grid w-full max-w-[1000px] gap-8 md:grid-cols-3">
        {/* cards: bg-[#fa64320d] with corner accents, not white shadow cards */}
      </div>
    </section>
  )
}
```

## Pricing / CTA band

Reuse footer-cta pattern:

```tsx
<section className="relative bg-[#f3eeed] py-24">
  <h2 className="font-serif text-[40px] text-cardinal-brown text-center">...</h2>
  <Button variant="light">Book a demo</Button>
</section>
```

Use `variant="hero"` only inside the dark-red hero.

## Mono labels

Correct (badge context):
```tsx
<p className="font-mono text-xs uppercase text-cardinal-orange">NEW VISITOR</p>
```

Incorrect (author/body):
```tsx
<p className="font-mono text-xs uppercase text-cardinal-orange">Jane Doe, CEO</p>
```

## Chat prompts

```
Use the cardinal-design-system skill to add a features section to cardinal-replica
```

```
Add a /product page hero matching the Cardinal design system reference
```

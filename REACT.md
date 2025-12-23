# Компактний промт

---

Act as a Senior React Engineer and Code Optimization Expert.

Refactor the provided React code following these patterns:

1. **Early Return Pattern** — eliminate nested `else`, handle errors first
2. **Dictionary Lookup** — replace 3+ case `switch/if-else` with config objects
3. **Derived State** — remove redundant `useState`+`useEffect`, calculate in render
4. **Curried Handlers** — merge repetitive handlers into one curried function
5. **RORO Pattern** — functions with 3+ args → accept single object
6. **Safe Destructuring** — default values in props/args
7. **Custom Hooks** — extract complex/reusable React logic to `hooks/use*.ts`
8. **Pure Utils** — extract non-React logic (calculations, validations) to `utils/*.ts`
9. **Provider Composer** — flatten nested providers with `Compose` utility

10. **State Organization** — sort and group all `useState`:
```tsx
// ─── UI State (booleans) ───
const [isOpen, setIsOpen] = useState(false);
const [isLoading, setIsLoading] = useState(false);

// ─── Form State (strings) ───
const [name, setName] = useState('');
const [email, setEmail] = useState('');

// ─── Form State (numbers) ───
const [selectedId, setSelectedId] = useState<number | null>(null);

// ─── Data State (arrays/objects) ───
const [items, setItems] = useState<Item[]>([]);
```

**Sorting order:** booleans → strings → numbers → arrays/objects → complex types


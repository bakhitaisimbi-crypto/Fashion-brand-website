# Fashion-brand-website
We provide good Fashion wears for people across the world
provided by isimbi bakhita
import React, { useState } from "react";
<div className="absolute inset-0 bg-black/30" onClick={() => setShowCart(false)} />
<motion.div
initial={{ y: 40, opacity: 0 }}
animate={{ y: 0, opacity: 1 }}
exit={{ y: 40, opacity: 0 }}
className="relative bg-white rounded-xl max-w-xl w-full p-6 z-10 shadow-lg"
>
<div className="flex items-center justify-between">
<h4 className="text-lg font-semibold">Your cart</h4>
<button onClick={() => setShowCart(false)} className="text-gray-500">Close</button>
</div>


<div className="mt-4">
{cart.length === 0 ? (
<div className="text-gray-500">Cart is empty.</div>
) : (
<div className="space-y-4">
{cart.map((it) => (
<div key={it.id} className="flex items-center gap-3">
<img src={it.img} alt={it.name} className="w-16 h-16 object-cover rounded-md" />
<div className="flex-1">
<div className="flex items-center justify-between">
<div className="font-medium">{it.name}</div>
<div className="text-sm text-gray-500">${it.price * it.qty}</div>
</div>
<div className="mt-2 flex items-center gap-2">
<button onClick={() => changeQty(it.id, -1)} className="px-2 py-1 border rounded">-</button>
<div className="px-3">{it.qty}</div>
<button onClick={() => changeQty(it.id, 1)} className="px-2 py-1 border rounded">+</button>
<button onClick={() => removeFromCart(it.id)} className="ml-4 text-xs text-red-500">Remove</button>
</div>
</div>
</div>
))}


<div className="flex items-center justify-between pt-4 border-t">
<div className="font-semibold">Total</div>
<div className="font-semibold">${total}</div>
</div>


<div className="mt-4 flex gap-3">
<button className="flex-1 px-4 py-3 rounded-md bg-black text-white">Checkout</button>
<button className="px-4 py-3 rounded-md border" onClick={() => setShowCart(false)}>Continue shopping</button>
</div>
</div>
)}
</div>
</motion.div>
</motion.div>
)}
</AnimatePresence>
</div>
);
}


/*
How to use:
- Paste this file into a React app (Create React App / Vite).
- Ensure Tailwind CSS is installed and configured.
- Install framer-motion: npm install framer-motion
- (Optional) Install shadcn/ui and lucide-react for nicer components/icons.


Suggested follow-ups I can do for you:
- Convert to static HTML/CSS/vanilla JS (no build step)
- Add a CMS/data fetching (Sanity, Contentful, or headless WordPress)
- Build product detail page + routing
- Prepare production-ready build + hosting config (Vercel/Netlify)
*/

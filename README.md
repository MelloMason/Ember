import { Button } from "@/components/ui/button";
import { Card, CardContent } from "@/components/ui/card";
import { Flame } from "lucide-react";
import { motion } from "framer-motion";

export default function EmberLandingPage() {
  return (
    <main className="min-h-screen bg-black text-white px-6 py-10">
      <section className="max-w-4xl mx-auto text-center space-y-6">
        <motion.div initial={{ opacity: 0, y: -20 }} animate={{ opacity: 1, y: 0 }}>
          <h1 className="text-4xl md:text-5xl font-bold">Ignite the Future with <span className="text-pink-500">Ember (EMB)</span></h1>
          <p className="text-lg md:text-xl mt-4 text-gray-300">
            A deflationary cryptocurrency rewarding true engagement. No mining. No staking. Just pure proof of activity.
          </p>
        </motion.div>

        <motion.div initial={{ opacity: 0 }} animate={{ opacity: 1 }} transition={{ delay: 0.3 }}>
          <Button className="bg-pink-600 hover:bg-pink-700 rounded-2xl px-6 py-2 text-lg mt-6">
            Join the Movement
          </Button>
        </motion.div>
      </section>

      <section className="max-w-5xl mx-auto mt-20 grid md:grid-cols-3 gap-6">
        {[
          {
            title: "Fixed Supply",
            desc: "33,333,333 EMB forever. No inflation. Ever.",
          },
          {
            title: "Proof of Activity",
            desc: "Earn by using, voting, building—not just holding.",
          },
          {
            title: "0.03% Burn",
            desc: "Every transaction burns EMB, making it scarcer.",
          },
          {
            title: "DAO Governed",
            desc: "Community-controlled treasury & decisions.",
          },
          {
            title: "EmberChain Migration",
            desc: "Start on Ethereum. Grow into our own Layer 1.",
          },
          {
            title: "Ignite Events",
            desc: "Weekly challenges to grow the ecosystem.",
          },
        ].map((item, i) => (
          <Card key={i} className="bg-zinc-900 border-zinc-700 rounded-2xl">
            <CardContent className="p-6">
              <h3 className="text-xl font-semibold text-pink-400 mb-2">{item.title}</h3>
              <p className="text-gray-300">{item.desc}</p>
            </CardContent>
          </Card>
        ))}
      </section>

      <footer className="mt-20 text-center text-sm text-gray-500">
        <Flame className="mx-auto mb-1 text-pink-500" />
        <p>© {new Date().getFullYear()} Ember Protocol. All rights reserved.
        </p>
      </footer>
    </main>
  );
}

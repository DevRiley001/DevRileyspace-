import { useEffect } from "react"; import { motion } from "framer-motion";

export default function HomeHero() { useEffect(() => { window.scrollTo(0, 0); }, []);

return ( <div className="relative w-full overflow-hidden bg-black text-white"> {/* Glitchy Parallax Background */} <div className="absolute inset-0 z-0 bg-fixed bg-center bg-no-repeat bg-cover animate-pulse opacity-80 mix-blend-overlay" style={{ backgroundImage: "url('/mnt/data/file-Ds8BH8GJLncX8d7RCqmvs1')" }} ></div>

{/* Dark Overlay */}
  <div className="absolute inset-0 bg-black/60 z-10"></div>

  {/* Navigation */}
  <nav className="absolute top-0 left-0 w-full p-6 flex justify-between items-center z-20">
    <h1 className="text-xl font-bold tracking-wide uppercase">DevRiley</h1>
    <ul className="flex gap-6 text-sm uppercase">
      <li className="cursor-pointer hover:underline">Home</li>
      <li className="cursor-pointer hover:underline">About</li>
      <li className="cursor-pointer hover:underline">Services</li>
      <li className="cursor-pointer hover:underline">Portfolio</li>
      <li className="cursor-pointer hover:underline">Contact</li>
    </ul>
  </nav>

  {/* Hero Text */}
  <motion.div
    initial={{ opacity: 0, y: 40 }}
    animate={{ opacity: 1, y: 0 }}
    transition={{ duration: 1.2 }}
    className="relative z-20 flex flex-col items-center justify-center text-center h-screen px-4"
  >
    <h2 className="text-3xl md:text-5xl font-bold tracking-tight leading-tight">
      Ethical Hacking Expert
    </h2>
    <p className="mt-4 text-lg max-w-xl">
      Pen-Testing, Web3 Solutions and Dev, Bot Training | DevRileyspace
    </p>
  </motion.div>
</div>

); }


import { motion } from "framer-motion";

export default function ServicesSection() {
  return (
    <section className="relative bg-black text-white py-20 overflow-hidden">
      <div className="absolute inset-0 z-0">
        <motion.img 
          src="/services-glitch.png" // Place your glitchy service image here
          alt="Ethical Hacking Services"
          className="w-full h-full object-cover opacity-20"
          initial={{ scale: 1.1 }}
          animate={{ scale: 1 }}
          transition={{ duration: 4, repeat: Infinity, repeatType: "reverse" }}
        />
      </div>

      <motion.div 
        className="relative z-10 max-w-4xl mx-auto text-center px-6"
        initial={{ opacity: 0, y: 50 }}
        whileInView={{ opacity: 1, y: 0 }}
        transition={{ duration: 1 }}
      >
        <h2 className="text-4xl md:text-5xl font-bold mb-8">
          Ethical Hacking Services
        </h2>
        <ul className="space-y-4 text-lg md:text-xl text-gray-300">
          <li>• Penetration Testing</li>
          <li>• Vulnerability Assessments</li>
          <li>• Social Engineering Testing</li>
          <li>• Network Security Audits</li>
          <li>• Web Application Security</li>
        </ul>
        <motion.button
          className="mt-10 bg-blue-600 hover:bg-blue-700 text-white font-semibold py-3 px-6 rounded-2xl shadow-lg"
          whileHover={{ scale: 1.05 }}
        >
          Book Now
        </motion.button>
      </motion.div>
    </section>
  );
}


import { motion } from "framer-motion";

export default function ServicesSection() {
  return (
    <section className="relative bg-black text-white py-20 overflow-hidden">
      <div className="absolute inset-0 z-0">
        <motion.img 
          src="/services-glitch.png" // Place your glitchy service image here
          alt="Ethical Hacking Services"
          className="w-full h-full object-cover opacity-20"
          initial={{ scale: 1.1 }}
          animate={{ scale: 1 }}
          transition={{ duration: 4, repeat: Infinity, repeatType: "reverse" }}
        />
      </div>

      <motion.div 
        className="relative z-10 max-w-4xl mx-auto text-center px-6"
        initial={{ opacity: 0, y: 50 }}
        whileInView={{ opacity: 1, y: 0 }}
        transition={{ duration: 1 }}
      >
        <h2 className="text-4xl md:text-5xl font-bold mb-8">
          Ethical Hacking Services
        </h2>
        <ul className="space-y-4 text-lg md:text-xl text-gray-300">
          <li>• Penetration Testing</li>
          <li>• Vulnerability Assessments</li>
          <li>• Social Engineering Testing</li>
          <li>• Network Security Audits</li>
          <li>• Web Application Security</li>
        </ul>
        <motion.button
          className="mt-10 bg-blue-600 hover:bg-blue-700 text-white font-semibold py-3 px-6 rounded-2xl shadow-lg"
          whileHover={{ scale: 1.05 }}
        >
          Book Now
        </motion.button>
      </motion.div>
    </section>
  );
}

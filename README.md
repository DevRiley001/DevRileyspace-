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

export default function PortfolioSection() {
  return (
    <section className="relative bg-[#0e0e0e] text-white py-24 px-6 overflow-hidden">
      <div className="max-w-5xl mx-auto relative z-10">
        <motion.h2 
          className="text-4xl md:text-5xl font-bold mb-4 text-cyan-400"
          initial={{ opacity: 0, y: -20 }}
          whileInView={{ opacity: 1, y: 0 }}
          transition={{ duration: 0.6 }}
        >
          Penetration Testing Tales: Adventures in Cyber Security
        </motion.h2>
        <motion.h3 
          className="text-2xl md:text-3xl font-semibold mb-6 text-purple-300"
          initial={{ opacity: 0, y: -20 }}
          whileInView={{ opacity: 1, y: 0 }}
          transition={{ duration: 0.8, delay: 0.2 }}
        >
          Uncovering the Hidden Secrets: A Day in the Life of an Ethical Hacker
        </motion.h3>
        <motion.p 
          className="text-lg md:text-xl text-gray-300 mb-8"
          initial={{ opacity: 0 }}
          whileInView={{ opacity: 1 }}
          transition={{ duration: 1, delay: 0.4 }}
        >
          Join me on my journey as an ethical hacker, uncovering vulnerabilities and protecting critical systems.
        </motion.p>
        <motion.div 
          className="bg-gradient-to-r from-[#1a1a1a] to-[#111] p-6 rounded-2xl shadow-xl border border-gray-700"
          initial={{ opacity: 0, y: 50 }}
          whileInView={{ opacity: 1, y: 0 }}
          transition={{ duration: 1 }}
        >
          <h4 className="text-xl font-semibold text-white mb-2">SecureCorp Case Study</h4>
          <p className="text-gray-400">
            In collaboration with SecureCorp, I conducted a comprehensive penetration testing of their network, 
            identifying multiple vulnerabilities and providing actionable recommendations.
          </p>
        </motion.div>
      </div>
    </section>
  );
}


import { motion } from "framer-motion";

export default function ValuesMissionSection() {
  return (
    <section className="relative bg-black text-white py-24 px-6 overflow-hidden">
      <div className="max-w-4xl mx-auto z-10 relative">
        <motion.h2 
          className="text-4xl md:text-5xl font-bold text-cyan-500 mb-6"
          initial={{ opacity: 0, y: -30 }}
          whileInView={{ opacity: 1, y: 0 }}
          transition={{ duration: 0.7 }}
        >
          Our Values & Mission
        </motion.h2>
        
        <motion.p 
          className="text-lg text-gray-300 mb-6"
          initial={{ opacity: 0 }}
          whileInView={{ opacity: 1 }}
          transition={{ duration: 1, delay: 0.2 }}
        >
          Riley's values and mission are driven by a deep sense of responsibility and a commitment to protecting the digital world. He believes that ethical hacking is not just a job, but a calling to improve the security of individuals and organizations around the world.
        </motion.p>

        <motion.p 
          className="text-lg text-gray-300"
          initial={{ opacity: 0 }}
          whileInView={{ opacity: 1 }}
          transition={{ duration: 1, delay: 0.4 }}
        >
          His mission is to stay at the forefront of cybersecurity and to constantly innovate and adapt his techniques to stay ahead of emerging threats. He is dedicated to helping his clients stay safe and secure, and is always looking for ways to enhance his skills and knowledge to better serve their needs.
        </motion.p>
      </div>

      <div className="absolute inset-0 z-0 opacity-10">
        <img src="/cyber-glitch-bg.png" alt="Glitchy Digital Background" className="w-full h-full object-cover" />
      </div>
    </section>
  );
}


import { motion } from "framer-motion";

export default function ContactSection() {
  return (
    <section className="bg-black text-white py-24 px-6 relative">
      <motion.div 
        className="max-w-3xl mx-auto text-center"
        initial={{ opacity: 0, y: 40 }}
        whileInView={{ opacity: 1, y: 0 }}
        transition={{ duration: 1 }}
      >
        <h2 className="text-4xl md:text-5xl font-bold text-cyan-400 mb-8">
          Get in Touch with Riley
        </h2>

        <form className="space-y-6 text-left">
          <div>
            <label className="block mb-1 text-gray-300">Name</label>
            <input 
              type="text" 
              defaultValue="Riley"
              className="w-full p-3 rounded-md bg-[#1a1a1a] text-white border border-gray-600 focus:outline-none focus:ring-2 focus:ring-cyan-500"
            />
          </div>
          <div>
            <label className="block mb-1 text-gray-300">Email</label>
            <input 
              type="email" 
              defaultValue="autotrackerr@gmail.com"
              className="w-full p-3 rounded-md bg-[#1a1a1a] text-white border border-gray-600 focus:outline-none focus:ring-2 focus:ring-cyan-500"
            />
          </div>
          <div>
            <label className="block mb-1 text-gray-300">WhatsApp Number</label>
            <input 
              type="text" 
              defaultValue="+1 720-233-6886"
              className="w-full p-3 rounded-md bg-[#1a1a1a] text-white border border-gray-600 focus:outline-none focus:ring-2 focus:ring-cyan-500"
            />
          </div>

          <div className="flex flex-col gap-3 mt-6">
            <p className="text-gray-400">TikTok: <a href="https://www.tiktok.com/@rileythedev?_t=ZM-8vl8noGHdo7&_r=1" target="_blank" className="text-cyan-400 hover:underline">rileythedev</a></p>
            <p className="text-gray-400">Discord: <span className="text-cyan-400"></span></p>
          </div>

          <button 
            type="submit"
            className="mt-6 w-full bg-cyan-600 hover:bg-cyan-700 text-white font-semibold py-3 rounded-2xl shadow-lg"
          >
            Submit
          </button>
        </form>
      </motion.div>
    </section>
  );
}

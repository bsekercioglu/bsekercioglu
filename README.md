import React from "react";

// Professional single-file React component for a personal profile page
// Tailwind CSS utility classes are used for styling (assumes Tailwind configured)

export default function ProfilePage() {
  const repos = [
    { name: "VergiNoKontrol", desc: "Turkish Tax Number Checker", lang: "TSQL", link: "https://github.com/bsekercioglu/VergiNoKontrol" },
    { name: "Console_NumLck", desc: "Numeric lock helper for console apps", lang: "C#", link: "https://github.com/bsekercioglu/Console_NumLck" },
    { name: "ConsoleApp", desc: "Test uygulaması / Jupyter Notebook examples", lang: "Jupyter Notebook", link: "https://github.com/bsekercioglu/ConsoleApp" },
    { name: "samsunTSO", desc: "Samsun TSO related project", lang: "Java", link: "https://github.com/bsekercioglu/samsunTSO" },
    { name: "translator", desc: "Translator utilities", lang: "Java", link: "https://github.com/bsekercioglu/translator" },
    { name: "app01", desc: "Kotlin demo app", lang: "Kotlin", link: "https://github.com/bsekercioglu/app01" }
  ];

  return (
    <div className="min-h-screen bg-gray-50 text-gray-900 antialiased">
      <header className="bg-white shadow-sm">
        <div className="container mx-auto px-6 py-6">
          <h1 className="text-3xl font-bold">Burak ŞEKERCİOĞLU</h1>
          <p className="text-sm text-gray-600 mt-1">Fullstack Developer · System Administrator</p>
          <p className="text-xs text-gray-500 mt-1">Samsun · Samsun TSO</p>
          <p className="mt-4 text-sm leading-relaxed text-gray-700 max-w-2xl">
            Experienced Fullstack Developer and System Administrator with a passion for building
            scalable web applications, automation systems, and reliable infrastructures.
            With professional experience dating back to 1985, I have worked with a wide range of
            technologies including C#, Java, Python, and cloud-native solutions. I regularly share
            technical insights on my blog and actively contribute to open-source projects.
          </p>
          <div className="mt-4 flex items-center gap-3">
            <a href="https://github.com/bsekercioglu" className="btn-link" aria-label="GitHub">GitHub</a>
            <a href="https://www.sekercioglu.eu" className="btn-link" aria-label="Website">Website</a>
            <a href="https://twitter.com/bsekercioglu" className="btn-link" aria-label="Twitter">X</a>
            <a href="https://linkedin.com/in/bsekercioglu" className="btn-link" aria-label="LinkedIn">LinkedIn</a>
          </div>
        </div>
      </header>

      <main className="container mx-auto px-6 py-10 grid grid-cols-1 lg:grid-cols-3 gap-8">
        {/* Left column */}
        <section className="lg:col-span-1 bg-white p-6 rounded-2xl shadow-sm">
          <h2 className="text-lg font-medium">Quick Bio</h2>
          <p className="mt-3 text-sm leading-relaxed text-gray-700">
            I have been developing software with love since 1985. Currently working as a Fullstack
            developer and System Administrator. I write technical articles regularly at
            <a href="https://www.sekercioglu.eu" className="ml-1 text-indigo-600 underline"> sekercioglu.eu</a>.
          </p>

          <div className="mt-6">
            <h3 className="text-sm font-medium text-gray-700">Contact</h3>
            <ul className="mt-2 text-sm text-gray-600 space-y-1">
              <li>Email: <a href="mailto:bsekercioglu@gmail.com" className="text-indigo-600">bsekercioglu@gmail.com</a></li>
              <li>Location: Samsun, Turkey</li>
              <li>Company/Org: Samsun TSO</li>
            </ul>
          </div>

          <div className="mt-6">
            <h3 className="text-sm font-medium text-gray-700">Languages & Tools</h3>
            <div className="mt-3 flex flex-wrap gap-2">
              {['C#','Java','Kotlin','Python','Go','SQL','Linux','Docker','Vue','Android'].map((t)=> (
                <span key={t} className="px-3 py-1 text-xs bg-gray-100 rounded-full">{t}</span>
              ))}
            </div>
          </div>

          <div className="mt-6">
            <button className="w-full py-2 px-4 rounded-xl bg-indigo-600 text-white font-medium hover:bg-indigo-700">Download CV</button>
          </div>
        </section>

        {/* Right column */}
        <section className="lg:col-span-2 space-y-6">
          <div className="bg-white p-6 rounded-2xl shadow-sm">
            <h2 className="text-xl font-semibold">Featured Projects</h2>
            <p className="text-sm text-gray-600 mt-1">A selection of repositories from my GitHub profile.</p>

            <div className="mt-4 grid grid-cols-1 md:grid-cols-2 gap-4">
              {repos.map(r => (
                <a key={r.name} href={r.link} className="block p-4 rounded-lg border hover:shadow-md transition">
                  <div className="flex items-start justify-between">
                    <div>
                      <h3 className="font-medium">{r.name}</h3>
                      <p className="text-xs text-gray-600 mt-1">{r.desc}</p>
                    </div>
                    <span className="text-xs text-gray-500">{r.lang}</span>
                  </div>
                </a>
              ))}
            </div>
          </div>

          <div className="bg-white p-6 rounded-2xl shadow-sm">
            <h2 className="text-xl font-semibold">Articles & Writing</h2>
            <p className="text-sm text-gray-600 mt-1">I regularly publish technical articles. Examples and longer posts are available on my blog.</p>
            <div className="mt-4 flex gap-3">
              <a href="https://www.sekercioglu.eu" className="px-4 py-2 rounded-md border">Visit blog</a>
              <a href="https://github.com/bsekercioglu" className="px-4 py-2 rounded-md border">View GitHub</a>
            </div>
          </div>

          <div className="bg-white p-6 rounded-2xl shadow-sm">
            <h2 className="text-xl font-semibold">Availability & Hiring</h2>
            <p className="text-sm text-gray-600 mt-1">Open to freelance or contract opportunities. If you'd like to work together, let's connect.</p>
            <div className="mt-4">
              <a href="mailto:bsekercioglu@gmail.com" className="inline-block px-5 py-2 rounded-lg bg-green-600 text-white">Contact me</a>
            </div>
          </div>
        </section>
      </main>

      <footer className="py-8 text-center text-sm text-gray-500">© {new Date().getFullYear()} Burak ŞEKERCİOĞLU — Built with care</footer>
    </div>
  );
}

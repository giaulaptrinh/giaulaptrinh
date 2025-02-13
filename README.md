import React from 'react';

const ProfilePage = () => {
  const socialLinks = [
    { name: 'facebook', url: 'https://www.facebook.com/giau.lee.9693/' },
    { name: 'gmail', url: 'mailto:levangiau20032020@gmail.com' },
    { name: 'linkedin', url: 'https://www.linkedin.com/in/gi%C3%A0u-l%C3%AA-338235308/' }
  ];

  const skills = {
    languages: [
      'JavaScript',
      'PHP',
      'TypeScript',
      'C++',
      'C#',
      'Python',
      'HTML5',
      'CSS3'
    ],
    frameworks: [
      'Node.js',
      'Express',
      'Laravel',
      'Flask'
    ],
    databases: [
      'MySQL',
      'MongoDB',
      'Microsoft SQL Server'
    ],
    tools: [
      'Docker',
      'Postman',
      'Swagger',
      'AWS',
      'Git',
      'GitHub',
      'Linux'
    ]
  };

  const SkillSection = ({ title, items }) => (
    <section className="mb-8">
      <h2 className="text-xl font-semibold mb-4">{title}:</h2>
      <div className="flex flex-wrap gap-4">
        {items.map(item => (
          <div 
            key={item} 
            className="w-16 h-16 rounded-full bg-gray-100 flex items-center justify-center hover:bg-gray-200 transition-colors cursor-pointer shadow-sm hover:shadow-md"
          >
            <img
              src={`/api/placeholder/48/48`}
              alt={item}
              className="w-10 h-10"
            />
            <span className="sr-only">{item}</span>
          </div>
        ))}
      </div>
    </section>
  );

  return (
    <div className="max-w-4xl mx-auto p-8">
      <header className="mb-8">
        <h1 className="text-3xl font-bold mb-4">Hi, I'm Le Van Giau 👋</h1>
        <p className="text-lg text-gray-700">Aspiring BackEnd Developer</p>
      </header>

      <section className="space-y-4 mb-8">
        <p className="text-gray-800">
          🚀 I'm a 4th year Computer Science student, passionate about Backend Development 
          and continuously learning new technologies.
        </p>
        <p className="text-gray-800">
          🌱 Currently, I'm improving my skills in JavaScript, PHP, AWS, and Web3 
          while looking for an internship opportunity.
        </p>
        <p className="text-gray-800">
          📧 How to reach me: levangiau20032020@gmail.com
        </p>
      </section>

      <section className="mb-8">
        <h2 className="text-xl font-semibold mb-4">Connect with me:</h2>
        <div className="flex gap-4">
          {socialLinks.map(platform => (
            <a
              key={platform.name}
              href={platform.url}
              target="_blank"
              rel="noopener noreferrer"
              className="w-12 h-12 rounded-full bg-gray-100 flex items-center justify-center hover:bg-gray-200 transition-colors shadow-sm hover:shadow-md"
            >
              <img
                src={`/api/placeholder/48/48`}
                alt={platform.name}
                className="w-8 h-8"
              />
              <span className="sr-only">{platform.name}</span>
            </a>
          ))}
        </div>
      </section>

      <SkillSection title="Languages" items={skills.languages} />
      <SkillSection title="Frameworks" items={skills.frameworks} />
      <SkillSection title="Databases" items={skills.databases} />
      <SkillSection title="DevOps & Tools" items={skills.tools} />
    </div>
  );
};

export default ProfilePage;
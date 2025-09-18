```js

from dataclasses import dataclass, field
from typing import List


@dataclass
class Skills:
    languages: List[str] = field(default_factory=lambda: ["Python", "Dart", "C++"])
    front_end: List[str] = field(default_factory=lambda: ["HTML", "CSS", "JavaScript"])
    frameworks: List[str] = field(default_factory=lambda: ["Flutter", "Django"])
    others: List[str] = field(default_factory=lambda: ["JWT Auth", "Git", "GitHub", "CI/CD", "CyberSecurity"])


@dataclass
class Bio(Skills):
    name: str = "Atul Vishwakarma"
    title: str = "Software Engineer"
    location: str = "Ahmedabad"
    linkedin: str = "https://www.linkedin.com/in/atul-0906b71b4/"
    github: str = "https://github.com/vishwakarma62"

    def show(self):
        print(f"👨‍💻 {self.name} — {self.title}")
        print(f"📍 Location: {self.location}")
        print(f"🔗 LinkedIn: {self.linkedin}")
        print(f"🐙 GitHub: {self.github}")
        print("\n💻 Skills:")
        print(f"  🖥 Languages : {', '.join(self.languages)}")
        print(f"  🎨 Frontend  : {', '.join(self.front_end)}")
        print(f"  🏗 Frameworks: {', '.join(self.frameworks)}")
        print(f"  🔧 Others    : {', '.join(self.others)}")


if __name__ == "__main__":
    dev_bio = Bio()
    dev_bio.show()


```

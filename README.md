```python
from datetime import datetime


class ReadMe:
    def __init__(self, username="Tedyst", year=2022):
        self.username = username
        self.name = 'Stoica Tedy'
        self.education = {
            'college': 'Costache Negruzzi National College',
            'programming': ['Self Learning', 'Alexandru Ioan Cuza University'],
        }
        self.employment = {
            'organization': 'Tremend Software Consulting SRL',
            'role': 'Junior Python Developer',
            'since': datetime.strptime('2022-07-04', '%Y-%m-%d')
        }

    def doing(self, now=2022):
        today = self.year

        if now <= today:
            return (
                f"I am attending the Alexandru Ioan Cuza University from Iasi, Romania."
                f"Also, I am working at {self.employment['name']} as a {self.employment['title']}"
            )

        else:
            goal = self.employment['developer']
            return """
            I am eager to collaborate with {teams} on {projects}.
            """.format(teams=goal[0], projects='software development')

    def collaborate(self, role, organization):
        self.employment = {
            'organization': organization,
            'role': role,
            'since': datetime.now()
        }


me = ReadMe(year=2022)
```

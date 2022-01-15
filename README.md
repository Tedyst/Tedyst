```python
class ReadMe:
    def __init__(self, username="Tedyst", year=2022):
        self.username = username
        self.name = 'Stoica Tedy'
        self.education = {
            'college': 'Costache Negruzzi National College',
            'programming': ['Self Learning', 'Alexandru Ioan Cuza University'],
        }
        self.employment = None

    def doing(self, now=2022):
        today = self.year

        if now <= today:
            return """
            I am attending the Alexandru Ioan Cuza University from Iasi, Romania.
            """

        elif now > today:
            goal = self.employment['developer']
            return """
            I am eager to collaborate with {teams} on {projects}.
            """.format(teams=goal[0], projects='software development')

        else:
            return """
            Hello
            """

    def collaborate(self, role, organization, location):
        opportunity = self.employment
        opportunity[role] = [organization, location]

me = ReadMe(year=2022)
```

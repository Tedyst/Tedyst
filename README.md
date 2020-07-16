```python
class ReadMe:
    def __init__(self, username="Tedyst", year=2020):
        self.username = username
        self.name = 'Stoica Tedy'
        self.education = {
            'college': 'In Romania',
            'programming': ['Self Learning'],
        }
        self.employment = None

    def doing(self, now=2020):
        today = self.year

        if now <= today:
            return """
            I am still learning to go to university
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

me = ReadMe(2020)
```

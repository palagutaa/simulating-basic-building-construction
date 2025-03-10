# simulating-basic-building-construction
class Building:
    def __init__(self, name, floors, material):
        self.name = name
        self.floors = floors
        self.material = material
        self.built = False

    def build(self):
        self.built = True
        print(f'{self.name} is built with {self.floors} floors using {self.material}.')

class House(Building):
    def __init__(self, name, floors, material, garden_size):
        super().__init__(name, floors, material)
        self.garden_size = garden_size

    def build(self):
        super().build()
        print(f'It has a garden of {self.garden_size} square meters.')

class Office(Building):
    def __init__(self, name, floors, material, office_count):
        super().__init__(name, floors, material)
        self.office_count = office_count

    def build(self):
        super().build()
        print(f'It contains {self.office_count} offices.')

class Skyscraper(Building):
    def __init__(self, name, floors, material, elevators):
        super().__init__(name, floors, material)
        self.elevators = elevators

    def build(self):
        super().build()
        print(f'It has {self.elevators} elevators.')

class ConstructionManager:
    def __init__(self):
        self.projects = []

    def add_project(self, project):
        self.projects.append(project)
        print(f'Project {project.name} added.')

    def start_construction(self):
        for project in self.projects:
            project.build()

# Example usage
if __name__ == "__main__":
    house = House("Family House", 2, "brick", 50)
    office = Office("Tech Office", 5, "steel", 20)
    skyscraper = Skyscraper("Downtown Skyscraper", 50, "glass", 10)
123

# nature
class Nature:
    def __init__(self, name, description):
        self.name = name
        self.description = description

    def display_info(self):
        return f"{self.name}: {self.description}"

class Tree(Nature):
    def __init__(self, name, description, species):
        super().__init__(name, description)
        self.species = species

    def display_info(self):
        return f"{self.name} ({self.species}): {self.description}"

class River(Nature):
    def __init__(self, name, description, length):
        super().__init__(name, description)
        self.length = length

    def display_info(self):
        return f"{self.name} (Length: {self.length}): {self.description}"

def main():
    # Creating instances of nature elements
    oak_tree = Tree("Oak Tree", "Tall and strong", "Quercus")
    amazon_river = River("Amazon River", "Longest river in South America", "6,575 km")

    # Displaying information
    print(oak_tree.display_info())
    print(amazon_river.display_info())

if __name__ == "__main__":
    main()

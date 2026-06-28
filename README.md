226-6# Oci-Pals-Roof-v2
Fun Serious Joke Map

"""

Personal notes.

Probably overthinking something again.
Probably not.

One signal.
One witness.
One more witness.
Then people start acting like it was obvious the whole time.
"""
"""


class BrainCellMap:
    def __init__(self):
        self.origin = "One person with an idea"
        self.connector = None
        self.second_person = None
        self.signal = 0

    def meet_connector(self, connector_name):
        self.connector = connector_name
        self.signal += 1
        print(f"{self.origin} meets {self.connector}.")
        print("The idea now feels less random.")

    def bring_second_person(self, person_name):
        self.second_person = person_name
        self.signal += 2
        print(f"{self.connector} brings in {self.second_person}.")
        print("Now the idea has outside confirmation.")

    def loop_status(self):
        if self.signal == 0:
            return "Stage 1: Just one person talking."
        elif self.signal == 1:
            return "Stage 2: One trusted connector gives the idea weight."
        else:
            return "Stage 3: The loop starts. More people can believe it faster."


# Example run
map = BrainCellMap()

print(map.loop_status())

map.meet_connector("Trusted Connector")
print(map.loop_status())

map.bring_second_person("Second Person")
print(map.loop_status())

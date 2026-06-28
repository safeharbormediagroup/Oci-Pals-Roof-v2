

notes


A symbolic model

Interpret however you want



class SignalMap:
    def __init__(self):
        self.seed = "Initial Signal"
        self.bridge = None
        self.echo = None
        self.resonance = 0

    def add_bridge(self, bridge_name):
        self.bridge = bridge_name
        self.resonance += 1

        print(f"{self.seed} reaches {self.bridge}.")
        print("The signal starts gaining weight.")

    def add_echo(self, echo_name):
        self.echo = echo_name
        self.resonance += 2

        print(f"{self.bridge} reflects into {self.echo}.")
        print("The signal now carries confirmation.")

    def loop_status(self):
        if self.resonance == 0:
            return "Phase 1: A signal exists."
        elif self.resonance == 1:
            return "Phase 2: The signal has a bridge."
        else:
            return "Phase 3: The signal carries itself."


# Example run
loop = SignalMap()

print(loop.loop_status())

loop.add_bridge("Bridge")
print(loop.loop_status())

loop.add_echo("Echo")
print(loop.loop_status())

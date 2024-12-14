# OE-7

class tekkenCharacter:
    def __init__(self, name, ability):
        self.name = name
        self.ability = ability
        
    def introduce(self, func):
        def introducer(*args, **kwargs):
            print("Introducing...")
            func(*args, **kwargs)
            print("This character is amazing")
            
        return introducer
        
nina = tekkenCharacter("Nina Williams", "Shoulder Through Buster")

@nina.introduce
def character_intro():
    print(f"I am {nina.name} and I can use {nina.ability}")
    
character_intro()

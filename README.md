# names-age-range
Playing around with variables with added ranges and subjects
people = {'Tim': 43, 'Brian': 44, 'Nadia': 39, 'Quitta':36, 'Maurice': 13, 'PJ': 7}
ppl_list = list(people.keys())
for n in range(len(ppl_list)):
    younger = [x[0] for x in people.items() if x[1] < people[ppl_list[n]]]
    y_prnt = ""
    for y in younger:
        if y_prnt == "":
            y_prnt += f"younger than {y}"
        else:
            y_prnt += f" and {y}"
    print(f'{ppl_list[n]} is {people[ppl_list[n]]} years old. They are {y_prnt if len(y_prnt) > 0 else "the oldest"}')

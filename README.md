# ===============================
# PSHS GRADE CALCULATOR
# ===============================

# Convert percentage to point grade
def percent_to_point(p):
    brackets = [
        (96, 1.00), (90, 1.25), (84, 1.50), (78, 1.75),
        (72, 2.00), (66, 2.25), (60, 2.50), (55, 2.75),
        (50, 3.00), (40, 4.00), (0, 5.00)
    ]
    for cutoff, grade in brackets:
        if p >= cutoff:
            return grade

# Adjectival equivalent
def adjectival(grade):
    labels = [
        (1.00, "EXCELLENT"),
        (1.50, "VERY GOOD"),
        (2.00, "GOOD"),
        (2.50, "SATISFACTORY"),
        (3.00, "FAIR"),
        (4.00, "FAILED ON CONDITION"),
        (5.00, "FAILED")
    ]
    for limit, label in labels:
        if grade <= limit:
            return label

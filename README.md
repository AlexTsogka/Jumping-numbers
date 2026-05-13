def is_jumping(number):
    digits = str(number)
    
    # 1. Έλεγχος για μονοψήφιους
    if len(digits) == 1:
        return "JUMPING"
    
    # 2. Ξεκινάμε από το 0 για να πιάσουμε όλα τα ζευγάρια
    for i in range(len(digits) - 1):
        # Μετατρέπουμε σε int για να κάνουμε την αφαίρεση
        diff = int(digits[i]) - int(digits[i+1])
        
        # Αν η απόλυτη διαφορά ΔΕΝ είναι 1, τότε σταματάμε αμέσως
        if abs(diff) != 1:
            return "NOT JUMPING"
            
    # 3. Αν η λούπα τελειώσει χωρίς να βρει λάθος, τότε είναι JUMPING
    return "JUMPING"

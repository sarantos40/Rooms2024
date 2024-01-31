# Τα δωμάτια που διατηρούνται σε διαφορετικές θερμοκρασίες

*Rooms* από τους **Ισορροπιστές**

Έργο πάνω σε Τεχνητή Νοημοσύνη σε περιβαντολογικά ζητήματα

Στον 6ο ΠΑΝΕΛΛΗΝΙΟ ΔΙΑΓΩΝΙΣΜΟ ΑΝΟΙΧΤΩΝ ΤΕΧΝΟΛΟΓΙΩΝ ΣΤΗΝ ΕΚΠΑΙΔΕΥΣΗ

---

Αποθετήριο github:
git@github.com:sarantos40/Rooms2024.git

## Θερμοκρασίες δωματίων

Η εξοικονόμηση ενέργειας, χωρίς θυσία των επιθυμητών συνθηκών, είναι σημαντικό μέτρο για το περιβάλλον.
Σε ένα μεγάλο κτίριο που αποτελείται από πολλούς χώρους (γραφεία, εργαστήρια, ...) συχνά επιθυμούμε διαφορετικές θερμοκρασίες ανά χώρο / δωμάτιο.
Και συχνά υπάρχουν και διαφορετικές αρχικές συνθήκες θερμοκρασίας σε κάθε δωμάτιο (ανάλογα με τη χρήση του, τον αριθμό των ανθρώπων που φιλοξενεί, τα μηχανήματα που περιέχει, κ.λπ).
Επιθυμούμε ένα σύστημα που θα διατηρεί τις θερμοκρασίες όχι ίσες (όπως υποθέτουμε όταν δεν έχουμε άλλα δεδομένα), αλλά σε ισορροπία που απορρέει από τις συνηθισμένες συνθήκες και τις διαφοροποιήσεις των δωματίων.

## Εφαρμογή

Σε ένα κτίριο κάθε δωμάτιο έχει
  * θερμόμετρο
  * χειριστήριο αλλαγής θερμοκρασίας
  * αγωγούς που με κινητήρες μεταφέρουν θερμότητα (αέρα) προς/από άλλα δωμάτια
      * κάποια δωμάτια επικοινωνούν με κάποια άλλα
          * δεν υπάρχουν όλοι οι συνδυασμοί.

Ένα κεντρικό σύστημα
  * επεξεργάζεται τα δεδομένα
      * των θερμοκρασιών
      * των χειριστηρίων
      * παλαιότερη γνώση και δεδομένα
  * εφαρμόζει τεχνικές τεχνητής νοημοσύνης
  * και αποφασίζει την μεταφορά θερμότητας μεταξύ δωματίων
      * ενεργοποιώντας τους κατάλληλους αγωγούς

## Είσοδος

  * Οι τρέχουσες θερμοκρασίες των δωματίων
  * Οι αυξομειώσεις / ρυθμίσεις που ζητά κάθε χώρος
  * Όλα τα σχετικά ιστορικά δεδομένα

## Έξοδος

  * Ενεργοποίηση των κινητήρων μεταφοράς θερμότητας
  
## Αναλογία με άλλα προβλήματα
Η μεταφορά θερμότητας μεταξύ δωματίων είναι ένας τρόπος επίδειξης του γενικότερου προβλήματος,
που είναι εύκολο να καταλάβει κανείς (αλλά όχι εύκολο να δει).

Η προσέγγισή μας εφαρμόζεται και σε άλλα παρόμοια προβλήματα, όπου θέλουμε
μια κατανομή / ισορροπία ενός αγαθού (θερμότητας) σε επίπεδα που δεν είναι ίσα,
αλλά εξαρτώνται και εξελίσσονται με βάση τοπικές ανάγκες (χειρισμούς).

Πολλές φορές αυτή η προσαρμοζόμενη κατανομή του αγαθού
έχει σχέση με την επιθυμία το αγαθό να είναι κοντά στη ζήτηση του.
Όταν υπάρχουν δυσκολίες / περιορισμοί στη μεταφορά του αγαθού,
ειδικά όταν η μεταφορά δεν μπορεί να γίνει στιγμιαία,
αυτή πρέπει να γίνεται προληπτικά νωρίτερα, με βάση τις εκτιμώμενες ανάγκες.

Για παράδειγμα:
  * Κατανομή ενέργειας σε μονάδες αποθήκευσής της
  * Κατανομή νερού σε κοντινές δεξαμενές
  * Κατανομή τροφίμων στους χώρους κατανάλωσης
  * Κατανομή προμηθειών / εφοδίων στους χώρους ζήτησης
  * κ.λπ.

## Υλικά

Ένα microbit, θα λειτουργεί ως μονάδα εισόδου/εξόδου σε κάθε δωμάτιο:
θερμοστάτης / χειριστήριο αλλά και ως ενεργοποιητής των κινητήρων.

Ένα raspberry pi θα λειτουργεί ως το κεντρικό σύστημα υπολογισμού

Ένα microbit (με zip halo) θα δείχνει / επεξηγεί την κατάσταση και τις ενέργειες του συστήματος

## Λίστα Υλικών

Εξάρτημα | Ποσότητα
--- | ---
BBC Micro:bit V2 Board (Bulk) | 4
Compact All-In-One Robotics Board for BBC micro:bit | 2
Βηματικός Κινητήρας | 2
Waveshare Driver Breakout for micro:bit | 1
servo motor + mount | 1
ZIP Halo for the BBC micro:bit | 1
Raspberry Pi 5 - 8GB | 1
Raspberry Pi 5 Case White/Red | 1

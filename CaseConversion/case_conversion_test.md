## I. Basic Case Conversion (Lower to Upper and Vice-Versa)
- Test 1: Simple Lowercase to Uppercase:
	- Input: "αβγδεζηθικλμνξοπρστυφχψω"
	- Expected Output (Uppercase): "ΑΒΓΔΕΖΗΘΙΚΛΜΝΞΟΠΡΣΤΥΦΧΨΩ"
*`Purpose: Check the basic lowercase to uppercase conversion for all letters.`*
- Test 2: Simple Uppercase to Lowercase:
	- Input: "ΑΒΓΔΕΖΗΘΙΚΛΜΝΞΟΠΡΣΤΥΦΧΨΩ"
	- Expected Output (Lowercase): "αβγδεζηθικλμνξοπρστυφχψω"
*`Purpose: Check the basic uppercase to lowercase conversion for all letters.`*
- Test 3: Mixed Case:
	- Input: "ΑβΓδΕζΗθΙκΛμΝξΟπΡσΤυΦχΨω"
	- Expected Output (Uppercase): "ΑΒΓΔΕΖΗΘΙΚΛΜΝΞΟΠΡΣΤΥΦΧΨΩ"
	- Expected Output (Lowercase): "αβγδεζηθικλμνξοπρστυφχψω"
*`Purpose: Test mixed input to both all caps and all lowercase.`*
## II. Sigma Handling (Final vs. Non-Final)
- Test 4: Non-Final Sigma to Uppercase (Simple Word):
	- Input: "συνάδελφος"
	- Expected Output (Uppercase): "ΣΥΝΑΔΕΛΦΟΣ"
*`Purpose: Check the 'σ' to 'Σ' conversion in a word with no final sigma.`*
- Test 5: Final Sigma to Uppercase in multi-word string:
	- Input: "Ένας καλός κόσμος είναι εδώ"
	- Expected Output (Uppercase): "ΕΝΑΣ ΚΑΛΟΣ ΚΟΣΜΟΣ ΕΙΝΑΙ ΕΔΩ"
*`Purpose: Test sigma conversion when it is at the end of a word inside a string of words.`*
- Test 6: Final Sigma to Lowercase:
	- Input: "ΣΑΣ"
	- Expected Output (Lowercase): "σας"
*`Purpose: Test that uppercase sigma converts back to lowercase final sigma if in the last letter of the word.`*
- Test 7: Multiple Sigmas in a Word (Mixed Cases):
	- Input: "Συσσωματώσεις"
	- Expected Output (Lowercase): "συσσωματώσεις"
	- Expected Output (Uppercase): "ΣΥΣΣΩΜΑΤΩΣΕΙΣ"
*`Purpose: Verify handling of multiple sigmas, in particular in lowercase.`*
- Test 8: Final Sigma Before a Punctuation:
	- Input: "Ο καιρός ήταν καλός."
	- Expected Output (Uppercase): "Ο ΚΑΙΡΟΣ ΗΤΑΝ ΚΑΛΟΣ."
*`Purpose: Check that a final sigma will properly change in uppercase even if it is followed by a punctuation`*
- Test 9: Final Sigma BeforeAfter a Punctuation:
	- Input: "Ο ΚΑΙΡΟΣ ΗΤΑΝ ΚΑΛΟΣ."
	- Expected Output (Lowercase): "Ο καιρός ήταν καλός."
*`Purpose: Check that a final sigma will properly change in uppercase even if it is followed by a punctuation`*
## III. Accents Handling (Correct - No Changes)
- Test 10: Lowercase Accented Vowels to Uppercase (All Accents):
	- Input: "άέήίόύώ"
	- Expected Output (Uppercase): "ΑΕΗΙΟΥΩ"
*`Purpose: Verify accents are removed on uppercase conversion of fully-uppercase text.`*
- Test 11: Uppercase to Lowercase with Accents:
	- Input: "ΑΕΗΙΟΥΩ"
	- Expected Output (Lowercase): "αεηιουω"
*`Purpose: Verify accents are NOT added back when converting to lowercase.`*
- Test 12: Title Case with Accented First Letter:
	- Input: "Άλφα"
	- Expected Output (Title Case - First Letter Uppercase): "Άλφα"
*`Purpose: Check that title case does not strip out the accent.`*
- Test 13: Title case when accented letter is not first:
	- Input: "πολύ"
	- Expected Output (Title case): "Πολύ"
*`Purpose: Check that title case does not add accents in subsequent letters.`*
- Test 14: Title case when uppercase letter is not the first:
	- Input: "ΆΛφα"
	- Expected Output (Title Case): "Άλφα"
*`Purpose: Check that title case preserves accent if it exists in uppercase and the first letter of the word.`*
- Test 15: Accented word in sentence:
	- Input: "Αυτό είναι το σωστό"
	- Expected Output (Title case): "Αυτό Είναι Το Σωστό"
*`Purpose: Test that title case properly handles accented first letters when multiple words are present.`*
- Test 16: Title case with no accents:
	- Input: "αλφα"
	- Expected Output (Title Case): "Αλφα"
*`Purpose: Test that title case does add an accent if it's the standard form of that uppercase letter.`*
## IV. Dieresis Handling (Revised Again!)
- Test 17: Lowercase Dieresis:
	- Input: "ϊϋ"
	- Expected Output (Uppercase): "ΪΫ"
*`Purpose: Verify dieresis is preserved on uppercase conversion.`*
- Test 18: Accented Dieresis:
	- Input: "ΐΰ"
	- Expected Output (Uppercase): "ΪΫ"
*`Purpose: Verify dieresis is preserved and accents are removed on uppercase conversion.`*
- Test 19: Uppercase to Lowercase Accented Dieresis:
	- Input: "ΪΫ"
	- Expected Output (Lowercase with accents and dieresis): "ϊϋ"
*`Purpose: Verify proper conversion and re-introduction of dieresis and accents after going through uppercase`*
## V. Combined Cases, Accents, and Dieresis (Revised)
- Test 20: Complex Mixed Input:
	- Input: "άβγδΈζηθΙκλμνξόπρσΤυφχψώϊϋΐΰ"
	- Expected Output (Uppercase): "ΑΒΓΔΕΖΗΘΙΚΛΜΝΞΟΠΡΣΤΥΦΧΨΩΪΫΪΫ"
	- Expected Output (Lowercase): "αβγδέζηθικλμνξόπρστυφχψωϊϋΐΰ"
*`Purpose: Test all rules in a single, complex input.`*
- Test 21: A sentence with all edge cases included:
	- Input: "Ο καλλιτέχνης έδωσε το έργο με στυλ ϊου."
	- Expected Output (Uppercase): "Ο ΚΑΛΛΙΤΕΧΝΗΣ ΕΔΩΣΕ ΤΟ ΕΡΓΟ ΜΕ ΣΤΥΛ ΪΟΥ."
	- Expected Output (Title Case): "Ο Καλλιτέχνης Έδωσε Το Έργο Με Στυλ Ίου."
*`Purpose: A real-world sentence that covers most of the cases we are testing.`*
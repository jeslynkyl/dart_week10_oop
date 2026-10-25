# Dart Exercises - Object-Oriented Programming

**Name:** Jeslyn Kyl Sesma
**Section:** 3.3 BSIT
**Course:** NTC_PC16 - Mobile Development w/ Lab

---

## Week 10: Enhanced OOP App (Inheritance, Polymorphism, Abstract Classes, Mixins)

### Description
This console-based Dart program extends the Week 9 `Student` class into a class hierarchy. `Student` is now an abstract base class, with two derived classes that behave differently. A mixin adds logging to classes outside the Student hierarchy.

### Files
| File | Description |
|---|---|
| `week10_student_hierarchy.dart` | Source code for the hierarchy, mixin and `main()` |
| `output_week10.txt` | Sample program output |

### Class Structure
```
Loggable (mixin)
   |-- Instructor
   |-- Course

Student (abstract)
   |-- UndergraduateStudent
   |-- GraduateStudent
```

### OOP Concepts Applied
| Concept | Where it is used |
|---|---|
| **Inheritance** | `UndergraduateStudent` and `GraduateStudent` both `extends Student`. |
| **Polymorphism** | Both subclasses override `passingGrade` and `level`, and `GraduateStudent` also overrides `showReport()`. A `List<Student>` calls the correct version for each object. |
| **Abstract class** | `Student` is `abstract`. The getters `passingGrade` and `level` are abstract, so every subclass must implement them. |
| **Mixin** | `Loggable` is added with `with` to `Instructor` and `Course`, which are outside the Student inheritance chain. |
| **Encapsulation** (from Week 9) | `_grades` is private, read through the `grades` getter and updated through `addGrade()` and `removeGrade()` with validation (0-100). |
| **Constructor** | Each class sets its initial values, and subclasses pass shared values to the base class with `super`. |
| **List / Map** | `_grades` is a `Map<String, double>`, and `students` and `_enrolled` are `List<Student>`. |

### Sample Behavior
The same `standing` logic gives different results because each subclass has its own passing grade:
- **Undergraduate** passing grade is 75.
- **Graduate** passing grade is 85.

### How to Run
1. Open [DartPad](https://dartpad.dev).
2. Copy the contents of `week10_student_hierarchy.dart` into the editor.
3. Click **Run**.

Or, with the Dart SDK installed:
```bash
dart run week10_student_hierarchy.dart
```

---

## Week 9: Student Class (OOP Basics)
A `Student` class with a constructor, private `_grades` field, getter, and a `Map` of subject grades. Covered classes, constructors, encapsulation and Lists/Maps.

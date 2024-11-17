# prmlassignment2

\Solution to the Intersecting Set Problem

The Intersecting Set problem is defined as follows:
	•	We are given:
	•	A universe ￼.
	•	A family ￼ of disjoint subsets of ￼.
	•	A family ￼ of subsets of ￼, each associated with a budget ￼.
	•	The objective is to find a subset ￼ of minimum size such that:
	1.	For each ￼, ￼. This ensures that ￼ intersects every set in ￼.
	2.	For each ￼, ￼. This ensures that ￼ does not exceed the budget constraints for sets in ￼.

We aim to show that the Intersecting Set problem is NP-complete by reducing it from the known NP-complete Set Cover problem.

Steps for Proving NP-Completeness

	1.	Problem Restatement (Intersecting Set Problem):
	•	Find a subset ￼ such that:
	•	Intersection Condition: ￼ intersects each ￼ (i.e., covers all sets in ￼).
	•	Budget Condition: For each ￼, ￼.
	2.	Reduction from Set Cover Problem:
	•	Set Cover Problem Definition:
	•	Input: A universe ￼ and a collection ￼ of subsets of ￼.
	•	Goal: Find a sub-collection ￼ such that the union of all sets in ￼ covers ￼ and ￼ is minimized.
	•	We will reduce this problem to the Intersecting Set problem.
	3.	Constructing the Reduction:
	•	Let ￼ and ￼ be the inputs for the Set Cover problem.
	•	Construct an instance of the Intersecting Set problem as follows:
	•	Universe ￼: Use the same universe ￼ from the Set Cover instance.
	•	Family ￼: Create ￼ such that each element ￼ corresponds to a singleton set ￼ in ￼. This ensures that any valid subset ￼ must contain at least one element from each ￼, thereby covering all elements of ￼.
	•	Family ￼: Let ￼, where each set ￼ in the Set Cover problem is associated with a budget ￼. This budget allows any subset ￼ to include all elements in ￼ without exceeding ￼.
	4.	Properties Verification:
	•	Condition 1 (Intersection Condition): For each ￼, ￼. Since ￼ consists of singleton sets ￼, this condition ensures that ￼ must contain at least one element from each singleton in ￼, thereby covering ￼.
	•	Condition 2 (Budget Condition): For each ￼, ￼. By setting ￼, we ensure that any subset ￼ can fully include any ￼ without exceeding the budget, allowing a valid solution to use each set in ￼ if needed.
	5.	Correctness of the Reduction:
	•	A feasible solution to the Intersecting Set problem corresponds to a subset ￼ that intersects every singleton ￼ in ￼, ensuring that ￼ covers ￼. This is equivalent to a solution of the Set Cover problem.
	•	Any solution ￼ that satisfies both conditions (Intersection and Budget) in the Intersecting Set problem will also satisfy the conditions for a solution to the Set Cover problem.
	•	Thus, any solution to the Intersecting Set problem can be mapped back to a solution of the Set Cover problem, proving that the reduction is valid.
	6.	NP-Completeness Conclusion:
	•	The Set Cover problem is NP-complete, and we have constructed a polynomial-time reduction from Set Cover to the Intersecting Set problem. Therefore, the Intersecting Set problem is also NP-complete.

Final Remarks

The reduction demonstrates that the Intersecting Set problem is at least as hard as the Set Cover problem, as any solution to the Intersecting Set problem can be translated into a solution for the Set Cover problem. Thus, we have proven that the Intersecting Set problem is NP-complete.

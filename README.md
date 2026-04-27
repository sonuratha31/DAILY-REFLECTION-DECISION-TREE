# Daily Reflection Deterministic Decision Tree (v2.0)

## Description
This project implements a deterministic decision tree for daily self-reflection.  
Each input leads to a clear and consistent output using condition-based logic, avoiding ambiguity.

---

## Decision Logic

IF priority_done = yes → priority = done  
ELSE IF blocker_external = yes → priority = external_miss  
ELSE → priority = self_miss  

IF anxious OR flat → emotion = negative  
ELSE IF energized → emotion = positive  
ELSE → emotion = neutral  

IF goal_action = yes:
    IF focus_minutes ≥ 30 → progress = deep  
    ELSE → progress = light  
ELSE → progress = none  

IF repeated_mistake = yes:
    IF rule_exists = yes → improvement = recommit_rule  
    ELSE → improvement = define_new_rule  
ELSE → improvement = none
{
  "priority_status": "done | external_miss | self_miss",
  "emotion": "negative | neutral | positive",
  "progress": "deep | light | none",
  "improvement": "recommit_rule | define_new_rule | none"
}
## AI Usage and Refinement

- Used AI tools to generate an initial version of the decision tree
- Identified issues such as ambiguity, subjective inputs, and missing conditions
- Refined the structure by converting inputs into clear yes/no conditions
- Removed non-deterministic elements and ensured consistent output paths
- Simplified the overall logic to make the system more structured and reliable

---

## Output Format

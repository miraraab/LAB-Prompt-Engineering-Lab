# lab_summary.md

I tested three AI tasks — sentiment classification, product description, 
and data extraction — starting with vague instructions that produced 
completely inconsistent outputs, sometimes as low as 6.7% consistency 
across 15 runs. By adding clear format rules, worked examples, and 
step-by-step reasoning instructions, all three tasks reached 100% 
consistency. The biggest lesson I learned was that a single well-placed 
constraint — like "respond with exactly one word" — can be more powerful 
than a long, elaborate prompt. I also realized that measuring success the 
wrong way can hide real progress: creative tasks need to be judged on 
structure and format, not on whether every word matches exactly. Next 
time, I would define what "good output" looks like before writing a 
single prompt.

and to go a bit more into detail:
Moving from v1 to v3, the most impactful step was simply adding 
format constraints — one rule like "respond with exactly one word" 
moved Sentiment from 26% to 100% without a single example, proving 
that most prompt failures are structural, not conceptual. Few-shot 
prompting fixed format problems by showing the model a complete 
pattern to follow, while Chain-of-Thought fixed reasoning problems 
by forcing the model to think step by step before outputting — 
choosing between them comes down to one question: is the model 
formatting wrong or thinking wrong? In production, these techniques 
only work reliably when combined with systematic testing across at 
least 15 runs and a clear evaluation metric defined before writing 
any prompt — because a prompt that works once proves nothing.
How I will remember the learnings: pdf creation by Claude https://drive.google.com/drive/folders/1Ta4bGZ8Gb1PiR0GL8r8Ex6VWD5R8pIrQ
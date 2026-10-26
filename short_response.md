# Short Responses

For this short response assignment, aim to write a response with the following
qualities (your instructor will give you feedback on these areas):

- [ ] Addresses all parts of the prompt
- [ ] Accurately uses relevant technical terminology
- [ ] Is free of grammar and spelling mistakes (double check with Grammarly!)
- [ ] Uses markdown to enhance readability (preview in VS Code with
      Command/Control + Shift + V)
- [ ] Is easy to comprehend

Write your response in the space provided. Make sure to preview your markdown
to check how it is rendered before submitting.

## Question 1

A gym charges its members $5 for every visit, but never more than $40 in a
month. Devon wrote this function, and then wrote a test for it:

```py
# src/fees.py
def get_monthly_fee(visits):
    """$5 per visit, but never more than $40 in a month."""
    fee = visits * 5
    if fee > 40:
        fee = 40
    return fee
```

```py
# tests/test_fees.py
from src.fees import get_monthly_fee


def test_get_monthly_fee():
    """get_monthly_fee - charges $5 per visit"""
    assert get_monthly_fee(3) == 15
```

The test passed. A month later, Rosa refactored the function and changed one
line, from `if fee > 40:` to `if visits > 40:` even though the policy of "never more
than $40" never changed. Rosa ran the tests, saw them
pass, and shipped the change. Now members who visit 10 times in a month are
being charged $50 instead of $40.

### Prompt 1

_Note_: Read up on [Test-Driven Development in the GitBook](https://marcylabschool.gitbook.io/swe/computational-thinking-and-responsible-use-of-ai/mod-1-python-fundamentals/10-test-driven-development) before writing your response

Use these terms correctly within your response:

- **assert**
- **refactor**
- **test-driven development**

Explain why the tests passed even though the function was broken. Cover all three:

- What `assert get_monthly_fee(3) == 15` actually checks, and why it still
  passed after Rosa's change. Reference specific code that contributed to this
  behavior.
- The test or tests Devon should have written, as code, so that Rosa's change
  would have failed. Say which aspect of the gym's pricing policy each test checks.
- Suppose Devon had written your tests _first_, before the `if` statement that
  caps the fee existed. For example:

  ```py
  def get_monthly_fee(visits):
      fee = visits * 5
      return fee
  ```

  What would pytest have reported on the first run, and
  why is that failing result useful rather than a problem?

### Response 1

Your response here...

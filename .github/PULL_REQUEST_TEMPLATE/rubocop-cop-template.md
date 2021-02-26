---
name: Rubocop Cop template
about: Use this template when proposing to enable/disable a certain cop.
title: Enabled <Lint/ShadowingOuterLocalVariable> cop
labels: ''
assignees: ''

---

<!--
A brief description of why you are making the changes. Aim to keep this high level and 
understandable for the wider team. 
-->
## 💡 Why
[Asana Card]()

<!-- Full cop name and link to docs.rubocop.org -->
[Lint/ShadowingOuterLocalVariable](https://docs.rubocop.org/rubocop/cops_lint.html#lintshadowingouterlocalvariable)

<!-- RDoc link -->
[Rdoc](https://www.rubydoc.info/gems/rubocop/RuboCop/Cop/Lint/ShadowingOuterLocalVariable)

<!--
Default setting. You can find this on https://github.com/rubocop-hq/rubocop/blob/master/config/default.yml
(or the Rspec/plugin equivalent). Make sure to copy from the version of Rubocop that we currently have in our Gemfile.

It is important to include all options here and which option you are proposing to use (and why).
-->
```
Lint/ShadowingOuterLocalVariable:
  Description: >-
                 Do not use the same name as outer local variable
                 for block arguments or block local variables.
  Enabled: true
  VersionAdded: '0.9'
```

<!--
Example code from docs. This is to take a "snapshot" of what we agreed upon as just linking to the docs can get outdated.
-->
```
# bad

def some_method
  foo = 1

  2.times do |foo| # shadowing outer `foo`
    do_something(foo)
  end
end

# good

def some_method
  foo = 1

  2.times do |bar|
    do_something(bar)
  end
end
```

<!-- 
What changes are you making? The goal is to make it quick & easy for reviewers to get up to speed.
* Important additions/removals
* Important changes
* Major decisions
* How to review 
-->
## 📝 What

<!-- If you enabled/disabled the cop and what other options you've used. Also include additional notes here like if it's going to be updated in a future version etc. -->

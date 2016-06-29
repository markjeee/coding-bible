require 'rake'
require 'pp'

desc 'Update our copy of the style guide from the original at github:bbatsov'
task :update_ruby_style_guide do
  rsg_source = 'https://raw.githubusercontent.com/bbatsov/ruby-style-guide/master/README.md'
  rsg_output = 'ruby-style-guide.md'

  prepend_layout = <<PPLAYOUT
---
layout: page
---

```
# To keep this updated, run and commit updates.
rake update_ruby_style_guide
```

PPLAYOUT

  command = 'curl -s %s' % rsg_source
  original = `#{command}`
  new = prepend_layout + original

  written = File.write(rsg_output, new)
  puts 'Updated file %s (%d bytes)' % [ rsg_output, written ]
end

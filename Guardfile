rspec_options = {
  cmd: 'rspec -f nested',
  keep_failed: true,
  all_after_pass: true,
  all_on_start: true,
  run_all: {cmd: 'rspec -f progress'}
}

guard 'rspec', rspec_options do
  watch(%r{^spec/.+_spec\.rb$})
  watch(%r{^lib/(.+)\.rb$})     { |m| "spec/lib/#{m[1]}_spec.rb" }

  watch(%r{lib/roadie/rspec/.*\.rb}) { "spec" }

  watch(%r{spec/support/.*\.rb}) { "spec" }
  watch('spec/spec_helper.rb')   { "spec" }
end


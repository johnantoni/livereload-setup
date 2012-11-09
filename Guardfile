guard 'bundler', notify: false do
  watch('Gemfile')
end

guard 'pow', cli: '--notify false', restart_on_start: true, restart_on_reload: false do
  watch('.powrc')
  watch('.powenv')
  watch('.rvmrc')
  watch('Gemfile')
  watch('Gemfile.lock')
  watch('config/**/*.rb')
  watch('lib/routes/**/*.rb')
end

guard 'livereload', host: 'tutorbuddies.dev' do
  watch(%r{app/controllers/.+\.(rb)$})
  watch(%r{app/models/.+\.(rb)$})
  watch(%r{app/helpers/.+\.rb})
  watch(%r{app/views/.+\.(erb|haml|slim)$})
  watch(%r{public/.+\.(css|js|html)})
  watch(%r{config/locales/.+\.yml})
  # Rails Assets Pipeline
  watch(%r{app/assets/.+\.(js|coffee|css|scss|sass|less|jpg|jpeg|gif|png)$})
  watch(%r{(app|vendor)/assets/\w+/(.+\.(css|js|html)).*})  { |m| "/assets/#{m[2]}" }
end

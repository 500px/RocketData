# Note: You must be using Cocoapods 1.0.0 or above

use_frameworks!

target :'RocketData' do
  pod 'ConsistencyManager', :git => 'https://github.com/linkedin/ConsistencyManager-iOS', :commit => 'e75ed7adec5ec0eeebfa649262357dbe029cefe6'
end

target :'RocketDataTests' do
  pod 'ConsistencyManager', :git => 'https://github.com/linkedin/ConsistencyManager-iOS', :commit => 'e75ed7adec5ec0eeebfa649262357dbe029cefe6'
end

# This is necessary to convert the target to swift 4.0
# This isn't detected automatically by cocoapods or supported in the podspec
# We can remove this once Cocoapods has a better solution
post_install do |installer|
    installer.pods_project.targets.each do |target|
        target.build_configurations.each do |config|
            config.build_settings['SWIFT_VERSION'] = '4.0'
        end
    end
end
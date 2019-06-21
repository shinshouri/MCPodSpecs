This is our private Podspec repository
After developing your pod :

Push your code to : {YOUR_POD_REPO}


Tag your committed code for versioning
Make sure your podspec file is right 
the version is right / match with tag & source is directed to your pod repo
s.version      = "0.0.1"
s.source = { :git => 'https://github.com/shinshouri/{YOUR_POD_REPO}.git', :tag => "#{s.version}" }

If haven't, add this repo by running this command :
$ pod repo add PrivateTrunk https://github.com/shinshouri/MCPodSpecs.git

Push your podspec file to this repo PrivateTrunk
$ pod repo push PrivateTrunk MCUtils.podspec --verbose --allow-warnings

On the project you will be using / installing the pod,
add this following line at the top of your podfile

source 'https://github.com/shinshouri/MCPodUtils.git'
source 'https://github.com/shinshouri/MCPodUtils'

and then as usual on your podfile:

pod 'MCUtils', '0.0.1'

for pod install, to check if there is any update in the PrivateTrunk better put --repo-update when installing
$ pod install --repo-update


Thank You

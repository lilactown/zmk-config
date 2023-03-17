hummingbird_keymap.svg: hummingbird_keymap.yaml keymap_config.yaml
	keymap -c keymap_config.yaml draw \
	 hummingbird_keymap.yaml > hummingbird_keymap.svg

hummingbird_keymap.yaml: 30key.keymap hummingbird.keymap keymap_config.yaml
	cp hummingbird_keymap.yaml base.yaml
	keymap -c keymap_config.yaml parse \
	 --base-keymap base.yaml \
	 -z hummingbird.keymap > hummingbird_keymap.yaml

# keymap.yaml is technically circular
parse:
	cp hummingbird_keymap.yaml base.yaml
	keymap -c keymap_config.yaml parse \
	 --base-keymap base.yaml \
	 -z hummingbird.keymap > hummingbird_keymap.yaml

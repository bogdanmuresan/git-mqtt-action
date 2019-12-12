# git-mqtt-action

workflow "My build" {
  resolves = [
    "mqtt command",
  ]
  on = "push"
}

action "mqtt command" {
  uses = "bogdanmuresan/git-mqtt-action@v0.0.1"
  args = "pub -t deploy_topic -m "My deployment updates" -h mqtt.eclipse.org"
}

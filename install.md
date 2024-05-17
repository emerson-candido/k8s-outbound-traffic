helm -n falco upgrade falco --install --create-namespace \
    --set driver.kind=modern_ebpf \
    --set tty=true \
    --set falcosidekick.enabled=true \
    --set falcosidekick.webui.enabled=true \
    --set ebpf.enabled=true \
    -f custom-rules.yaml \
    falcosecurity/falco

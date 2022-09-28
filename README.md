# What is this?
Certain Gigabyte motherboards suffer from an issue that causes the GPP0 device (PCIe bridge for NVMe drive) to erroneously wake up the system from suspension/hibernation. This systemd service automatically disables ACPI wakeup for this device, fixing the issue.

# Usage
- Copy the file disable-gpp0-wakeup.service to /etc/systemd/system
- Enable and start it with systemd: systemctl enable --now disable-gpp0-wakeup.service

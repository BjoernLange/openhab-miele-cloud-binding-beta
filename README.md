# openHAB Miele Cloud Binding Beta
This repository serves as host for the documentation and issue tracker for the beta versions of the [Miele Cloud Binding](https://www.openhab.org/addons/bindings/mielecloud/) for [openHAB](https://www.openhab.org/).

## Quick Links
- [Documentation](https://github.com/BjoernLange/openhab-miele-cloud-binding-beta/blob/master/Documentation.md)
- [Issue Tracker](https://github.com/BjoernLange/openhab-miele-cloud-binding-beta/issues)
- [Tutorial: Querying the cloud status](https://github.com/BjoernLange/openhab-miele-cloud-binding-beta/blob/master/Query-Cloud-Status.md)
- [Tutorial: Querying live updates from the cloud](https://github.com/BjoernLange/openhab-miele-cloud-binding-beta/blob/master/Query-Live-Updates.md)

## FAQ

### Is the binding closed source?

No, the binding is open sourced and officially part of openHAB since openHAB 3.1.0.

### Are you maintaining the beta versions for openHAB 2.5.x and 3.x in parallel? Are you providing further releases for openHAB 2.5.x?

No, maintaining the binding for openHAB 2.5.x and 3.x at the same time is too much effort in our case. Targeting both versions requires some changes of which not all can be automated:
- Replacements of imports: Can be easily automated.
- Changes when using 3rd party libraries: openHAB 2.5.x uses JUnit 4 while openHAB 3.x uses JUnit 5. This requires some complex migrations that cannot be automated easily. We needed to make a choice here: Support two versions and drop the tests for one, making it possibly break without us noticing, or only support one well-tested version. We prefer the latter.
- Adapting to changed openHAB APIs: We use some of the changed APIs in the backend of the configuration UI, see [here](https://github.com/openhab/openhab-addons/pull/9146#issue-528723209) for details (last paragraph).

### How can I see the raw status of my devices in the cloud?

We wrote a [tutorial](https://github.com/BjoernLange/openhab-miele-cloud-binding-beta/blob/master/Query-Cloud-Status.md) on how to do this.

### How can I check whether live updates from the cloud are working?

We wrote a [tutorial](https://github.com/BjoernLange/openhab-miele-cloud-binding-beta/blob/master/Query-Live-Updates.md) on how to do this.

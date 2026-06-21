Hello!
======

<table>
<tr>
<td width="200px">
<img src="media/avatar.jpg" alt="IDCT Bartosz Pachołek, my photo" width="200">
</td>
<td>
I'm an open‑source developer from Poland, passionate about creating practical apps and libraries. Everything I share on GitHub is completely free to use, released under MIT or Apache licenses—so you're welcome to adapt, build upon, or enjoy them in any way that suits you.
<br><br>
I hope that, in time, this brand will grow into a fully established company—right now it's officially registered in Poland, though it's still just me behind it. For the moment, I'm sharing the software tools I find most useful in my everyday work, with the hope that they'll also support you on your own software journey.
</td>
</tr>
</table>

# Notable software

Explore some of my software projects—you may already find them practical and ready to use.

<table>
<tr>
<td width="80" align="center" valign="middle" rowspan="2"><picture><source media="(prefers-color-scheme: dark)" srcset="media/symfony-white.svg"><img src="media/symfony.svg" alt="Symfony" width="56"></picture></td>
<td><big><strong><a href="https://github.com/ideaconnect/symfony-nats-messenger">Symfony NATS Messenger [PHP]</a></strong></big></td>
</tr>
<tr>
<td>

A Symfony Messenger transport that bridges Symfony's message bus to NATS JetStream, handling message production/consumption and stream/consumer management. Configured via DSN in the form `nats-jetstream://[user:password@]host:port/stream/topic`, with a `nats-jetstream+tls://` variant for TLS.

</td>
</tr>
<tr>
<td colspan="2">

- Durable consumers with explicit ACK (optional double-ack), NAK-based redelivery handled either by NATS or by Symfony's own retry; tunable `ack_wait`, `max_deliver`, `backoff`, and `nak_delay`.
- Batch consumption, delayed messages via `DelayStamp` (NATS ≥ 2.12), multi-subject streams, and per-stream configuration (retention, storage, replicas).
- Authentication via user/password, token, JWT, NKey, or TLS certificates. Requires PHP ^8.2 and `symfony/messenger` ^7.2 || ^8.0; depends on `idct/php-nats-jetstream-client`. MIT.

</td>
</tr>
</table>

<table>
<tr>
<td width="80" align="center" valign="middle" rowspan="2"><img src="media/php.svg" alt="PHP" width="56"></td>
<td><big><strong><a href="https://github.com/ideaconnect/php-nats-jetstream-client">PHP NATS JetStream Client [PHP]</a></strong></big></td>
</tr>
<tr>
<td>

An asynchronous PHP client for NATS and JetStream, built on the AMPHP event loop for non-blocking I/O over the NATS wire protocol.

</td>
</tr>
<tr>
<td colspan="2">

- Core NATS pub/sub and request-reply; JetStream stream and consumer management with pull and push consumers and explicit ack semantics.
- KeyValue and ObjectStore buckets, distributed counters, a microservices framework, and reconnection with exponential backoff.
- Requires PHP ^8.2 and `ext-openssl`; depends on `amphp/amp` and `amphp/socket`. Packagist `idct/php-nats-jetstream-client`, BSD-3-Clause. Underlies the Symfony NATS Messenger bridge.

</td>
</tr>
</table>

<table>
<tr>
<td width="80" align="center" valign="middle" rowspan="2"><img src="media/csharp.svg" alt="C#" width="56"></td>
<td><big><strong><a href="https://github.com/ideaconnect/rabbit-going-nats">Rabbit-going-NATS [C#]</a></strong></big></td>
</tr>
<tr>
<td>

Tool which allows to passthrough messages fetched from RabbitMQ's queue to NATS PubSub.

</td>
</tr>
<tr>
<td colspan="2">

Useful if you receive a data feed through RabbitMQ, but you need to redistribute it further to multiple clients in the most efficient way.

</td>
</tr>
</table>

<table>
<tr>
<td width="80" align="center" valign="middle" rowspan="2"><img src="media/go.svg" alt="Go" width="56"></td>
<td><big><strong><a href="https://github.com/ideaconnect/go-fyne-pretty-view">Go Fyne Pretty View [Go]</a></strong></big></td>
</tr>
<tr>
<td>

A memory-efficient, virtualized Fyne v2 widget for viewing structured data—JSON, JSONC, XML, HTML, and raw text—styled after Bruno's response viewer. Only viewport-visible rows exist as live canvas objects; the rest of the document is held in a compact struct-of-arrays model.

</td>
</tr>
<tr>
<td colspan="2">

- Syntax highlighting, format auto-detection with raw-text fallback, expand/fold with collapse summaries, character-level selection and copy, and copy key path (JSONPath).
- Plain and regex search with auto-reveal into folded nodes, optional word-wrap, a line-number gutter, and keyboard navigation.
- Optional in-place editing (v2, `WithEditable`): live highlighting, caret-preserving `Reformat`, undo/redo, and a live parse-validity status. Requires Go 1.25+ and `fyne.io/fyne/v2`. BSD-3-Clause.

</td>
</tr>
</table>

<table>
<tr>
<td width="80" align="center" valign="middle" rowspan="2"><img src="media/go.svg" alt="Go" width="56"></td>
<td><big><strong><a href="https://github.com/ideaconnect/helena">Helena [Go]</a></strong></big></td>
</tr>
<tr>
<td>

A cross-platform native desktop API client (an alternative to Postman/Bruno) written in Go with the Fyne toolkit, distributed as a single self-contained binary with no Electron runtime.

</td>
</tr>
<tr>
<td colspan="2">

- Workspaces, collections, folders, and requests stored as Open Collection YAML for version control; auth secrets and Secret-flagged environment variables kept out of the YAML, in a per-collection store under the OS config dir.
- `{{variable}}` resolution across URL, query params, headers, and body; request chaining (before-hooks) and per-request pre/post JavaScript hooks (goja).
- Imports OpenAPI 3, Swagger 2, and WSDL (local file or URL); exports to cURL or wget; formats JSON/XML responses and flags CORS-blocked responses. Requires a C compiler and platform OpenGL libraries to build (Fyne uses cgo). BSD 4-Clause.

</td>
</tr>
</table>

<table>
<tr>
<td width="80" align="center" valign="middle" rowspan="2"><img src="media/php.svg" alt="PHP" width="56"></td>
<td><big><strong><a href="https://github.com/ideaconnect/idct-sftp-client">idct/sftp-client [PHP]</a></strong></big></td>
</tr>
<tr>
<td>

A typed, object-oriented PHP wrapper around the procedural `ext-ssh2` extension for file transfer over SSH, SCP, and SFTP. Composer package `idct/sftp-client`; namespace `IDCT\Networking\Ssh`, main class `SftpClient`.

</td>
</tr>
<tr>
<td colspan="2">

- SFTP upload/download with atomic temporary-file writes, one-shot SCP, resumable transfers, and stream sources/sinks; recursive directory upload/download/walk/remove with conflict and symlink policies.
- Exponential-backoff retry with reconnection, host-key fingerprint verification (SHA-1/SHA-256) against OpenSSH `known_hosts`, optional checksums, and path validation against traversal, control characters, and null bytes.
- Authentication via password, public key, combined, or anonymous; dynamic credentials via `CredentialsLoaderInterface`. Requires PHP ≥ 8.2 and `ext-ssh2` ≥ 1.4 (libssh2 ≥ 1.10).

</td>
</tr>
</table>

# 💖 Love my work? Support it! 🚀

* ☕ **Buy me a coffee**: https://buymeacoffee.com/idct
* 💝 **Sponsor**: https://github.com/sponsors/ideaconnect

I'm Emre, an IT student at Eastern Mediterranean University.
I write security tools in Python and web apps with Django,
mostly for my own server and home network.

## What I've built

<table>
<tr>
<td width="50%" valign="top">
<b><a href="https://github.com/rosko35/mini-siem">mini-siem</a></b> · log monitoring<br><br>
<b>Problem:</b> I wanted to see what was actually attacking my server without running a log stack heavier than the site itself.<br>
<b>Built:</b> A log reader with YAML detection rules, Telegram alerts and a read-only dashboard.<br>
<b>Decision:</b> It runs as a read-only guest. It touches no settings and opens no public port.<br>
<sub>Python · FastAPI · SQLite · Docker</sub>
</td>
<td width="50%" valign="top">
<b><a href="https://github.com/rosko35/ssh-honeypot">ssh-honeypot</a></b> · honeypot<br><br>
<b>Problem:</b> mini-siem showed brute force attempts, but not the passwords or what bots do once they get in.<br>
<b>Built:</b> A fake SSH server with an in-memory fake shell that records every attempt.<br>
<b>Decision:</b> No command ever runs and nothing is downloaded. The attacker never reaches a real shell.<br>
<sub>Python · asyncssh · SQLite</sub>
</td>
</tr>
<tr>
<td width="50%" valign="top">
<b><a href="https://github.com/rosko35/server-hardening">server-hardening</a></b> · Ansible<br><br>
<b>Problem:</b> Most hardening guides start with steps that can lock you out if done in the wrong order.<br>
<b>Built:</b> Playbooks that audit first, then apply one category at a time, with a rollback.<br>
<b>Decision:</b> By default it changes nothing. It only reads the server and writes a report.<br>
<sub>Ansible · Python · Lynis</sub>
</td>
<td width="50%" valign="top">
<b><a href="https://github.com/rosko35/net-traffic-analyzer">net-traffic-analyzer</a></b> · packet analysis<br><br>
<b>Problem:</b> I could read Wireshark's output but didn't really know what the bytes were.<br>
<b>Built:</b> A tool that reads packet captures and reports who talks to whom and what travels unencrypted.<br>
<b>Decision:</b> Every protocol decoder is written by hand, with no packet library.<br>
<sub>Python</sub>
</td>
</tr>
<tr>
<td width="50%" valign="top">
<b><a href="https://github.com/rosko35/homelab-security-panel">homelab-security-panel</a></b> · home network<br><br>
<b>Problem:</b> My projects worked on their own, but none could tell me if an unknown device had joined my network.<br>
<b>Built:</b> A device inventory, a weekly scan compared with the week before, and one Grafana panel for everything.<br>
<b>Decision:</b> Everything listens only locally unless told otherwise.<br>
<sub>Python · Docker · Grafana</sub>
</td>
<td width="50%" valign="top">
<b><a href="https://github.com/rosko35/ozaydin-dev">ozaydin-dev</a></b> · website<br><br>
<b>Problem:</b> I wanted a site that shows what I do instead of reading like a CV.<br>
<b>Built:</b> A bilingual portfolio and blog in Django, running on my own server.<br>
<b>Decision:</b> Pages open as text first. The 3D field loads afterwards.<br>
<sub>Django · Three.js · PostgreSQL · Nginx</sub>
</td>
</tr>
</table>

Open to long-term internships. [ozaydin.dev](https://ozaydin.dev)

# MVP Feed generator

Version 1:
- Tool intended to be run as scheduled job
- Query entire Demozoo production endpoint periodically (check with Gasman if this is the best approach):  http://demozoo.org/api/v1/productions/
- Download all linked files without clobbering
- SHA256 all files and push to cloud storage
- Create CSV or JSON file cross-referencing Demozoo ID with SHA256
- Name files by SHA256 value
- Create JSON feed for client to parse and download from

Version 2:
- Note extracted size to pass to client

# MVP Client

Version 1:
- Download / Update JSON feed containing metadata and URLs
- Download latest months productions and extract to Group\[Year] - Name

Version 2:
- Disk space handling
- Pattern matching downloading and extracting; like 

---

Potential command lines:

v1 demo-get update			Downloads latest JSON file containing all productions and SHA256 checksums

v1 demo-get download    Requires argument:
												all						All demos
												new						New demos (defaults to last month)
												
												Optional:
												--cache-only (cache without extracting)
												
v1 demo-get check				Audits cache folder so filename matches SHA256




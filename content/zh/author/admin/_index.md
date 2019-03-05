+++
# Display name
name = "CNI-Genie"

# Is this the primary user of the site?
superuser = true

# Role/position
role = "CNI-Genie enables container orchestrators (Kubernetes, Mesos) to seamlessly connect to the choice of CNI plugins installed on a host."

# Organizations/Affiliations
#   Separate multiple entries with a comma, using the form: `[ {name="Org1", url=""}, {name="Org2", url=""} ]`.
organizations = [ { name = "", url = "" } ]

# Short bio (displayed in user profile at end of posts)
bio = "My research interests include distributed robotics, mobile computing and programmable matter."

# Enter email to display Gravatar (if Gravatar enabled in Config)
email = ""

# List (academic) interests or hobbies
interests = []

# List qualifications (such as academic degrees)
#[[education.courses]]
#  course = "PhD in Artificial Intelligence"
#  institution = "Stanford University"
#  year = 2012

#[[education.courses]]
#  course = "MEng in Artificial Intelligence"
#  institution = "Massachusetts Institute of Technology"
#  year = 2009

#[[education.courses]]
#  course = "BSc in Artificial Intelligence"
#  institution = "Massachusetts Institute of Technology"
#  year = 2008

# Social/Academic Networking
#
# Icon pack "fab" includes the following social network icons:
#
#   twitter, weibo, linkedin, github, facebook, pinterest, google-plus,
#   youtube, instagram, soundcloud
#
#   For email icon, use "fas" icon pack, "envelope" icon, and
#   "mailto:your@email.com" as the link.
#
#   Full list: https://fontawesome.com/icons
#
# Icon pack "ai" includes the following academic icons:
#
#   cv, google-scholar, arxiv, orcid, researchgate, mendeley
#
#   Full list: https://jpswalsh.github.io/academicons/

#[[social]]
#  icon = "envelope"
#  icon_pack = "fas"
#  link = "#contact"  # For a direct email link, use "mailto:test@example.org".

#[[social]]
#  icon = "twitter"
#  icon_pack = "fab"
#  link = "https://twitter.com/GeorgeCushen"

#[[social]]
 # icon = "google-scholar"
 # icon_pack = "ai"
 # link = "https://scholar.google.co.uk/citations?user=sIwtMXoAAAAJ"

[[social]]
  icon = "github"
  icon_pack = "fab"
  link = "https://github.com/cni-genie/CNI-Genie"

# Link to a PDF of your resume/CV from the About widget.
# To enable, copy your resume/CV to `static/files/cv.pdf` and uncomment the lines below.
# [[social]]
#   icon = "cv"
#   icon_pack = "ai"
#   link = "files/cv.pdf"

+++
CNI-Genie enables container orchestrators (Kubernetes, Mesos) to seamlessly connect to the choice of CNI plugins installed on a host, including:  

1. ['reference' CNI plugins](https://github.com/containernetworking/plugins), e.g., bridge, macvlan, ipvlan, loopback
2. '3rd-party' CNI plugins, e.g., ([Calico](https://github.com/projectcalico/calico), [Romana](https://github.com/romana/romana), [Weave-net](https://github.com/weaveworks/weave))
3. 'specialized' CNI plugins, e.g., [SR-IOV](https://github.com/hustcat/sriov-cni), DPDK (work-in-progress)
4. any generic CNI plugin of choice installed on the host  

Without CNI-Genie, the orchestrator is bound to only a single CNI plugin. E.g., for the case of Kubernetes, without CNI-Genie, kubelet is bound to only a single CNI plugin passed to kubelet on start. CNI-Genie allows for the co-existance of multiple CNI plugins in runtime.

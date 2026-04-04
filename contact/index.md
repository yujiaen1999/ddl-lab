---
title: Contact
nav:
  order: 5
  tooltip: Email, address, and location
---

# {% include icon.html icon="fa-regular fa-envelope" %}Contact

We welcome inquiries from prospective students, collaborators, and researchers who are interested in our work. 
If you would like to learn more about our research, please feel free to reach out.

{%
  include button.html
  type="email"
  text="EMAIL US"
  link="jiy037@ucsd.com"
%}
<!-- {%
  include button.html
  type="phone"
  text="(000) 000-0000"
  link="+1-000-000-0000"
%} -->
{%
  include button.html
  type="address"
  tooltip="Our location on Google Maps for easy navigation"
  text="3234 Matthews Ln, La Jolla, CA 92093"
  link="https://maps.app.goo.gl/46EFXeZWULDuzMLr7"
%}

{% include section.html %}

{% capture col1 %}

{%
  include figure.html
  image="images/group_image_anime.png"
  caption=" "
%}

{% endcapture %}

{% capture col2 %}

{%
  include figure.html
  image="images/group_image_lego.png"
  caption=" "
%}

{% endcapture %}

{% include cols.html col1=col1 col2=col2%}


---
title: Thank You
layout: splash
header:
    overlay_color: "#F2A83B"
permalink: /thank-you/
excerpt: "Thank you for contacting Associated Eye Physicians. We've received your message and will get back to you soon."
description: "Thank you for reaching out to Associated Eye Physicians. Your message has been received and our team will respond promptly."
---

<div id="personalized-message"></div>

## What Happens Next?

- **Review**: Our staff will carefully review your message
- **Response**: We'll contact you via phone or email with next steps
- **Appointment**: If you're requesting an appointment, we'll help schedule at your preferred location

## Need Immediate Assistance?

If you have an urgent eye care concern, please call us directly:

- **Elizabeth Office**: [908-355-0478](tel:908-355-0478)
- **Clifton Office**: [973-472-6405](tel:973-472-6405)
- **Newark Office**: [973-589-0104](tel:973-589-0104)
- **Pompton Lakes Office**: [973-835-1222](tel:973-835-1222)
- **Westfield Office**: [908-232-0909](tel:908-232-0909)

## Our Services

While you wait for our response, learn more about our comprehensive eye care services:

- [Cataract Surgery](/cataract/)
- [Glaucoma Treatment](/glaucoma/)
- [Diabetic Eye Care](/diabetic-retinopathy/)
- [Pediatric Eye Care](/vision-loss/)
- [Contact Lenses & Eyeglasses](/contacts-eyeglasses/)

[← Back to Contact Page](/contact-page/) | [View Our Locations](/locations/)

<script>
// Get URL parameters
function getUrlParameter(name) {
    name = name.replace(/[\[]/, '\\[').replace(/[\]]/, '\\]');
    const regex = new RegExp('[\\?&]' + name + '=([^&#]*)');
    const results = regex.exec(location.search);
    return results === null ? '' : decodeURIComponent(results[1].replace(/\+/g, ' '));
}

// Display personalized message
const name = getUrlParameter('name');
const email = getUrlParameter('email');
const phone = getUrlParameter('phone');

if (name && (email || phone)) {
    const personalizedDiv = document.getElementById('personalized-message');
    if (personalizedDiv) {
        let contactInfo = '';
        if (email) {
            contactInfo += `at your email <strong>${email}</strong>`;
        }
        if (phone) {
            if (contactInfo) contactInfo += ' and ';
            contactInfo += `at your phone <strong>${phone}</strong>`;
        }

        personalizedDiv.innerHTML = `
            <div style="background-color: #f8f9fa; padding: 1rem; border-radius: 5px; margin-bottom: 2rem; border-left: 4px solid #F2A83B;">
                <p style="margin: 0; font-weight: bold;">Thank you for your message, ${name}!</p>
                <p style="margin: 0.5rem 0 0 0;">We will get back to you as soon as we can ${contactInfo}.</p>
            </div>
        `;
    }
}
</script>

# Dose Curve

A small offline web app (PWA) that plots an estimated Adderall IR blood-level curve over 24 hours.
Everything runs on the phone. Nothing is stored or sent anywhere.

## The model

- One-compartment curve with first-order absorption, added up across doses.
- Peak about 3 h after a dose. Half-life 10.4 h (d-amphetamine) and 12.65 h (l-amphetamine), mixed 3:1.
- These are average adult numbers from the FDA label for Adderall tablets.
- The y-axis is "% of one 10 mg peak". It's a planning aid, not dosing advice.

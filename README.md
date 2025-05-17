📞 **Inbound Call System – Appointment Management**

In addition to outbound cold calling, this system also handles inbound calls from patients. 
The virtual assistant can perform the following actions during a phone call:

-Book a new appointment

-Cancel an existing appointment

-Reschedule an existing appointment

🗓️ **How It Works**


✅ Booking a New Appointment

The patient calls the assistant.

The assistant asks for the patient’s name and complaint.

Then the assistant asks which date the patient would like to book an appointment for.

The assistant triggers the checkAvailable scenario via Make to verify slot availability.

If the selected time is available, the booking scenario is triggered, and the new booking flow creates the appointment.

If the selected time is not available, the assistant suggests three alternative time slots and proceeds to create the booking.

❌ Canceling an Appointment

The assistant retrieves the patient’s current appointment time.

It then triggers the cancel branch of the booking scenario to cancel the appointment.

🔁 Rescheduling an Appointment

The assistant first retrieves the patient’s current appointment time.

It calls the getPatientData scenario to obtain the relevant eventId and medical issue (disease).

The assistant asks the patient for a new preferred appointment time.

The checkAvailable module is used again to verify availability.

If available, the assistant triggers the reschedule branch of the booking scenario.

Using the previously retrieved eventId, the system updates the appointment in the calendar.

# OS-project-
Project -Question :
Consider a clinic with one doctor and a very large waiting room (of infinite capacity). Any
patient entering the clinic will wait in the waiting room until the doctor is free to see her.
Similarly, the the doctor also waits for a patient to arrive to treat. All communication between the
patients and the doctor happens via a shared memory buffer. Any of the several patient
processes, or the doctor process can write to it. Once the patient “enters the doctors office”, she
conveys her symptoms to the doctor using a call to consultDoctor(), which updates the shared
memory with the patient‟s symptoms. The doctor then calls treatPatient() to access the buffer and
update it with details of the treatment. Finally, the patient process must call noteTreatment() to
see the updated treatment details in the shared buffer, before leaving the doctor‟s office. A
template code for the patient and doctor processes is shown below. Enhance this code to
correctly synchronize between the patient and the doctor processes. Your code should ensure that
no race conditions occur due to several patients overwriting the shared buffer concurrently.
Similarly, you must ensure that the doctor accesses the buffer only when there is valid new
patient information in it, and the patient sees the treatment only after the doctor has written it to
the buffer. You must use only semaphores to solve this problem. Clearly list the semaphore
variables you use and their initial values first. Please pick sensible names for your variables.
(a) Semaphore variables and initial values:
(b) Patient process:
consultDoctor();
noteTreatment();
( c) Doctor process:
while(1)
{
treatPatient();
}

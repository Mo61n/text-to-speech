# How is this work :

The function PopulateVoices() is called, which populates the voices array with the available speech synthesis voices. 
If the browser supports speech synthesis, speechSynthesis.onvoiceschanged event listener is triggered to populate the voices array on voice changes.

When the btnSpeak button is clicked, an event listener is triggered.
This event listener creates a new SpeechSynthesisUtterance using the text from txtInput.value
It then selects the voice from voiceList.selectedOptions based on its name by iterating over the voice array using forEach,
and comparing the name of the voice with selectedVoiceName

Once the appropriate voice is found, it sets the voice property of the SpeechSynthesisUtterance object to the selected voice,
and finally initiates the speech outpt using synth.speak(toSpeak).

Finally, the PopulateVoices() function loops through the voices array to create a set of option elements for the voiceList dropdown menu.
Each option element is created using document.createElement() to create an option tag, which is then appended to the voiceList using voiceList.appendChild()
The new option tag is then populated with the name of the voice, as well as the specific lang and name details
Once all the available voices are added to the dropdown menu, the previously selected option index value is set as the selected index using voiceList.selectedIndex = selectedIndex

## CodePen :
https://codepen.io/Mo61n/pen/ZEMRjew

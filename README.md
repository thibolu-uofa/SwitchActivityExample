# 
This is an example for AUCSC 220 of a minimal Android Studio example demonstrating how to switch between activities using buttons. 
The app consists of two activities:

MainActivity.java – The main screen with a button to navigate to the second activity.
SecondActivity.java – The second screen with a button to return to the main activity.

# Step 1:
  Create your default Android project with one main Activity.
# Step 2:
  Create SecondActivity.java and activity_second.xml
# Step 3:
  Add the new activity to app/manifests/AndroidManifest.xml
      <activity android:name=".SecondActivity" />
# Step 4: 
  Add buttons.
# Step 5:
  Create the intent for each button and start the activity when the button is clicked. You may want to finish (or not) the current activity with the finish() function before moving on.
  For example, in the onCreate of the SecondActivity:
  
        Button button = findViewById(R.id.button_second);
        button.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                Intent intent = new Intent(SecondActivity.this, MainActivity.class);
                startActivity(intent);
                // finish();
            }
        });



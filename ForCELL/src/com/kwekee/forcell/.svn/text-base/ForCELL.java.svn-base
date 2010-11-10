package com.kwekee.forcell;

import android.app.Activity;
import android.app.AlertDialog;
import android.content.Intent;
import android.os.Bundle;
import android.view.Menu;
import android.view.MenuInflater;
import android.view.MenuItem;
import android.view.View;
import android.widget.TextView;
import android.widget.Toast;

public class ForCELL extends Activity {
    /** Called when the activity is first created. */
	 	 
	 @Override
	 public void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.main);
        
    }
    public boolean onCreateOptionsMenu(Menu menu) {
    	MenuInflater inflater = getMenuInflater();
        inflater.inflate(R.menu.menu, menu);
        

        return true;
    }
    public boolean onOptionsItemSelected(MenuItem item) {
        switch (item.getItemId()) {
            case R.id.settings:
            	Toast.makeText(this, "Work In Progress", Toast.LENGTH_SHORT).show();
                Intent settingsActivity = new Intent(getBaseContext(), Preferences.class);
                startActivity(settingsActivity);
                return true;
            case R.id.about:
            	showAbout();
            	return true;
            case R.id.close:
            	this.finish();
        }
        return false;
    }
    protected void showAbout() {
        View messageView = getLayoutInflater().inflate(R.layout.about, null, false);
        TextView textView = (TextView) messageView.findViewById(R.id.about_credits);
        int defaultColor = textView.getTextColors().getDefaultColor();
        textView.setTextColor(defaultColor);

        AlertDialog.Builder builder = new AlertDialog.Builder(this);
        builder.setIcon(R.drawable.about);
        builder.setTitle(R.string.app_version);
        builder.setView(messageView);
        builder.create();
        builder.show();
    }
}

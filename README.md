# ocrGit
Activité Partie 2

Voici le fichier README.txt qui explique cet Exercice.

Ici je vais vous montrer comment enregitrer un fichier dans SharedPreferences avavec Java.

//Voici le code
package com.exemple.app

public class MainActivity extends AppCompatActiviy{

private SharedPreferences preferences;
private static final String PREF_KEY_NAME_1 = "PREF_KEY_NAME_1";
private String NAME = "firstname";

@Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

	//Load default SharedPreferences, it's better to Load in MODE_PRIVATE
	 preferences = PreferenceManager.getDefaultSharedPreferences(this);

	 //Load the content you want to display, return null if there is no 
	 data

	 NAME = preferences.getString(PREF_KEY_NAME_1, null);

	}
}

# AXE 
import android.os.Bundle;
import android.widget.RadioGroup;
import android.widget.RadioButton;
import android.widget.TextView;
import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {
    RadioGroup radioGroup;
    TextView displayPet;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        radioGroup = findViewById(R.id.radioGroup);
        displayPet = findViewById(R.id.displayPet);

        radioGroup.setOnCheckedChangeListener(new RadioGroup.OnCheckedChangeListener() {
            @Override
            public void onCheckedChanged(RadioGroup group, int checkedId) {
                RadioButton …
<!-- activity_main.xml -->
<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="16dp">

    <RadioGroup
        android:id="@+id/radioGroup"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:orientation="vertical">
        <RadioButton
            android:id="@+id/radioBird"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Bird" />
        <RadioButton
            android:id="@+id/radioDog"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Dog" />
        <RadioButton
            android:id="@+id/radioCat"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Cat" />
        <RadioButton
            android:id="@+id/radioRabbit"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Rabbit" />
        <RadioButton
            android:id="@+id/radioPig"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Pig" />
    </RadioGroup>

    <TextView
        android:id="@+id/displayPet"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Selected Pet will be displayed here" />
</LinearLayout

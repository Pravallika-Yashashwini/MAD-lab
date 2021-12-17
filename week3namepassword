package com.example.myapplication111;
import androidx.appcompat.app.AppCompatActivity;
import android.content.Intent;
import android.os.Bundle;
import android.view.View;
import android.widget.AdapterView;
import android.widget.ArrayAdapter;
import android.widget.ListView;
import android.util.Pair;
import java.util.ArrayList;
import java.util.*;
import java.util.Map;
public class MainActivity extends AppCompatActivity {
 public static final String EXTRA_TEXT="com.example.myapplication111.EXTRA_TEXT";
 ListView l;
 String[] names={"Ram","Lakshman","Bharat"};
 Map<String,String> map=new HashMap<String,String>();
 @Override
 protected void onCreate(Bundle savedInstanceState) {
 super.onCreate(savedInstanceState);
 setContentView(R.layout.activity_main);
 map.put("Ram","Name:Ram\nFather Name:Abc\nMother Name:hyj\nph.no:1234567890\n");
 map.put("Lakshman","Name:Lakshman\nFather Name:Abc\nMother
Name:hyj\nph.no:1234567890\n");
 map.put("Bharat","Name:Bharat\nFather Name:Abc\nMother Name:hyj\nph.no:1234567890\n");
 l=findViewById(R.id.listview);
 ArrayAdapter<String> adapter=new ArrayAdapter<String>(this,
 android.R.layout.simple_list_item_activated_1,names);
 l.setAdapter(adapter);
 l.setOnItemClickListener(new AdapterView.OnItemClickListener() {
 @Override
 public void onItemClick(AdapterView<?> adapterView, View view, int i, long l) {
 int ind=i;
 activity(i,map);
 }
 });
 }
 public void activity(int i, Map<String, String> map){
 Intent intent=new Intent(this,MainActivity2.class);
 intent.putExtra(EXTRA_TEXT,map.get(names[i]));
 startActivity(intent);
 }
}
Xml 1 code:
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout
xmlns:android="http://schemas.android.com/apk/res/android"
 xmlns:app="http://schemas.android.com/apk/res-auto"
 xmlns:tools="http://schemas.android.com/tools"
 android:layout_width="match_parent"
 android:layout_height="match_parent"
 tools:context=".MainActivity">
 <ListView
 android:id="@+id/listview"
 android:layout_width="match_parent"
 android:layout_height="match_parent"/>
</androidx.constraintlayout.widget.ConstraintLayout>
Java 2 Code:
package com.example.myapplication111;
import androidx.appcompat.app.AppCompatActivity;
import android.content.Intent;
import android.os.Bundle;
import android.view.View;
import android.widget.TextView;
public class MainActivity2 extends AppCompatActivity {
 @Override
 protected void onCreate(Bundle savedInstanceState) {
 super.onCreate(savedInstanceState);
 setContentView(R.layout.activity_main2);
 Intent intent=getIntent();
 String text=intent.getStringExtra(MainActivity.EXTRA_TEXT);
 TextView t1=(TextView) findViewById(R.id.textView);
 t1.setText(text);
 } 
}
Xml 2 Code:
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout
xmlns:android="http://schemas.android.com/apk/res/android"
 xmlns:app="http://schemas.android.com/apk/res-auto"
 xmlns:tools="http://schemas.android.com/tools"
 android:layout_width="match_parent"
 android:layout_height="match_parent"
 tools:context=".MainActivity2">
 <TextView
 android:id="@+id/textView"
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 app:layout_constraintBottom_toBottomOf="parent"
 app:layout_constraintEnd_toEndOf="parent"
 app:layout_constraintHorizontal_bias="0.498"
 app:layout_constraintStart_toStartOf="parent"
 app:layout_constraintTop_toTopOf="parent"
 app:layout_constraintVertical_bias="0.092" />
</androidx.constraintlayout.widget.ConstraintLayout>

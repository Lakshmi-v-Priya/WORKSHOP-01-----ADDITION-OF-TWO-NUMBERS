## Workshop 1:  Create a application for addition of two numbers
Step 1: Create a New Android Studio Project
Open Android Studio
Select Empty Activity
Choose Java as the programming language

```
Done by : Lakshmi Priya V
Register Number : 212223220049
```

activity_main.xml
```

<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="20dp">


    <EditText
        android:id="@+id/etNum1"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter First Number"
        android:inputType="numberDecimal"/>


    <EditText
        android:id="@+id/etNum2"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter Second Number"
        android:inputType="numberDecimal"/>


    <Button
        android:id="@+id/btnAdd"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Add"/>


    <TextView
        android:id="@+id/tvResult"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Result"
        android:textSize="22sp"
        android:paddingTop="20dp"/>


</LinearLayout>
```

MainActivity.java

```

package com.example.additionapp;


import androidx.appcompat.app.AppCompatActivity;


import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;


public class MainActivity extends AppCompatActivity {


    EditText etNum1, etNum2;
    Button btnAdd;
    TextView tvResult;


    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);


        etNum1 = findViewById(R.id.etNum1);
        etNum2 = findViewById(R.id.etNum2);
        btnAdd = findViewById(R.id.btnAdd);
        tvResult = findViewById(R.id.tvResult);


        btnAdd.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {


                double num1 = Double.parseDouble(etNum1.getText().toString());
                double num2 = Double.parseDouble(etNum2.getText().toString());


                double sum = num1 + num2;


                tvResult.setText("Sum = " + sum);
            }
        });
    }
}
```

Output
Enter the first number.
Enter the second number.
Click the Add button.
The sum of the two numbers is displayed in the TextView.

Example:

First Number: 10
Second Number: 20
Output: Sum = 30.0
# OUTPUT :

<img width="593" height="793" alt="image" src="https://github.com/user-attachments/assets/ae3d66f4-0704-4866-96e8-feb810df1ccf" />

# RESULT : 
Thus , the program to execute the sum of the two numbers is displayed in the TextView us successfully implemented

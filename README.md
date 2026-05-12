# Ex.No:6 Create a simple application to request storage and camera permission at RunTime using android studio.

## AIM:

To develop a simple application for RunTime Permission in Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Min.required Giraffe)

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as runtimepermission and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Display process of runtimepermission in android mobile devices.

Step 7: Save and run the application.

## PROGRAM:
```
/*
Program to print the process of runtimepermission in android mobile devices”.
Developed by: VARSHA A
Registeration Number : 212223220121
*/
```
### ActivityMain.xml:
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.coordinatorlayout.widget.CoordinatorLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="?attr/colorSurface"
    tools:context=".MainActivity">

    <com.google.android.material.appbar.AppBarLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:background="@android:color/transparent"
        app:elevation="0dp">

        <com.google.android.material.appbar.MaterialToolbar
            android:id="@+id/toolbar"
            android:layout_width="match_parent"
            android:layout_height="?attr/actionBarSize"
            app:title="Permission Manager"
            app:titleCentered="true"
            app:titleTextAppearance="@style/TextAppearance.Material3.TitleLarge" />
    </com.google.android.material.appbar.AppBarLayout>

    <androidx.core.widget.NestedScrollView
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        app:layout_behavior="@string/appbar_scrolling_view_behavior">

        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:orientation="vertical"
            android:padding="24dp">

            <com.google.android.material.imageview.ShapeableImageView
                android:layout_width="120dp"
                android:layout_height="120dp"
                android:layout_gravity="center"
                android:layout_marginBottom="32dp"
                android:scaleType="centerInside"
                android:src="@android:drawable/ic_lock_idle_lock"
                app:tint="?attr/colorPrimary" />

            <TextView
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:text="Permissions Required"
                android:textAlignment="center"
                android:textAppearance="@style/TextAppearance.Material3.HeadlineMedium"
                android:textStyle="bold" />

            <TextView
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:layout_marginTop="8dp"
                android:layout_marginBottom="32dp"
                android:text="To provide the best experience, we need access to the following features:"
                android:textAlignment="center"
                android:textAppearance="@style/TextAppearance.Material3.BodyMedium"
                android:textColor="?attr/colorOnSurfaceVariant" />

            <!-- Camera Card -->
            <com.google.android.material.card.MaterialCardView
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:layout_marginBottom="16dp"
                app:cardCornerRadius="16dp"
                app:cardElevation="0dp"
                app:strokeColor="?attr/colorOutlineVariant"
                app:strokeWidth="1dp">

                <LinearLayout
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:gravity="center_vertical"
                    android:orientation="horizontal"
                    android:padding="16dp">

                    <ImageView
                        android:layout_width="40dp"
                        android:layout_height="40dp"
                        android:src="@android:drawable/ic_menu_camera"
                        app:tint="?attr/colorPrimary" />

                    <LinearLayout
                        android:layout_width="0dp"
                        android:layout_height="wrap_content"
                        android:layout_marginStart="16dp"
                        android:layout_weight="1"
                        android:orientation="vertical">

                        <TextView
                            android:layout_width="match_parent"
                            android:layout_height="wrap_content"
                            android:text="Camera"
                            android:textAppearance="@style/TextAppearance.Material3.TitleMedium" />

                        <TextView
                            android:layout_width="match_parent"
                            android:layout_height="wrap_content"
                            android:text="Used to take photos and videos."
                            android:textAppearance="@style/TextAppearance.Material3.BodySmall" />
                    </LinearLayout>
                </LinearLayout>
            </com.google.android.material.card.MaterialCardView>

            <!-- Storage Card -->
            <com.google.android.material.card.MaterialCardView
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:layout_marginBottom="32dp"
                app:cardCornerRadius="16dp"
                app:cardElevation="0dp"
                app:strokeColor="?attr/colorOutlineVariant"
                app:strokeWidth="1dp">

                <LinearLayout
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:gravity="center_vertical"
                    android:orientation="horizontal"
                    android:padding="16dp">

                    <ImageView
                        android:layout_width="40dp"
                        android:layout_height="40dp"
                        android:src="@android:drawable/ic_menu_save"
                        app:tint="?attr/colorPrimary" />

                    <LinearLayout
                        android:layout_width="0dp"
                        android:layout_height="wrap_content"
                        android:layout_marginStart="16dp"
                        android:layout_weight="1"
                        android:orientation="vertical">

                        <TextView
                            android:layout_width="match_parent"
                            android:layout_height="wrap_content"
                            android:text="Storage"
                            android:textAppearance="@style/TextAppearance.Material3.TitleMedium" />

                        <TextView
                            android:layout_width="match_parent"
                            android:layout_height="wrap_content"
                            android:text="Used to save and access your files."
                            android:textAppearance="@style/TextAppearance.Material3.BodySmall" />
                    </LinearLayout>
                </LinearLayout>
            </com.google.android.material.card.MaterialCardView>

            <com.google.android.material.button.MaterialButton
                android:id="@+id/btnRequestPermissions"
                style="@style/Widget.Material3.Button"
                android:layout_width="match_parent"
                android:layout_height="64dp"
                android:text="Allow Access"
                android:textAllCaps="false"
                android:textSize="18sp"
                app:cornerRadius="16dp" />

        </LinearLayout>
    </androidx.core.widget.NestedScrollView>

</androidx.coordinatorlayout.widget.CoordinatorLayout>
```
### MainActivity.java:
```
package com.example.runtimepermission;

import android.Manifest;
import android.content.pm.PackageManager;
import android.os.Build;
import android.os.Bundle;
import android.widget.Button;
import android.widget.Toast;

import androidx.activity.EdgeToEdge;
import androidx.activity.result.ActivityResultLauncher;
import androidx.activity.result.contract.ActivityResultContracts;
import androidx.appcompat.app.AppCompatActivity;
import androidx.core.content.ContextCompat;
import androidx.core.graphics.Insets;
import androidx.core.view.ViewCompat;
import androidx.core.view.WindowInsetsCompat;

import java.util.ArrayList;
import java.util.List;
import java.util.Map;

public class MainActivity extends AppCompatActivity {

    private ActivityResultLauncher<String[]> permissionLauncher;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        EdgeToEdge.enable(this);
        setContentView(R.layout.activity_main);
        ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main), (v, insets) -> {
            Insets systemBars = insets.getInsets(WindowInsetsCompat.Type.systemBars());
            v.setPadding(systemBars.left, systemBars.top, systemBars.right, systemBars.bottom);
            return insets;
        });

        // Initialize the permission launcher
        permissionLauncher = registerForActivityResult(
                new ActivityResultContracts.RequestMultiplePermissions(),
                result -> {
                    boolean allGranted = true;
                    for (Map.Entry<String, Boolean> entry : result.entrySet()) {
                        if (!entry.getValue()) {
                            allGranted = false;
                            break;
                        }
                    }
                    if (allGranted) {
                        Toast.makeText(this, "All permissions granted", Toast.LENGTH_SHORT).show();
                    } else {
                        Toast.makeText(this, "Some permissions were denied", Toast.LENGTH_SHORT).show();
                    }
                }
        );

        Button btnRequestPermissions = findViewById(R.id.btnRequestPermissions);
        btnRequestPermissions.setOnClickListener(v -> checkAndRequestPermissions());
    }

    private void checkAndRequestPermissions() {
        List<String> permissionsNeeded = getPermissionsNeeded();

        List<String> listPermissionsToRequest = new ArrayList<>();
        for (String perm : permissionsNeeded) {
            if (ContextCompat.checkSelfPermission(this, perm) != PackageManager.PERMISSION_GRANTED) {
                listPermissionsToRequest.add(perm);
            }
        }

        if (!listPermissionsToRequest.isEmpty()) {
            permissionLauncher.launch(listPermissionsToRequest.toArray(new String[0]));
        } else {
            Toast.makeText(this, "All permissions already granted", Toast.LENGTH_SHORT).show();
        }
    }

    private List<String> getPermissionsNeeded() {
        List<String> permissionsNeeded = new ArrayList<>();

        // Camera permission
        permissionsNeeded.add(Manifest.permission.CAMERA);

        // Storage permission logic based on Android version
        if (Build.VERSION.SDK_INT >= Build.VERSION_CODES.TIRAMISU) {
            // Android 13+ (API 33+) uses granular media permissions
            permissionsNeeded.add(Manifest.permission.READ_MEDIA_IMAGES);
        } else {
            // Android 12 and below
            permissionsNeeded.add(Manifest.permission.READ_EXTERNAL_STORAGE);
        }
        return permissionsNeeded;
    }
}
```


## OUTPUT
<img width="1920" height="1080" alt="pmd ex6" src="https://github.com/user-attachments/assets/0dba6ef8-c9f5-445f-bb7b-e11c042b855a" />
<img width="1920" height="1080" alt="pmd ex6 access" src="https://github.com/user-attachments/assets/4b2aacdb-17b6-4ac6-b01f-af596751517b" />
<img width="1920" height="1080" alt="pmd ex6 allow2" src="https://github.com/user-attachments/assets/7a35f065-116c-4bd2-82e0-ef55510ac502" />
<img width="1920" height="1080" alt="pmd ex6 allow" src="https://github.com/user-attachments/assets/570da457-ec67-4518-b2ee-e82dd7d66e8a" />
<img width="1920" height="1080" alt="pmd ex6 done" src="https://github.com/user-attachments/assets/fb4cd4b7-6190-4962-9c5b-5e1d508ad166" />



## RESULT
Thus a Simple Android Application to request storage and camera permission at RunTime in Android Studio is developed and executed successfully.

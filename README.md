# outlined-editTextBox
This is a frequently used editText material design.
first create the editText within TextInputLayout
<com.google.android.material.textfield.TextInputLayout
                android:id="@+id/routerLayout"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:layout_marginHorizontal="16dp"
                android:layout_marginTop="20dp"
                android:focusable="false"
                android:hint="@string/guest_name"
                android:theme="@style/TextInputLayoutStyle"
                app:boxBackgroundMode="outline"
                app:errorEnabled="true"
                app:errorTextColor="@color/vi_error"
                app:hintTextColor="@color/vi_input_field_text_color">

                <EditText
                    android:id="@+id/NameEditText"
                    android:layout_width="match_parent"
                    android:layout_height="50dp"
                    android:background="@null"
                    android:fontFamily="@font/poppins_medium"
                    android:inputType="textPersonName"
                    android:maxLength="8"
                    android:paddingHorizontal="10dp"
                    android:singleLine="true"
                    android:textColor="@color/vi_font_white" />
            </com.google.android.material.textfield.TextInputLayout>

important is to create a theme for textInputLayout
and editText Background should be null
here you can you TextInputEditText instead of EditText

below is the theme
<style name="TextInputLayoutStyle" parent="Widget.MaterialComponents.TextInputLayout.OutlinedBox.Dense">
        <item name="boxBackgroundMode">outline</item>

        <item name="boxStrokeColor">@color/vi_input_field_stroke_color</item>

        <item name="boxStrokeWidth">2dp</item>
        <item name="boxStrokeWidthFocused">2dp</item>

        <item name="boxCornerRadiusBottomEnd">10dp</item>
        <item name="boxCornerRadiusBottomStart">10dp</item>
        <item name="boxCornerRadiusTopEnd">10dp</item>
        <item name="boxCornerRadiusTopStart">10dp</item>


        <item name="android:textColorHint">@color/vi_input_field_text_color</item>

        <item name="boxStrokeErrorColor">@color/vi_error</item>
    </style>

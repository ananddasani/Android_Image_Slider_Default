# Android_Image_Slider_Default
Using Image Slider in theapp

# Code

#### activity_main.xml
```
        <ViewFlipper
        android:id="@+id/viewFlipper"
        android:layout_width="match_parent"
        android:layout_height="300dp"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.5"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />
```

#### 1st Activity 
```
ViewFlipper viewFlipper;

webView = findViewById(R.id.webView);

viewFlipper = findViewById(R.id.viewFlipper);

        //create an Image Array
        int[] imageArray = {R.drawable.kali_black, R.drawable.kali_blue, R.drawable.kali_red, R.drawable.kali_white, R.drawable.kali_futuristic};

        for (int i = 0; i < imageArray.length; i++)
            showImage(imageArray[i]);
            
    public void showImage(int image) {
        
        ImageView imageView = new ImageView(this);
        imageView.setBackgroundResource(image);

        viewFlipper.addView(imageView);
        viewFlipper.setFlipInterval(3000);
        viewFlipper.setAutoStart(true);

        viewFlipper.setInAnimation(this, android.R.anim.slide_in_left);
        viewFlipper.setOutAnimation(this, android.R.anim.slide_out_right);
    }
```

# App Highlight

<img src="app_images/Image Slider Code.png" /><br>

<img src="app_images/Image Slider App1.png" width="300" /> <img src="app_images/Image Slider App2.png" width="300" /> <img src="app_images/Image Slider App4.png" width="300" /> <br>

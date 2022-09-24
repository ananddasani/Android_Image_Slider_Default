# Android_Image_Slider_Default
Using Image Slider in theapp

This topic is a part of [My Complete Andorid Course](https://github.com/ananddasani/Android_Apps)

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

![Image Slider App1](https://user-images.githubusercontent.com/74413402/192095805-4e645d65-25cd-4c6e-abe7-6b4da3d2ef80.png)
![Image Slider App2](https://user-images.githubusercontent.com/74413402/192095808-c051adc1-d566-4cdf-9e0c-80f383882d48.png)
![Image Slider App4](https://user-images.githubusercontent.com/74413402/192095814-82473019-d168-4659-8cc4-986795dcd631.png)
![Image Slider Code](https://user-images.githubusercontent.com/74413402/192095817-e4aa4184-29d4-4847-827c-554bf2676e04.png)


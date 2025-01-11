<h1>Steps To Perform Jquery In Asp.Net:</h1>

<h2>Write A Script For Jquery:</h2>

```
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.7.1/jquery.min.js"></script>
```

<h2>Write HTML Code Which Contains Some Tags e.g.:</h2>

```
    <h1>Animation Using Jquery</h1>

    <!-- Example Elements -->
    <div class="box" id="box1">Box 1</div>
    <div class="box circle" id="box2">Circle</div>
    <p class="text" id="text1">Hello, this is animated text!</p>
    <button id="startAnimations">Start Animations</button>

```

<h2>After That Write JQuery:</h2>
<h3>Syntax: </h3>

```
   $(document).ready(function(){
         $("*").hide();
});
```

<h2>Example Of It:</h2>

```
   <script>
    $(document).ready(function () {
        $("#startAnimations").click(function () {
            // Animation 1: Fade In and Fade Out
            $("#box1").fadeOut(1000).fadeIn(1000);

            // Animation 2: Slide Up and Slide Down
            $("#box2").slideUp(1000).slideDown(1000);

            // Animation 3: Toggle Visibility
            $("#text1").toggle(1000);

            // Animation 4: Grow Height and Width
            $("#box1").animate({ width: "200px", height: "200px" }, 1000).animate({ width: "100px", height: "100px" }, 1000);

            // Animation 5: Change Background Color
            $("#box2").animate({ backgroundColor: "#8e44ad" }, 1000);

            // Animation 6: Rotate Element
            $("#box2").css({ transform: "rotate(0deg)" }).animate({ borderSpacing: 360 }, {
                step: function (now) {
                    $(this).css('transform', 'rotate(' + now + 'deg)');
                },
                duration: 2000
            });

            // Animation 7: Bounce Effect
            $("#box1").animate({ top: "-=50px" }, 300).animate({ top: "+=50px" }, 300);

            // Animation 8: Opacity Change
            $("#text1").animate({ opacity: 0.5 }, 1000).animate({ opacity: 1 }, 1000);

            // Animation 9: Move Element
            $("#box2").animate({ marginLeft: "200px" }, 1000).animate({ marginLeft: "0px" }, 1000);

            // Animation 10: Shake Effect
            for (let i = 0; i < 3; i++) {
                $("#box1").animate({ marginLeft: "-=20px" }, 100).animate({ marginLeft: "+=40px" }, 100).animate({ marginLeft: "-=20px" }, 100);
            }
        });
    });
</script>
```

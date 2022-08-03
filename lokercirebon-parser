<?php

    $xml = simplexml_load_file("https://lokercirebon.com/sitemap-pt-post-2022-08.xml") or die("Error: Cannot create object");
    
    $no = $no2 = $no3 = $no4 = $no5 = 1;

    echo "<p><b>Today</b></p>";

    foreach($xml as $xkey => $xval){
        $title_unparse  = str_replace("https://lokercirebon.com/", "", $xval->loc);
        $title_unparse2 = str_replace("-", " ", $title_unparse);
        $title_unparse3 = str_replace("/", "", $title_unparse2);
        $title          = ucwords($title_unparse3);

        $lastmod        = substr($xval->lastmod, 0, 10);

        if($lastmod == date("Y-m-d")){
            echo $no++ .". <a href='". $xval->loc ."'>". $title ." - ". $lastmod ."</a><br />";
        }
    }

    echo "<hr />";

    echo "<p><b>Yesterday</b></p>";

    foreach($xml as $xkey => $xval){
        $title_unparse  = str_replace("https://lokercirebon.com/", "", $xval->loc);
        $title_unparse2 = str_replace("-", " ", $title_unparse);
        $title_unparse3 = str_replace("/", "", $title_unparse2);
        $title          = ucwords($title_unparse3);

        $lastmod        = substr($xval->lastmod, 0, 10);

        if($lastmod == date("Y-m-d", strtotime("-1 day"))){
            echo $no2++ .". <a href='". $xval->loc ."'>". $title ." - ". $lastmod ."</a><br />";
        }
    }

    echo "<hr />";

    echo "<p><b>This Month</b></p>";

    foreach($xml as $xkey => $xval){
        $title_unparse  = str_replace("https://lokercirebon.com/", "", $xval->loc);
        $title_unparse2 = str_replace("-", " ", $title_unparse);
        $title_unparse3 = str_replace("/", "", $title_unparse2);
        $title          = ucwords($title_unparse3);

        $lastmod        = substr($xval->lastmod, 0, 7);

        if($lastmod == date("Y-m")){
            echo $no3++ .". <a href='". $xval->loc ."'>". $title ." - ". $lastmod ."</a><br />";
        }
    }

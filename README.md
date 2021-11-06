# ARSCTool
* Handy tool to convert from android resources.arsc to XML and build back to .arsc format
* Totaly independent of aapt and aapt2
* 100% java
* ## Dump
```console
java -jar arsctool.jar dump -i "/home/kikfox/test/resources.arsc" -o "/home/kikfox/test/out_xml"

I: 00.001 Dumping ... '/home/kikfox/test/resources.arsc'
I: 01.371 TABLE(0x0002){HeaderSize=12, ChunkSize=2802860}
I: 02.638 PACKAGE(0x0200){HeaderSize=288, ChunkSize=1795428} ID=0x7f{com.facebook.katana}
I: 02.816     SPEC(0x0202){HeaderSize=16, ChunkSize=944} anim[0x01, Entries=232]
I: 02.870     SPEC(0x0202){HeaderSize=16, ChunkSize=68} animator[0x02, Entries=13]
.
.
I: 07.829     SPEC(0x0202){HeaderSize=16, ChunkSize=92} style[0x14, Entries=19]
I: 07.835     SPEC(0x0202){HeaderSize=16, ChunkSize=156} xml[0x16, Entries=35]
I: 07.837     SPEC(0x0202){HeaderSize=16, ChunkSize=1756} dimen2[0x17, Entries=435]
I: 07.975     SPEC(0x0202){HeaderSize=16, ChunkSize=1208} drawable4[0x1a, Entries=298]
I: 07.988     SPEC(0x0202){HeaderSize=16, ChunkSize=21396} drawable5[0x1b, Entries=5345]
I: 08.313     SPEC(0x0202){HeaderSize=16, ChunkSize=15180} layout2[0x1c, Entries=3791]
I: 08.528     SPEC(0x0202){HeaderSize=16, ChunkSize=340} raw2[0x1d, Entries=81]
I: 08.532     SPEC(0x0202){HeaderSize=16, ChunkSize=10504} style2[0x1e, Entries=2622]
I: 08.859 Dumped to '/home/kikfox/test/out_xml'

```
* ## Dumped xml sample
```console

           <!--0x7f1e0361:@style2/(name removed)-->
           <entry flags="1" reference="8260" index="865">
              <bag index="0" parent="0x7f1e0360" count="1">
                <item index="0" id="0x01010098" type="REFERENCE" data="0x7f06013a"/>
              </bag>
           </entry>

```
* ## Build
```console
java -jar arsctool.jar build -i "/home/kikfox/test/out_xml" -o "/home/kikfox/test/out_arsc/resources.arsc"

I: 00.002 Building from xml files ... '/home/kikfox/test/out_xml'
I: 01.990     SPEC(0x0202){HeaderSize=16, ChunkSize=944} anim[0x01, Entries=232]
I: 02.681     SPEC(0x0202){HeaderSize=16, ChunkSize=41768} id[0x0b, Entries=10438]
I: 04.749     SPEC(0x0202){HeaderSize=16, ChunkSize=92} style[0x14, Entries=19]
I: 04.752     SPEC(0x0202){HeaderSize=16, ChunkSize=156} xml[0x16, Entries=35]
I: 04.764     SPEC(0x0202){HeaderSize=16, ChunkSize=1756} dimen2[0x17, Entries=435]
I: 04.820     SPEC(0x0202){HeaderSize=16, ChunkSize=10288} drawable2[0x18, Entries=2568]
I: 04.861     SPEC(0x0202){HeaderSize=16, ChunkSize=348} drawable3[0x19, Entries=83]
.
.
I: 04.869     SPEC(0x0202){HeaderSize=16, ChunkSize=1208} drawable4[0x1a, Entries=298]
I: 05.059     SPEC(0x0202){HeaderSize=16, ChunkSize=21396} drawable5[0x1b, Entries=5345]
I: 05.682     SPEC(0x0202){HeaderSize=16, ChunkSize=180} array[0x03, Entries=41]
I: 06.244     SPEC(0x0202){HeaderSize=16, ChunkSize=5920} color[0x06, Entries=1476]
I: 06.292     SPEC(0x0202){HeaderSize=16, ChunkSize=544} dimen[0x07, Entries=132]
I: 06.314     SPEC(0x0202){HeaderSize=16, ChunkSize=464} drawable[0x08, Entries=112]
I: 06.541 PACKAGE(0x0200){HeaderSize=288, ChunkSize=1795428} ID=0x7f{com.facebook.katana}
I: 06.804 TABLE(0x0002){HeaderSize=12, ChunkSize=2802860}
I: 07.826 Built to '/home/kikfox/test/out_arsc/resources.arsc'

```


## Download
    
### [Jar file](https://github.com/kikfox/ARSCTool/releases/latest)
    
    
## Source code 
* Will be realeased soon 

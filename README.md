# Schwibbogen aus der Zukunft
## ~avatar avatar @unplugged
In der Botschaft vom Nordpol hat der Weihnachtsmann um deine Hilfe gebeten. Doch bevor du dich auf den Weg machst, solltest du sicherstellen, dass du auch wieder zurück nach Hause findest. <br>
Schon früh nutzte man im Erzgebirge Schwibbögen. Mit diesen individuell verzierten Lichterbögen an den Fenstern war es den Arbeitern im Bergwerk auch nach einem langen Arbeitstag, wenn es schon dunkel war, möglich, zuverlässig dank der Beleuchtung ihr Zuhause zu finden. <br>
![SchwibbogenRot](https://github.com/r00b1nh00d/futurschwibbogen/blob/master/SchwibbogenRot.jpg?raw=true)

## ~ @unplugged 
So ein Schwibbogen wird klassisch aus Holz gefertigt. Natürlich kannst du aber auch erstmal einen Prototyp aus Pappe herstellen. Um besonders große Kreise auf die Pappe oder das Holz zu zeichnen, kannst du einen Stift an eine Schnur binden. Das eine Ender der Schnur hältst du mit der Hand fest (vielleicht kann dir hier jemand helfen, um den Mittelpunkt fest an einer Stelle zu halten). Dieses Ende ergibt den Kreismittelpunkt. Mit dem Stift kannst du jetzt einen großen Kreisbogen zeichnen (für einen kleinen Schwibbogen kann auch ein großer Topfdeckel als Schablone dienen). Du benötigst zwei etwas breitere Bögen, welche später von außen zu sehen sind. Der Innere sollte etwas schmaler sein, sodass die LED's später hinter den Äußeren versteckt sind. Die Dicke des inneren Bogens sollte ca. 1cm betragen, was der Breite des LED-Streifens entspricht.

## ~ @unplugged
Sobald alle Teile ausgesägt bzw. zurecht geschnitten sind, klebst du zuerst den LED-Streifen auf die Unterseite des inneren Bogens. Anschließend kannst du die äußeren Bögen bündig ankleben. Damit dein Holzleim oder Alleskleber seine Wirkung entfalten kann, lass ihn am besten über Nacht oder mindestens ein paar Stunden austrocknen (am besten du beschwerst den Bogen, damit die einzelnen Teile aufeinander gedrückt werden).

##  ~ @unplugged 
**Programmierung**
Bei der Programmierung stehen dir nun alle Türen offen.<br>
Wenn du dich an die Alarmanlage für die Keksdose erinnerst, könntest du Teile des Programms nutzen, um deinen Schwibbogen automatisch anzuschalten, sobald es draußen dunkel wird. <br>
Du kannst ihn auch wie das Party-Licht in Abhängigkeit zur Musik flackern lassen oder dir eine eigene Animation programmieren.  Diese könnte später so aussehen, als würden Sternschnuppen am Bogen entlang huschen. <br>
![Schwibbogen](https://github.com/r00b1nh00d/futurschwibbogen/blob/master/Schwibbogen.jpg?raw=true)

## Beispiel
Falls du erstmal testen möchtest, ob deine Konstruktion funktioniert, bevor du selbst programmierst, kannst du dieses Beispiel nachbauen und testen. 
```blocks
let Pixel = 0
let strip = neopixel.create(DigitalPin.P1, 36, NeoPixelMode.RGB)
strip.showColor(basic.rgbw(
100,
255,
255,
0
))
strip.show()
basic.forever(function () {
    if (Pixel < 35) {
        strip.setPixelColor(Pixel, neopixel.colors(NeoPixelColors.Red))
        strip.setPixelColor(Pixel + 1, neopixel.colors(NeoPixelColors.Red))
        strip.setPixelColor(Pixel + 2, neopixel.colors(NeoPixelColors.Red))
        strip.setPixelColor(Pixel + 3, neopixel.colors(NeoPixelColors.Red))
        strip.setPixelColor(Pixel + 4, neopixel.colors(NeoPixelColors.Red))
        strip.setPixelColor(Pixel + 5, neopixel.colors(NeoPixelColors.Red))
        strip.setPixelColor(Pixel + -1, basic.rgbw(
        100,
        255,
        255,
        0
        ))
        strip.show()
        basic.pause(10)
        Pixel += 1
    } else {
        Pixel = 0
    }
})
```

---
description: Una figura chiusa, ad esempio un rettangolo o un'ellisse, è costituita da una struttura e da una parte interna.
ms.assetid: 889558d5-9181-43ff-b862-e92966324208
title: Pennelli e forme piene
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eb772be88ce26325337fd9c88fc0319631895e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104570850"
---
# <a name="brushes-and-filled-shapes"></a>Pennelli e forme piene

Una figura chiusa, ad esempio un rettangolo o un'ellisse, è costituita da una struttura e da una parte interna. Il contorno viene disegnato con un oggetto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) e l'interno viene riempito con un oggetto [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) . In Windows GDI+ sono disponibili diverse classi di pennelli per riempire le parti interne delle figure chiuse, ovvero [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), [**HatchBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush), [**TextureBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush), [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush)e [**PathGradientBrush**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush). Tutte queste classi ereditano dalla classe **Brush** . Nella figura seguente viene illustrato un rettangolo riempito con un pennello a tinta unita e un'ellisse riempita con un pennello di tratteggio.

![illustrazione che mostra un rettangolo blu e un'ellisse magenta riempita con un modello di tratteggio blu](images/aboutgdip02-art17.png)

 

-   [Pennelli a tinta unita](#solid-brushes)
-   [Pennelli tratteggiati](#hatch-brushes)
-   [Pennelli trama](#texture-brushes)
-   [Pennelli sfumatura](#gradient-brushes)

## <a name="solid-brushes"></a>Pennelli a tinta unita

Per riempire una forma chiusa sono necessari un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e un oggetto [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) . L'oggetto **Graphics** fornisce metodi, ad esempio [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inconstrectf_)) e [FillEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inconstrectf_)), e l'oggetto **Brush** archivia gli attributi del riempimento, ad esempio il colore e il motivo. L'indirizzo dell'oggetto **pennello** viene passato come uno degli argomenti del metodo Fill. Nell'esempio seguente viene riempita un'ellisse con un colore rosso a tinta unita.


```
SolidBrush mySolidBrush(Color(255, 255, 0, 0));
myGraphics.FillEllipse(&mySolidBrush, 0, 0, 60, 40);
```



Si noti che nell'esempio precedente il pennello è di tipo [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), che eredita da [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush).

## <a name="hatch-brushes"></a>Pennelli tratteggiati

Quando si riempie una forma con un pennello tratteggiato, è necessario specificare un colore di primo piano, un colore di sfondo e uno stile di tratteggio. Il colore di primo piano è il colore del tratteggio.


```
HatchBrush myHatchBrush(
   HatchStyleVertical, 
   Color(255, 0, 0, 255),
   Color(255, 0, 255, 0));
```



GDI+ fornisce più di 50 stili di tratteggio, specificati in [**HatchStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-hatchstyle). I tre stili illustrati nella figura seguente sono Horizontal, ForwardDiagonal e Cross.

![illustrazione che mostra tre ellissi colorate, ognuna con uno stile di tratteggio diverso](images/aboutgdip02-art18.png)

 

## <a name="texture-brushes"></a>Pennelli trama

Con un pennello trama è possibile riempire una forma con un modello archiviato in una bitmap. Si supponga, ad esempio, che l'immagine seguente venga archiviata in un file su disco denominato MyTexture.bmp.

![Screenshot di un piccolo quadrato riempito con vari colori](images/aboutgdip02-art19.png)

Nell'esempio seguente viene riempita un'ellisse ripetendo l'immagine archiviata in MyTexture.bmp.


```
Image myImage(L"MyTexture.bmp");
TextureBrush myTextureBrush(&myImage);
myGraphics.FillEllipse(&myTextureBrush, 0, 0, 100, 50);
```



Nell'illustrazione seguente viene mostrata l'ellisse piena.

![illustrazione che mostra un'ellisse riempita con il modello definito in precedenza](images/aboutgdip02-art20.png)

 

## <a name="gradient-brushes"></a>Pennelli sfumatura

È possibile utilizzare un pennello sfumatura per riempire una forma con un colore che cambia gradualmente da una parte della forma a un'altra. Un pennello sfumato orizzontale, ad esempio, cambierà colore mentre si sposta dal lato sinistro di una figura a destra. Nell'esempio seguente viene riempita un'ellisse con un pennello sfumato orizzontale che passa da blu a verde mentre si sposta dal lato sinistro dell'ellisse al lato destro.


```
LinearGradientBrush myLinearGradientBrush(
   myRect,
   Color(255, 0, 0, 255),
   Color(255, 0, 255, 0),
   LinearGradientModeHorizontal);
myGraphics.FillEllipse(&myLinearGradientBrush, myRect); 
```



Nell'illustrazione seguente viene mostrata l'ellisse piena.

![illustrazione che mostra un'ellisse con un riempimento sfumato: blu a destra verso il verde a sinistra](images/aboutgdip02-art21.png)

Un pennello sfumatura percorso può essere configurato per modificare il colore mentre si sposta dal centro di una figura verso il limite.

![illustrazione di un'ellisse con blu scuro al centro, ombreggiatura a blu chiaro sul bordo](images/aboutgdip02-art22.png)

I pennelli sfumatura del percorso sono piuttosto flessibili. Il pennello sfumatura utilizzato per riempire il triangolo nell'illustrazione seguente passa gradualmente da rosso al centro a ognuno dei tre colori diversi nei vertici.

![illustrazione di un triangolo rosso al centro, ombreggiatura a un colore diverso in ogni vertice](images/aboutgdip02-art23.png)

 

 




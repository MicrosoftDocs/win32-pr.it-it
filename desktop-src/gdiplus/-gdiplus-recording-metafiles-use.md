---
description: La classe Metafile, che eredita dalla classe Image, consente di registrare una sequenza di comandi di disegno.
ms.assetid: 062de6c2-9f82-415d-860e-2d1afd2ac027
title: Registrazione di metafile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 047cdce842a9b44096ebd0f866e1b1551a5f951e138557062dff5e8f8d54f3ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014781"
---
# <a name="recording-metafiles"></a>Registrazione di metafile

La [**classe Metafile,**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) che eredita dalla [**classe Image,**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) consente di registrare una sequenza di comandi di disegno. I comandi registrati possono essere archiviati in memoria, salvati in un file o salvati in un flusso. I metafile possono contenere grafica vettoriale, immagini raster e testo.

Nell'esempio seguente viene creato [**un oggetto Metafile.**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) Il codice usa **l'oggetto Metafile** per registrare una sequenza di comandi grafici e quindi salva i comandi registrati in un file denominato SampleMetafile.emf. Si noti che **il costruttore metafile** riceve un handle del contesto di dispositivo e il [**costruttore Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) riceve l'indirizzo dell'oggetto **Metafile.** La registrazione si interrompe (e i comandi registrati vengono salvati nel file) quando **l'oggetto Graphics** esce dall'ambito. Le ultime due righe di codice visualizzano il metafile creando un nuovo oggetto **Graphics** e passando l'indirizzo dell'oggetto **Metafile** al **metodo DrawImage** di tale **oggetto Graphics.** Si noti che il codice usa lo stesso **oggetto Metafile** per registrare e visualizzare (riprodurre) il metafile.


```
Metafile metafile(L"SampleMetafile.emf", hdc); 
{
   Graphics graphics(&metafile);
   Pen greenPen(Color(255, 0, 255, 0));
   SolidBrush solidBrush(Color(255, 0, 0, 255));

   // Add a rectangle and an ellipse to the metafile.
   graphics.DrawRectangle(&greenPen, Rect(50, 10, 25, 75));
   graphics.DrawEllipse(&greenPen, Rect(100, 10, 25, 75));

   // Add an ellipse (drawn with antialiasing) to the metafile.
   graphics.SetSmoothingMode(SmoothingModeHighQuality);
   graphics.DrawEllipse(&greenPen, Rect(150, 10, 25, 75));

   // Add some text (drawn with antialiasing) to the metafile.
   FontFamily fontFamily(L"Arial");
   Font font(&fontFamily, 24, FontStyleRegular, UnitPixel);
   
   graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);
   graphics.RotateTransform(30.0f);
   graphics.DrawString(L"Smooth Text", 11, &font, 
      PointF(50.0f, 50.0f), &solidBrush);
} // End of recording metafile.

// Play back the metafile.
Graphics playbackGraphics(hdc);
playbackGraphics.DrawImage(&metafile, 200, 100);
```



> [!Note]  
> Per registrare un metafile, è necessario costruire un [**oggetto Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) basato su un [**oggetto Metafile.**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) La registrazione del metafile termina quando **l'oggetto Graphics** viene eliminato o esce dall'ambito.

 

Un metafile contiene il proprio stato grafico, definito [**dall'oggetto Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) usato per registrare il metafile. Tutte le proprietà dell'oggetto **Graphics** (area di ritaglio, trasformazione globale, modalità smoothing e simili) impostate durante la registrazione del metafile verranno archiviate nel metafile. Quando si visualizza il metafile, il disegno verrà eseguito in base alle proprietà archiviate.

Nell'esempio seguente si supponga che la modalità smoothing sia stata impostata su SmoothingModeNormal durante la registrazione del metafile. Anche se la modalità smoothing dell'oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) usato per la riproduzione è impostata su SmoothingModeHighQuality, il metafile verrà riprodotto in base all'impostazione SmoothingModeNormal. È importante impostare la modalità di smussamento durante la registrazione, non la modalità di smoothing impostata prima della riproduzione.


```
graphics.SetSmoothingMode(SmoothingModeHighQuality);
graphics.DrawImage(&meta, 0, 0);
```



 

 




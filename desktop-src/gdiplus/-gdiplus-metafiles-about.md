---
description: Windows GDI+ fornisce la classe Metafile che consente di registrare e visualizzare i metafile.
ms.assetid: a9f9bac4-f3c7-44a1-9f0f-59ff1a27b077
title: Metafile (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae75c2185670563f9a9e624d868da5b0e299cbec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343406"
---
# <a name="metafiles-gdi"></a>Metafile (GDI+)

Windows GDI+ fornisce la classe [**metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) che consente di registrare e visualizzare i metafile. Un metafile, detto anche immagine vettoriale, è un'immagine archiviata come sequenza di comandi e impostazioni di disegno. I comandi e le impostazioni registrati in un oggetto **metafile** possono essere archiviati in memoria o salvati in un file o in un flusso.

GDI+ consente di visualizzare i metafile archiviati nei formati seguenti:

-   Windows Metafile Format (WMF)
-   Enhanced Metafile (EMF)
-   EMF +

GDI+ può registrare i metafile nei formati EMF e EMF +, ma non nel formato WMF.

EMF + è un'estensione di EMF che consente l'archiviazione di record GDI+. Sono disponibili due varianti nel formato EMF +, ovvero EMF + Only e EMF + Dual. EMF + solo i metafile contengono solo record GDI+. Tali metafile possono essere visualizzati da GDI+ ma non da Windows Graphics Device Interface (GDI). I metafile EMF + Dual contengono i record GDI+ e GDI. Ogni record GDI+ in un metafile EMF + Dual è associato a un record GDI alternativo. Tali metafile possono essere visualizzati da GDI+ o da GDI.

Nell'esempio seguente vengono registrate un'impostazione e un comando Drawing in un file su disco. Si noti che nell'esempio viene creato un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e che il costruttore per l'oggetto **Graphics** riceve l'indirizzo di un oggetto [**metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) come argomento.


```
myMetafile = new Metafile(L"MyDiskFile.emf", hdc);
myGraphics = new Graphics(myMetafile);
   myPen = new Pen(Color(255, 0, 0, 200));
   myGraphics->SetSmoothingMode(SmoothingModeAntiAlias);
   myGraphics->DrawLine(myPen, 0, 0, 60, 40);
delete myGraphics;
delete myPen;
delete myMetafile;
```



Come illustrato nell'esempio precedente, la classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) è la chiave per la registrazione di istruzioni e impostazioni in un oggetto [**metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) . Qualsiasi chiamata eseguita a un metodo di un oggetto **Graphics** può essere registrata in un oggetto **metafile** . Analogamente, è possibile impostare qualsiasi proprietà di un oggetto **Graphics** e registrare tale impostazione in un oggetto **metafile** . La registrazione termina quando l'oggetto **Graphics** viene eliminato o esce dall'ambito.

Nell'esempio seguente viene visualizzato il metafile creato nell'esempio precedente. Il metafile viene visualizzato con l'angolo superiore sinistro in (100, 100).


```
Graphics myGraphics(hdc);
Image myImage(L"MyDiskFile.emf");
myGraphics.DrawImage(&myImage, 100, 100);
```



Nell'esempio seguente vengono registrate diverse impostazioni delle proprietà (area di ritaglio, trasformazione globale e modalità di smussatura) in un oggetto [**metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) . Il codice registra quindi diverse istruzioni di disegno. Le istruzioni e le impostazioni vengono salvate in un file su disco.


```
myMetafile = new Metafile(L"MyDiskFile2.emf", hdc); 
myGraphics = new Graphics(myMetafile);
   myGraphics->SetSmoothingMode(SmoothingModeAntiAlias);
   myGraphics->RotateTransform(30);

   // Create an elliptical clipping region.
   GraphicsPath myPath;
   myPath.AddEllipse(0, 0, 200, 100);
   Region myRegion(&myPath);
   myGraphics->SetClip(&myRegion);

   Pen myPen(Color(255, 0, 0, 255));
   myGraphics->DrawPath(&myPen, &myPath);

   for(INT j = 0; j <= 300; j += 10)
   {
      myGraphics->DrawLine(&myPen, 0, 0, 300 - j, j);
   }
delete myGraphics;
delete myMetafile;
```



Nell'esempio seguente viene visualizzata l'immagine del metafile creata nell'esempio precedente.


```
myGraphics = new Graphics(hdc);
myMetafile = new Metafile(L"MyDiskFile.emf");
myGraphics->DrawImage(myMetafile, 10, 10);
```



Nella figura seguente viene illustrato l'output del codice precedente. Si noti l'anti-aliasing, l'area di ritaglio ellittica e la rotazione di 30 gradi.

![Screenshot di una finestra che contiene un'ellisse riempita con righe che hanno origine in un punto esterno all'ellisse](images/aboutgdip05-art00.png)

 

 




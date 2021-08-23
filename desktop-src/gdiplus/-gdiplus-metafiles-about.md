---
description: Windows GDI+ fornisce la classe Metafile in modo da poter registrare e visualizzare i metafile.
ms.assetid: a9f9bac4-f3c7-44a1-9f0f-59ff1a27b077
title: Metafile (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 190d03edd8857da3e840c2b3fde04314fa1fb1ddb01c8e69c684bccecf3e708d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778681"
---
# <a name="metafiles-gdi"></a>Metafile (GDI+)

Windows GDI+ fornisce la [**classe Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) in modo da poter registrare e visualizzare i metafile. Un metafile, detto anche immagine vettoriale, è un'immagine archiviata come sequenza di comandi e impostazioni di disegno. I comandi e le impostazioni registrati in un **oggetto Metafile** possono essere archiviati in memoria o salvati in un file o in un flusso.

GDI+ visualizzare i metafile archiviati nei formati seguenti:

-   Windows Formato metafile (WMF)
-   Enhanced Metafile (EMF)
-   EMF+

GDI+ possibile registrare metafile nei formati EMF ed EMF+, ma non nel formato WMF.

EMF+ è un'estensione di EMF che consente GDI+ record da archiviare. Nel formato EMF+ sono disponibili due varianti: Solo EMF+ ed EMF+ Dual. Solo i metafile EMF+ contengono solo GDI+ record. Questi metafile possono essere visualizzati da GDI+ ma non da Windows Graphics Device Interface (GDI). I metafile duali EMF+ contengono GDI+ e GDI. Ogni GDI+ record in un metafile duale EMF+ è associato a un record GDI alternativo. Questi metafile possono essere visualizzati da GDI+ o da GDI.

L'esempio seguente registra un'impostazione e un comando di disegno in un file su disco. Si noti che l'esempio crea un [**oggetto Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e che il costruttore per l'oggetto **Graphics** riceve l'indirizzo di un oggetto [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) come argomento.


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



Come illustrato nell'esempio precedente, la [**classe Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) è la chiave per registrare istruzioni e impostazioni in un [**oggetto Metafile.**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) Qualsiasi chiamata effettuata a un metodo di un **oggetto Graphics** può essere registrata in un **oggetto Metafile.** Analogamente, è possibile impostare qualsiasi proprietà di un **oggetto Graphics** e registrare tale impostazione in un **oggetto Metafile.** La registrazione termina quando **l'oggetto Graphics** viene eliminato o esce dall'ambito.

Nell'esempio seguente viene visualizzato il metafile creato nell'esempio precedente. Il metafile viene visualizzato con l'angolo superiore sinistro in corrispondenza di (100, 100).


```
Graphics myGraphics(hdc);
Image myImage(L"MyDiskFile.emf");
myGraphics.DrawImage(&myImage, 100, 100);
```



L'esempio seguente registra diverse impostazioni delle proprietà (area di ritaglio, trasformazione globale e modalità smoothing) in un [**oggetto Metafile.**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) Il codice registra quindi diverse istruzioni di disegno. Le istruzioni e le impostazioni vengono salvate in un file su disco.


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



Nella figura seguente viene illustrato l'output del codice precedente. Si noti l'antialiasing, l'area di ritaglio ellittica e la rotazione di 30 gradi.

![Screenshot di una finestra contenente un'ellisse riempita con linee che hanno origine in un punto all'esterno dell'ellisse](images/aboutgdip05-art00.png)

 

 




---
description: L'interfaccia C++ Windows GDI+ contiene circa 40 classi, 50 enumerazioni e 6 strutture. Esistono anche alcune funzioni che non sono membri di alcuna classe.
ms.assetid: 46051bfa-b842-4e4e-bda8-e9003b5b5da4
title: Struttura dell'interfaccia basata su classi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30909917ad89a65e88c4ca31ca229a5f25d503bced7a9cac81e4199ced1ba7d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830661"
---
# <a name="the-structure-of-the-class-based-interface"></a>Struttura dell'interfaccia basata su classi

L'interfaccia C++ Windows GDI+ contiene circa 40 classi, 50 enumerazioni e 6 strutture. Esistono anche alcune funzioni che non sono membri di alcuna classe.

È necessario indicare che lo spazio dei nomi Gdiplus viene usato prima GDI+ chiamate a qualsiasi funzione. L'istruzione seguente indica che lo spazio dei nomi Gdiplus viene usato nell'applicazione.

`using namespace Gdiplus;`

La [**classe Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) è il nucleo dell'GDI+ grafica; è la classe che disegna effettivamente linee, curve, figure, immagini e testo.

Molte classi funzionano insieme alla [**classe Graphics.**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Ad esempio, il [metodo Graphics::D rawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) riceve un puntatore a un oggetto [**Pen,**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) che contiene gli attributi (colore, larghezza, stile del trattino e simili) della linea da disegnare. Il [metodo Graphics::FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inconstrectf_)) può ricevere un puntatore a un oggetto [**LinearGradientBrush,**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) che funziona con l'oggetto **Graphics** per riempire un rettangolo con un colore che cambia gradualmente. [**Gli**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) oggetti [**Font e StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) influiscono sul modo in cui un **oggetto Graphics** disegna testo. Un [**oggetto Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) archivia e modifica la trasformazione globale di un oggetto **Graphics,** usato per ruotare, ridimensionare e capovolgere le immagini.

Alcune classi fungono principalmente da tipi di dati strutturati. Alcune di queste classi (ad [**esempio, Rect,**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point)e [**Size)**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-size)sono per scopi generali. Altri sono per scopi specializzati e sono considerati classi helper. Ad esempio, la [**classe BitmapData**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-bitmapdata) è un helper per la [**classe Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) e la [**classe PathData**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pathdata) è un helper per la classe [**GraphicsPath.**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) GDI+ definisce anche alcune strutture usate per organizzare i dati. Ad esempio, la [**struttura ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) contiene una coppia di oggetti [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) che formano una voce in una tabella di conversione dei colori.

GDI+ definisce diverse enumerazioni, ovvero raccolte di costanti correlate. Ad esempio, l'enumerazione [**LineJoin**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-linejoin) contiene gli elementi [****LineJoinBevel****](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-linejoin), [****LineJoinMiter***](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-linejoin)e [****LineJoinRound****](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-linejoin), che specificano gli stili che possono essere usati per unire due righe.

GDI+ fornisce alcune funzioni che non fanno parte di alcuna classe. Due di queste funzioni sono [**GdiplusStartup**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) e [**GdiplusShutdown.**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown) È necessario chiamare **GdiplusStartup** prima di effettuare qualsiasi altra chiamata GDI+ ed è necessario chiamare **GdiplusShutdown** dopo aver terminato di usare GDI+.

 

 

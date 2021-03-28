---
description: L'interfaccia C++ per Windows GDI+ contiene circa 40 classi, enumerazioni 50 e 6 strutture. Sono inoltre disponibili alcune funzioni che non sono membri di alcuna classe.
ms.assetid: 46051bfa-b842-4e4e-bda8-e9003b5b5da4
title: Struttura dell'interfaccia basata su classi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2627d695330c316a57c2593e75233d73b27a1524
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993741"
---
# <a name="the-structure-of-the-class-based-interface"></a>Struttura dell'interfaccia basata su classi

L'interfaccia C++ per Windows GDI+ contiene circa 40 classi, enumerazioni 50 e 6 strutture. Sono inoltre disponibili alcune funzioni che non sono membri di alcuna classe.

È necessario indicare che lo spazio dei nomi Gdiplus viene utilizzato prima della chiamata di qualsiasi funzione GDI+. L'istruzione seguente indica che è in uso lo spazio dei nomi Gdiplus nell'applicazione.

`using namespace Gdiplus;`

La classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) è il nucleo dell'interfaccia GDI+; si tratta della classe che disegna effettivamente linee, curve, figure, immagini e testo.

Molte classi interagiscono con la classe [**grafica**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Ad esempio, il metodo [Graphics::D rawline](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) riceve un puntatore a un oggetto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) , che include gli attributi (colore, larghezza, stile del trattino e like) della linea da disegnare. Il metodo [Graphics:: FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inconstrectf_)) può ricevere un puntatore a un oggetto [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) , che funziona con l'oggetto **Graphics** per riempire un rettangolo con un colore a modifica graduale. Gli oggetti [**font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) e [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) influenzano il modo in cui un oggetto **Graphics** disegna il testo. Un oggetto [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) archivia e modifica la trasformazione globale di un oggetto **Graphics** , che viene usato per ruotare, ridimensionare e capovolgere le immagini.

Alcune classi servono principalmente come tipi di dati strutturati. Alcune di queste classi (ad esempio, [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect), [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point)e [**size**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-size)) sono destinate a scopi generali. Altri sono destinati a scopi specializzati e sono considerati classi helper. Ad esempio, la classe [**BitmapData**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-bitmapdata) è un helper per la classe [**bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) e la classe [**PathData**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pathdata) è un helper per la classe [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) . In GDI+ sono inoltre definite alcune strutture utilizzate per organizzare i dati. Ad esempio, la struttura [**mappa**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) colori include una coppia di oggetti [**colore**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) che formano una voce in una tabella di conversione dei colori.

GDI+ definisce diverse enumerazioni, ovvero raccolte di costanti correlate. L'enumerazione [**LineJoin**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-linejoin) , ad esempio, contiene gli elementi [* * * * LineJoinBevel * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-linejoin)* *, * * * * [LineJoinMiter * * * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-linejoin)e [* * * * LineJoinRound * * * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-linejoin), che specificano gli stili che possono essere utilizzati per unire in join due righe.

GDI+ fornisce alcune funzioni che non fanno parte di alcuna classe. Due di queste funzioni sono [**GdiplusStartup**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) e [**GdiplusShutdown**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown). È necessario chiamare **GdiplusStartup** prima di eseguire qualsiasi altra chiamata a GDI+ ed è necessario chiamare **GdiplusShutdown** al termine dell'utilizzo di GDI+.

 

 

---
description: Una bitmap è uno degli oggetti GDI che è possibile selezionare in un contesto di dispositivo (DC).
ms.assetid: 36afaabc-1334-42d1-8004-7952ce3c119e
title: Informazioni sulle bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53dbba516734dc255ce33005a7a9073865765785
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527708"
---
# <a name="about-bitmaps"></a>Informazioni sulle bitmap

Una bitmap è uno degli oggetti GDI che è possibile selezionare in un *contesto di dispositivo* (DC). I [contesti di dispositivo](device-contexts.md) sono strutture che definiscono un set di oggetti grafici e i relativi attributi associati, nonché le modalità grafiche che interessano l'output. La tabella seguente descrive gli oggetti GDI che è possibile selezionare in un contesto di dispositivo.



| Oggetto grafico                         | Descrizione                                                                                                                                                                                          |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bitmap](bitmaps.md)                 | Consente di creare, modificare (ridimensionare, scorrere, ruotare e disegnare) e di archiviare le immagini come file su un disco.                                                                                                       |
| [Pennelli](brushes.md)                 | Disegna l'interno di poligoni, ellissi e percorsi.                                                                                                                                                |
| [Tipi di carattere](fonts-and-text.md)            | Disegna il testo su schermi video e altri dispositivi di output.                                                                                                                                               |
| [Tavolozza logica](logical-palette.md) | Tavolozza dei colori creato da un'applicazione e associato a un contesto di dispositivo specificato.                                                                                                                |
| [Percorsi](paths.md)                     | Una o più figure, o forme, compilate e/o delineate.                                                                                                                                     |
| [Penne](pens.md)                       | Strumento grafico utilizzato da un'applicazione per creare linee e curve.                                                                                                                                   |
| [Aree](regions.md)                 | Un rettangolo, un poligono o un'ellisse (o una combinazione di due o più di queste forme) che può essere riempito, disegnato, invertito, incorniciato e usato per eseguire l'hit testing (test per la posizione del cursore). |



 

Dal punto di vista dello sviluppatore, una bitmap è costituita da una raccolta di strutture che specificano o contengono gli elementi seguenti:

-   Intestazione che descrive la risoluzione del dispositivo in cui è stato creato il rettangolo di pixel, le dimensioni del rettangolo, le dimensioni della matrice di bit e così via.
-   Tavolozza logica.
-   Matrice di bit che definisce la relazione tra i pixel nell'immagine bitmap e le voci della tavolozza logica.

Una dimensione bitmap è correlata al tipo di immagine che contiene. Le immagini bitmap possono essere monocromatiche o colori. In un'immagine ogni pixel corrisponde a uno o più bit in una bitmap. Le immagini monocromatiche hanno un rapporto di 1 bit per pixel (BPP). La creazione di immagini colore è più complessa. Il numero di colori che possono essere visualizzati da una bitmap è pari a due elevato al numero di bit per pixel. Pertanto, una bitmap a 256 colori richiede 8 BPP (2 ^ 8 = 256).

Le applicazioni del pannello di controllo sono esempi di applicazioni che utilizzano bitmap. Quando si seleziona uno sfondo (o sfondo) per il desktop, si seleziona effettivamente una bitmap, che viene usata dal sistema per disegnare lo sfondo del desktop. Il sistema crea il modello di sfondo selezionato disegnando ripetutamente uno schema di pixel 32 per 32 sul desktop.

Nella figura seguente viene illustrata la prospettiva dello sviluppatore della bitmap trovata nel file Redbrick.bmp. Mostra una matrice di tavolozze, un rettangolo di 32 pixel per 32 e la matrice di indicizzazione che esegue il mapping dei colori dalla tavolozza ai pixel nel rettangolo.

![illustrazione del rettangolo pixel, della matrice della tavolozza e della matrice di indicizzazione di redbrick.bmp](images/csbmp-01.png)

Nell'esempio precedente, il rettangolo di pixel è stato creato in un dispositivo di visualizzazione VGA usando una tavolozza di 16 colori. Una tavolozza a 16 colori richiede indici a 4 bit. Pertanto, la matrice che esegue il mapping dei colori della tavolozza ai colori dei pixel è costituita anche da indici a 4 bit. Per ulteriori informazioni sulle tavolozze dei colori logiche, vedere [colori](colors.md).

> [!Note]
>
> Nella bitmap precedente il sistema esegue il mapping degli indici a pixel a partire dalla riga di analisi inferiore dell'area rettangolare e termina con la linea di analisi superiore. Una *linea di analisi* è una singola riga di pixel adiacenti in una visualizzazione video. Ad esempio, la prima riga della matrice (riga 0) corrisponde alla riga inferiore di pixel, Scan Line 31. Questo è dovuto al fatto che la bitmap precedente è una bitmap indipendente dal dispositivo (DIB), un tipo comune di bitmap. Nelle bitmap dall'alto verso il basso e nelle bitmap dipendenti dal dispositivo (DDB), il sistema esegue il mapping degli indici ai pixel a partire dalla riga di analisi superiore.

 

Negli argomenti seguenti vengono descritte le diverse aree di bitmap.

-   [Classificazioni bitmap](bitmap-classifications.md)
-   [Tipi di intestazione bitmap](bitmap-header-types.md)
-   [Estensioni JPEG e PNG per specifiche funzioni e strutture bitmap](jpeg-and-png-extensions-for-specific-bitmap-functions-and-structures.md)
-   [Bitmap, contesti di dispositivo e superfici di disegno](bitmaps--device-contexts--and-drawing-surfaces.md)
-   [Creazione di bitmap](bitmap-creation.md)
-   [Rotazione bitmap](bitmap-rotation.md)
-   [Ridimensionamento bitmap](bitmap-scaling.md)
-   [Bitmap come pennelli](bitmaps-as-brushes.md)
-   [Archiviazione bitmap](bitmap-storage.md)
-   [Compressione bitmap](bitmap-compression.md)
-   [Fusione alfa](alpha-blending.md)
-   [Ombreggiatura uniforme](smooth-shading.md)
-   [Funzioni bitmap abilitate per ICM](icm-enabled-bitmap-functions.md)

 

 




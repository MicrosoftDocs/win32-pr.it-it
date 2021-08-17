---
description: Una bitmap è uno degli oggetti GDI che possono essere selezionati in un contesto di dispositivo (DC).
ms.assetid: 36afaabc-1334-42d1-8004-7952ce3c119e
title: Informazioni sulle bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb155a2d96b32303c38438663cb7cc9b893a1560e8f33956ff894d309f055010
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119355511"
---
# <a name="about-bitmaps"></a>Informazioni sulle bitmap

Una bitmap è uno degli oggetti GDI che possono essere selezionati in un *contesto di dispositivo* (DC). [I contesti di](device-contexts.md) dispositivo sono strutture che definiscono un set di oggetti grafici e i relativi attributi associati e le modalità grafiche che influiscono sull'output. La tabella seguente descrive gli oggetti GDI che possono essere selezionati in un contesto di dispositivo.



| Oggetto grafico                         | Descrizione                                                                                                                                                                                          |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bitmap](bitmaps.md)                 | Crea, modifica (ridimensionamento, scorrimento, rotazione e disegno) e archivia le immagini come file su disco.                                                                                                       |
| [Pennelli](brushes.md)                 | Disegna l'interno di poligoni, ellissi e tracciati.                                                                                                                                                |
| [Tipi di carattere](fonts-and-text.md)            | Disegna testo su schermi video e altri dispositivi di output.                                                                                                                                               |
| [Riquadro logico](logical-palette.md) | Tavolozza dei colori creata da un'applicazione e associata a un determinato contesto di dispositivo.                                                                                                                |
| [Percorsi](paths.md)                     | Una o più figure (o forme) riempite e/o strutturate.                                                                                                                                     |
| [Penne](pens.md)                       | Strumento grafico utilizzato da un'applicazione per disegnare linee e curve.                                                                                                                                   |
| [Aree](regions.md)                 | Rettangolo, poligono o ellisse (o una combinazione di due o più di queste forme) che può essere riempito, dipinto, invertito, incorniciato e usato per eseguire l'hit testing (test per la posizione del cursore). |



 

Dal punto di vista dello sviluppatore, una bitmap è costituita da una raccolta di strutture che specificano o contengono gli elementi seguenti:

-   Intestazione che descrive la risoluzione del dispositivo in cui è stato creato il rettangolo dei pixel, le dimensioni del rettangolo, le dimensioni della matrice di bit e così via.
-   Riquadro logico.
-   Matrice di bit che definisce la relazione tra i pixel nell'immagine bitmap e le voci nella tavolozza logica.

Le dimensioni di una bitmap sono correlate al tipo di immagine che contiene. Le immagini bitmap possono essere monocroma o a colori. In un'immagine ogni pixel corrisponde a uno o più bit in una bitmap. Le immagini monocroma hanno un rapporto di 1 bit per pixel (bpp). La creazione di immagini a colori è più complessa. Il numero di colori che possono essere visualizzati da una bitmap è pari a due elevato al numero di bit per pixel. Una bitmap a 256 colori richiede quindi 8 bpp (2^8 = 256).

Pannello di controllo applicazioni sono esempi di applicazioni che usano bitmap. Quando si seleziona uno sfondo (o uno sfondo) per il desktop, si seleziona effettivamente una bitmap che il sistema usa per disegnare lo sfondo del desktop. Il sistema crea il modello di sfondo selezionato disegnando ripetutamente un motivo da 32 per 32 pixel sul desktop.

La figura seguente mostra la prospettiva dello sviluppatore della bitmap trovata nel file Redbrick.bmp. Mostra una matrice di tavolozza, un rettangolo di 32 per 32 pixel e la matrice di indici che esegue il mapping dei colori dalla tavolozza ai pixel nel rettangolo.

![illustrazione del rettangolo in pixel, della matrice di tavolozza e della matrice di indici redbrick.bmp](images/csbmp-01.png)

Nell'esempio precedente, il rettangolo di pixel è stato creato in un dispositivo di visualizzazione VGA usando una tavolozza di 16 colori. Una tavolozza a 16 colori richiede indici a 4 bit. Pertanto, la matrice che esegue il mapping dei colori della tavolozza ai colori pixel è costituita anche da indici a 4 bit. Per altre informazioni sulle tavolozze dei colori logiche, vedere [Colori.](colors.md)

> [!Note]
>
> Nella bitmap precedente il sistema esegue il mapping degli indici ai pixel che iniziano con la linea di analisi inferiore dell'area rettangolare e terminano con la riga di analisi superiore. Una *linea di analisi* è una singola riga di pixel adiacenti su una visualizzazione video. Ad esempio, la prima riga della matrice (riga 0) corrisponde alla riga inferiore di pixel, la riga di analisi 31. Ciò è dovuto al fatto che la bitmap precedente è una bitmap indipendente dal dispositivo (DIB) dal basso verso l'alto, un tipo comune di bitmap. Nelle dib dall'alto verso il basso e nelle bitmap dipendenti dal dispositivo (DDB), il sistema esegue il mapping degli indici ai pixel che iniziano con la riga di analisi superiore.

 

Negli argomenti seguenti vengono descritte diverse aree di bitmap.

-   [Classificazioni bitmap](bitmap-classifications.md)
-   [Tipi di intestazione bitmap](bitmap-header-types.md)
-   [Estensioni JPEG e PNG per funzioni e strutture bitmap specifiche](jpeg-and-png-extensions-for-specific-bitmap-functions-and-structures.md)
-   [Bitmap, contesti di dispositivo e superfici di disegno](bitmaps--device-contexts--and-drawing-surfaces.md)
-   [Creazione di bitmap](bitmap-creation.md)
-   [Rotazione bitmap](bitmap-rotation.md)
-   [Ridimensionamento delle bitmap](bitmap-scaling.md)
-   [Bitmap come pennelli](bitmaps-as-brushes.md)
-   [Bitmap Archiviazione](bitmap-storage.md)
-   [Compressione bitmap](bitmap-compression.md)
-   [Fusione alfa](alpha-blending.md)
-   [Ombreggiatura smussata](smooth-shading.md)
-   [ICM funzioni bitmap abilitate per l'accesso remoto](icm-enabled-bitmap-functions.md)

 

 




---
description: Un metafile avanzato è una matrice di record.
ms.assetid: af3261c7-2113-4777-97c0-504f23022550
title: Record metafile migliorati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 506ca77dda1bd90fc04b692dbbd98bc06f4da44c5fc6f8edb0fd17cbd3e94c96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038019"
---
# <a name="enhanced-metafile-records"></a>Record metafile migliorati

Un metafile avanzato è una matrice di record. Un record metafile è una struttura [**ENHMETARECORD**](/windows/win32/api/wingdi/ns-wingdi-enhmetarecord) a lunghezza variabile. All'inizio di ogni record di metafile avanzato è disponibile una [**struttura EMR**](/windows/win32/api/wingdi/ns-wingdi-emr) che contiene due membri. Il primo membro, iType, identifica il tipo di record, la funzione GDI i cui parametri sono contenuti nel record. Poiché le strutture sono di lunghezza variabile, l'altro membro, nSize, contiene le dimensioni del record. Immediatamente dopo il membro nSize sono presenti i parametri rimanenti della funzione GDI. Il resto della struttura contiene dati aggiuntivi dipendenti dal tipo di record.

Il primo record in un metafile avanzato è sempre la [**struttura ENHMETAHEADER,**](/windows/win32/api/wingdi/ns-wingdi-enhmetaheader) ovvero l'intestazione enhanced-metafile. L'intestazione specifica le informazioni seguenti:

-   Dimensioni del metafile, in byte
-   Dimensioni della cornice dell'immagine, in unità dispositivo
-   Dimensioni della cornice dell'immagine, in unità di 0,01 millimetri
-   Numero di record nel metafile
-   Offset a una descrizione di testo facoltativa
-   Dimensioni del riquadro facoltativo
-   Risoluzione del dispositivo originale, in pixel
-   Risoluzione del dispositivo originale, in millimetri

Una descrizione di testo facoltativa può seguire il record di intestazione. La descrizione del testo descrive l'immagine e il nome dell'autore. La tavolozza facoltativa specifica i colori usati per creare il metafile avanzato. I record rimanenti identificano le funzioni GDI usate per creare l'immagine. L'output esadecimale seguente corrisponde a un record generato per una chiamata alla [**funzione SetMapMode.**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode)


```C++
00000011 0000000C 00000004 
```



Il valore 0x00000011 specifica il tipo di record (corrisponde alla costante EMR \_ SETMAPMODE definita nel file Wingdi.h). Il valore 0x0000000C specifica la lunghezza del record, in byte. Il valore 0x00000004 identifica la modalità di mapping (corrisponde alla costante MM \_ LOENGLISH definita nella [**funzione SetMapMode).**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode)

Per un elenco di tipi di record aggiuntivi, vedere [Strutture metafile](metafile-structures.md).

 

 




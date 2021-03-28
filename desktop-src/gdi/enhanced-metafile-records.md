---
description: Un metafile migliorato è una matrice di record.
ms.assetid: af3261c7-2113-4777-97c0-504f23022550
title: Record metafile avanzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2097fd59497838c2a77a0209f6ae715dff2e1cf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978618"
---
# <a name="enhanced-metafile-records"></a>Record metafile avanzati

Un metafile migliorato è una matrice di record. Un record metafile è una struttura [**ENHMETARECORD**](/windows/win32/api/wingdi/ns-wingdi-enhmetarecord) a lunghezza variabile. All'inizio di ogni record del metafile migliorato si tratta di una struttura [**EMR**](/windows/win32/api/wingdi/ns-wingdi-emr) , che contiene due membri. Il primo membro, iType, identifica il tipo di record, ovvero la funzione GDI i cui parametri sono contenuti nel record. Poiché le strutture sono di lunghezza variabile, l'altro membro, nSize, contiene le dimensioni del record. Immediatamente dopo il membro nSize sono i parametri rimanenti, se presenti, della funzione GDI. Il resto della struttura contiene dati aggiuntivi che dipendono dal tipo di record.

Il primo record in un metafile migliorato è sempre la struttura [**ENHMETAHEADER**](/windows/win32/api/wingdi/ns-wingdi-enhmetaheader) , che è l'intestazione Enhanced-Metafile. L'intestazione specifica le informazioni seguenti:

-   Dimensioni del metafile, in byte
-   Dimensioni del frame immagine, in unità dispositivo
-   Dimensioni del frame immagine, in unità. 01-mm
-   Numero di record nel metafile
-   Offset a una descrizione di testo facoltativa
-   Dimensioni della tavolozza facoltativa
-   Risoluzione del dispositivo originale, in pixel
-   Risoluzione del dispositivo originale, in millimetri

Una descrizione di testo facoltativa può seguire il record di intestazione. La descrizione del testo descrive l'immagine e il nome dell'autore. La tavolozza facoltativa specifica i colori utilizzati per creare il metafile avanzato. I record rimanenti identificano le funzioni GDI utilizzate per la creazione dell'immagine. Il seguente output esadecimale corrisponde a un record generato per una chiamata alla funzione [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) .


```C++
00000011 0000000C 00000004 
```



Il valore 0x00000011 specifica il tipo di record (corrisponde alla \_ costante SETMAPMODE di EMR definita nel file wingdi. h). Il valore 0x0000000C specifica la lunghezza, in byte, del record. Il valore 0x00000004 identifica la modalità di mapping (corrisponde alla \_ costante mm LOENGLISH definita nella funzione [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) ).

Per un elenco di altri tipi di record, vedere [strutture di metafile](metafile-structures.md).

 

 




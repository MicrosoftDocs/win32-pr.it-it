---
description: Le applicazioni devono allocare memoria per questi dati. TAPI e il provider di servizi forniscono i dati. Se l'operazione è asincrona, i dati non saranno disponibili fino a quando il messaggio di risposta asincrono non indicherà l'esito positivo.
ms.assetid: 61313fe3-74a1-4195-b5af-37463dad02c1
title: Allocazione della memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f192e34fdc652293c480277631c3839ecd2435fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305587"
---
# <a name="memory-allocation"></a>Allocazione della memoria

Le applicazioni devono allocare memoria per questi dati. TAPI e il provider di servizi forniscono i dati. Se l'operazione è asincrona, i dati non saranno disponibili fino a quando il messaggio di risposta asincrono non indicherà l'esito positivo.

Tutte le strutture di dati utilizzate per passare i dati tra l'applicazione e il TAPI sono *bidimensionali*. Ovvero le strutture dei dati non contengono puntatori a sottostrutture che contengono componenti di dati di dimensioni variabili. Al contrario, le strutture di dati utilizzate per passare quantità variabili di dati all'applicazione devono avere la metastruttura seguente:

``` syntax
  DWORD  dwTotalSize;
  DWORD  dwNeededSize;
  DWORD  dwUsedSize; 
    <fixed size fields> 
  DWORD  dw<VarSizeField1>Size;
  DWORD  dw<VarSizeField1>Offset; 
    <fixed size fields> 
  DWORD  dw<VarSizeField2>Size;
  DWORD  dw<VarSizeField2>Offset; 
    <common extensions> 
    <var sized field1> 
    <var sized field2>
```

Il membro **dwTotalSize** è la dimensione, in byte, allocata a questa struttura di dati. Contrassegna la fine della struttura dei dati e viene impostata dall'applicazione prima di richiamare la funzione che usa questa struttura di dati. La funzione non legge o scrive oltre questa dimensione. Un'applicazione deve impostare il membro **dwTotalSize** per indicare il numero totale di byte allocati per TAPI per restituire il contenuto della struttura.

TAPI compila il membro **dwNeededSize** . Indica il numero di byte necessari per restituire tutti i dati richiesti. L'esistenza di campi di dimensioni variabili rende spesso impossibile per l'applicazione stimare la dimensione della struttura di dati necessaria per l'allocazione. Questo campo restituisce il numero di byte effettivamente necessari per i dati. Questo numero può essere minore, uguale o maggiore di **dwTotalSize** e include lo spazio per il membro **dwTotalSize** stesso. Se più grande, la struttura restituita viene riempita solo parzialmente. Se i campi richiesti dall'applicazione sono disponibili nella struttura parziale, non è necessario eseguire altre operazioni. In caso contrario, l'applicazione deve allocare una struttura almeno la dimensione di **dwNeededSize** e richiamare di nuovo la funzione. In genere, è disponibile spazio sufficiente per restituire tutte le informazioni, anche se è possibile che le dimensioni siano aumentate.

TAPI compila il membro **dwUsedSize** se restituisce dati all'applicazione per indicare le dimensioni effettive, in byte, della parte della struttura di dati che contiene dati utili. Se, ad esempio, una struttura allocata è troppo piccola e il campo troncato è un campo di dimensioni variabilmente, **dwNeededSize** è maggiore di **dwTotalSize** e il campo troncato viene lasciato vuoto. Il membro **dwUsedSize** può quindi essere minore di **dwTotalSize**. I valori dei campi parziali non vengono restituiti.

L'intestazione seguente è la parte fissa della struttura dei dati. Contiene campi normali e coppie di dimensioni/offset che descrivono i campi di dimensioni effettive. Il campo Offset contiene l'offset in byte del campo di dimensioni variabili dall'inizio del record. Il campo dimensione contiene le dimensioni in byte del campo di dimensioni variabili. Se un campo di dimensioni variabili è vuoto, il campo dimensione è zero e l'offset è impostato su zero. Campi di dimensioni variabili che verrebbero troncati se le dimensioni totali della struttura sono insufficienti. Ovvero il campo relativo alle dimensioni viene impostato su zero e l'offset viene impostato su zero. I campi di dimensioni variabili seguono i campi fissi.

Se il provider di servizi deve riempire un membro variabile, TAPI Inizializza i membri size e offset corrispondenti su zero. Se il provider di servizi compila il membro della variabile, deve impostare i membri di dimensioni e offset corrispondenti sui valori appropriati, inclusi **dwUsedSize** e **dwNeededSize** se imposta membri variabili. Il provider di servizi non deve troncare un membro della variabile per adattarlo allo spazio disponibile.

Il provider di servizi deve avviare membri variabili immediatamente dopo i membri fissi della struttura e lasciare spazio aggiuntivo alla fine della memoria allocata, in modo che TAPI possa usarlo per i membri a lunghezza variabile. Può inserire i membri della variabile in qualsiasi ordine, ma i membri devono essere contigui.

 

 




---
description: Viene fornita una breve introduzione ad alcuni tipi di situazioni di sovraccarico del buffer e vengono offerte alcune idee e risorse che consentono di evitare la creazione di nuovi rischi e attenuare quelli esistenti.
ms.assetid: 713fd6de-16af-49d2-8940-763c4a6e414b
title: Evitare i sovraccarichi del buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c8a3456384e799380fa0041172fb2b2ea09c0c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315422"
---
# <a name="avoiding-buffer-overruns"></a>Evitare i sovraccarichi del buffer

Un sovraccarico del buffer è una delle fonti più comuni di rischio per la sicurezza. Un sovraccarico del buffer è essenzialmente causato dal trattamento degli input esterni deselezionati come dati attendibili. L'atto di copiare questi dati, usando operazioni come [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)), **strcat**, **strcpy** o **wcscpy**, può creare risultati imprevisti che consentono il danneggiamento del sistema. Nei casi migliori, l'applicazione verrà interrotta con un dump di base, un errore di segmentazione o una violazione di accesso. Nel peggiore dei casi, un utente malintenzionato può sfruttare il sovraccarico del buffer introducendo ed eseguendo altro codice dannoso nel processo. La copia di dati di input deselezionati in un buffer basato su stack è la ragione più comune di errori sfruttabili.

I sovraccarichi del buffer possono essere eseguiti in diversi modi. Nell'elenco seguente viene fornita una breve introduzione ad alcuni tipi di situazioni di sovraccarico del buffer e vengono offerte alcune idee e risorse che consentono di evitare la creazione di nuovi rischi e attenuare quelli esistenti:

<dl> <dt>

<span id="Static_buffer_overruns"></span><span id="static_buffer_overruns"></span><span id="STATIC_BUFFER_OVERRUNS"></span>Sovraccarichi del buffer statici
</dt> <dd>

Un sovraccarico del buffer statico si verifica quando un buffer, dichiarato nello stack, viene scritto con un numero di dati superiore a quello allocato. Le versioni meno evidenti di questo errore si verificano quando i dati di input utente non verificati vengono copiati direttamente in una variabile statica, causando un potenziale danneggiamento dello stack.

</dd> <dt>

<span id="Heap_overruns"></span><span id="heap_overruns"></span><span id="HEAP_OVERRUNS"></span>Sovraccarichi heap
</dt> <dd>

I sovraccarichi dell'heap, come i sovraccarichi del buffer statico, possono causare danneggiamenti della memoria e dello stack. Poiché i sovraccarichi dell'heap si verificano nella memoria heap anziché nello stack, alcuni utenti li considerano meno in grado di causare gravi problemi; Tuttavia, i sovraccarichi dell'heap richiedono una reale attenzione alla programmazione e sono in grado di consentire i rischi di sistema come sovraccarichi del buffer statico.

</dd> <dt>

<span id="Array_indexing_errors"></span><span id="array_indexing_errors"></span><span id="ARRAY_INDEXING_ERRORS"></span>Errori di indicizzazione della matrice
</dt> <dd>

Gli errori di indicizzazione della matrice sono inoltre un'origine di sovraccarichi di memoria. Il controllo accurato dei limiti e la gestione degli indici contribuiranno a impedire questo tipo di sovraccarico di memoria.

</dd> </dl>

La prevenzione dei sovraccarichi del buffer riguarda principalmente la scrittura di codice valido. Convalidare sempre tutti gli input e non eseguire correttamente l'operazione quando necessario. Per ulteriori informazioni sulla scrittura di codice protetto, vedere le risorse seguenti:

-   Maguire, Steve \[ 1993 \] , *scrittura di codice solido*, ISBN 1-55615-551-4, Microsoft Press, Redmond, Washington.
-   Howard, Michael e LeBlanc, David \[ 2003 \] , *scrittura di codice sicuro*, 2D ed., ISBN 0-7356-1722-8, Microsoft Press, Redmond, Washington.

> [!Note]  
> Queste risorse potrebbero non essere disponibili in alcune lingue e paesi.

 

Una gestione sicura delle stringhe è un problema di lunga durata che continua a essere risolto, seguendo le buone procedure di programmazione e spesso usando e adeguando i sistemi esistenti con funzioni sicure di gestione delle stringhe. Un esempio di tale set di funzioni per la shell di Windows inizia con [**StringCbCat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata).

 

 

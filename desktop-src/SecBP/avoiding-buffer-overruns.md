---
description: Fornisce una breve introduzione ad alcuni tipi di situazioni di sovraccarico del buffer e offre alcune idee e risorse che consentono di evitare di creare nuovi rischi e mitigare quelli esistenti.
ms.assetid: 713fd6de-16af-49d2-8940-763c4a6e414b
title: Evitare sovraccarichi del buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae85d66d32b1efc29e75e187bb1afa67653084a3b9c729cd56728078f5e0c1ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622951"
---
# <a name="avoiding-buffer-overruns"></a>Evitare sovraccarichi del buffer

Un sovraccarico del buffer è una delle origini più comuni di rischio per la sicurezza. Un sovraccarico del buffer è causato essenzialmente dal fatto che l'input esterno non controllato viene trattato come dati attendibili. L'operazione di copia di questi dati, usando operazioni come [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)), **strcat**, **strcpy** o **wcscpy**, può creare risultati imprevisti, che consentono il danneggiamento del sistema. Nel migliore dei casi, l'applicazione verrà interrotta con un dump principale, un errore di segmentazione o una violazione di accesso. Nel peggiore dei casi, un utente malintenzionato può sfruttare il sovraccarico del buffer introducendo ed eseguendo altro codice dannoso nel processo. La copia dei dati di input non selezionata in un buffer basato su stack è la causa più comune di errori sfruttabili.

I sovraccarichi del buffer possono verificarsi in diversi modi. L'elenco seguente offre una breve introduzione ad alcuni tipi di situazioni di sovraccarico del buffer e offre alcune idee e risorse per evitare di creare nuovi rischi e mitigare quelli esistenti:

<dl> <dt>

<span id="Static_buffer_overruns"></span><span id="static_buffer_overruns"></span><span id="STATIC_BUFFER_OVERRUNS"></span>Sovraccarichi del buffer statici
</dt> <dd>

Un sovraccarico del buffer statico si verifica quando un buffer, dichiarato nello stack, viene scritto in con più dati di quelli allocati per contenere. Le versioni meno evidenti di questo errore si verificano quando i dati di input utente non verificato vengono copiati direttamente in una variabile statica, causando un potenziale danneggiamento dello stack.

</dd> <dt>

<span id="Heap_overruns"></span><span id="heap_overruns"></span><span id="HEAP_OVERRUNS"></span>Sovraccarichi dell'heap
</dt> <dd>

I sovraccarichi dell'heap, come i sovraccarichi statici del buffer, possono causare il danneggiamento della memoria e dello stack. Poiché i sovraccarichi dell'heap si verificano nella memoria heap anziché nello stack, alcuni utenti li considerano meno in grado di causare gravi problemi. tuttavia, i sovraccarichi dell'heap richiedono un'attenzione di programmazione reale e sono in grado di consentire rischi di sistema come sovraccarichi statici del buffer.

</dd> <dt>

<span id="Array_indexing_errors"></span><span id="array_indexing_errors"></span><span id="ARRAY_INDEXING_ERRORS"></span>Errori di indicizzazione delle matrici
</dt> <dd>

Gli errori di indicizzazione delle matrici sono anche un'origine di sovraccarichi della memoria. Un controllo accurato dei limiti e la gestione degli indici consentono di evitare questo tipo di sovraccarico della memoria.

</dd> </dl>

La prevenzione dei sovraccarichi del buffer riguarda principalmente la scrittura di codice valido. Convalidare sempre tutti gli input e, se necessario, non riuscire normalmente. Per altre informazioni sulla scrittura di codice sicuro, vedere le risorse seguenti:

-   Maguire, Steve \[ 1993, \] Writing Solid *Code*, ISBN 1-55615-551-4, Microsoft Press, Redmond, Washington.
-   Michael, Michael e LeBlanc, David \[ 2003, \] *Writing Secure Code*, 2d ed., ISBN 0-7356-1722-8, Microsoft Press, Redmond, Washington.

> [!Note]  
> Queste risorse potrebbero non essere disponibili in alcune lingue e paesi.

 

Cassaforte gestione delle stringhe è un problema di lunga data che continua a essere risolto sia seguendo procedure di programmazione ottimali che spesso usando e retrofitting sistemi esistenti con funzioni sicure di gestione delle stringhe. Un esempio di questo set di funzioni per la shell Windows inizia [**con StringCbCat.**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata)

 

 

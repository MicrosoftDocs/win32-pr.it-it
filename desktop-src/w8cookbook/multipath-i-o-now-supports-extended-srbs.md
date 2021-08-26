---
title: Multipath I/O ora supporta blocchi di richieste di archiviazione estese
description: Multipath I/O ora supporta blocchi di richieste di archiviazione estese
ms.assetid: 5373D9ED-34AF-4D66-8888-49F1EBF768F4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a3b3a5ce3050bf7fddc2bd77da30e766c7b9cd67a8c4f49c753da5302b104c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119932211"
---
# <a name="multipath-io-now-supports-extended-storage-request-blocks"></a>Multipath I/O ora supporta blocchi di richieste di archiviazione estese

## <a name="platforms"></a>Piattaforme

**Server** - Windows Server 2012 

## <a name="description"></a>Descrizione

In Windows Server 2012 nuova struttura, STORAGE \_ REQUEST \_ BLOCK (SRB esteso) sostituisce SCSI \_ REQUEST BLOCK \_ (SRB legacy) nello stack di archiviazione core. Gli SDB estesi replicano le funzionalità degli SDB legacy, ma sono anche estendibili e scalabili.

Multipath I/O (MPIO) supporta SRB estesi e consente ai moduli specifici del dispositivo (DMS) di specificare anche il supporto SRB esteso. Tuttavia, perché lo stack di archiviazione di un dispositivo multipath usi SDB estesi, tutti i componenti dello stack devono supportare SBS estesi, incluso **DSM**. Si noti che microsoft in-box DSM, MSDSM, supporta SDB estesi.

La struttura SCSI PASS THROUGH EX non fa parte della struttura pass-through MPIO estesa perché il pass-through SCSI esteso può avere dimensioni variabili, a seconda del debugger della riga di comando \_ \_ \_ (CDB). Il pass-through MPIO esteso include invece un campo che descrive l'offset dall'inizio della struttura pass-through MPIO estesa alla struttura \_ SCSI PASS \_ THROUGH \_ EX. Il chiamante deve assicurarsi di allocare un buffer delle dimensioni appropriate e impostare correttamente l'offset pass-through SCSI. Purché il chiamante segua le regole per i pass-through SCSI estesi, non deve essere necessario eseguire operazioni aggiuntive per l'uso del pass-through MPIO esteso.

> [!Note]  
> Se il DSM non supporta SDB estesi, MPIO avrà esito negativo per le richieste pass-through MPIO estese con il flag DSM MPIO \_ IOCTL \_ FLAG \_ INVOLVE \_ impostato.

 

## <a name="manifestation"></a>Manifestazione

Se una parte qualsiasi dello stack di archiviazione del dispositivo, incluso DSM, non supporta gli SDB estesi, lo stack di archiviazione tornerà a usare IB legacy.

## <a name="solution"></a>Soluzione

Esistono solo due requisiti MPIO per un DSM per supportare BLOCCHI DI \_ RICHIESTA DI \_ ARCHIVIAZIONE:

-   Il DSM deve segnalare il tipo come DsmType6
-   Il DSM deve fornire la funzione DSM \_ ADDRESS \_ TYPE \_ SUPPORTED

Se il DSM non segnala DsmType6 o se segnala DsmType6 ma non fornisce la funzione DSM \_ ADDRESS \_ TYPE SUPPORTED, MPIO presuppone che il DSM non supporti IDB \_ estesi.

La funzione DSM \_ ADDRESS TYPE SUPPORTED accetta due \_ \_ parametri, uno dei quali è un tipo di indirizzo. Questo tipo di indirizzo deve essere uno dei valori STORAGE \_ ADDRESS TYPE definiti in \_ \_ \* srb.h. Il DSM deve restituire TRUE se supporta il tipo di indirizzo specificato e FALSE in caso contrario. La definizione di "supporto" è alla fine del DSM. MPIO usa questa funzione per garantire che il DSM non si comporta in modo errato se viene passato un SRB esteso con una struttura STOR \_ ADDRESS del tipo specificato. Di conseguenza, MPIO chiama in genere questa funzione quando un dispositivo multipath viene enumerato, ma la funzione può essere chiamata in qualsiasi momento.

Se un DSM non tocca mai l'indirizzo STOR di un SRB esteso, può restituire TRUE per qualsiasi \_ valore DI TIPO DI INDIRIZZO DI ARCHIVIAZIONE \_ \_ \_ \* valido. Esaminare il DSM di esempio in WDK.

**Altre note importanti**

-   I DSM che supportano SDB estesi devono essere in grado di gestire sia le strutture SCSI REQUEST BLOCK che le strutture \_ \_ STORAGE REQUEST \_ \_ BLOCK. Solo perché un DSM segnala che supporta SDB estesi non significa che riceverà esclusivamente SRB estesi. Può comunque ricevere un numero qualsiasi di SDB legacy oltre a SRB estesi e pertanto deve essere in grado di gestirlo entrambi.
-   È stato fornito un file di intestazione in WDK denominato srbhelper.h che contiene funzioni inline per aiutare i driver che devono gestire sia gli SRB estesi che i legacy. Il DSM di esempio usa questa intestazione in modo da poterla usare come esempio di come usare queste funzioni.
-   Un DSM che non supporta gli SDB estesi non dovrà mai gestire gli SRB estesi.
-   È possibile che un MPIO causerà il fall back dello stack di archiviazione su SDB legacy nel caso in cui il modulo di protezione dei dati non supporti un determinato TIPO DI INDIRIZZO DI ARCHIVIAZIONE (ma supporta in caso contrario \_ \_ SRB \_ \* estesi).
-   "BTL8" è l'unico TIPO DI INDIRIZZO DI ARCHIVIAZIONE \_ \_ attualmente definito per \_ \* Windows Server 2012.

 

 





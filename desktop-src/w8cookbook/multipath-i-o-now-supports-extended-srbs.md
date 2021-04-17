---
title: Multipath I/O supporta ora i blocchi delle richieste di archiviazione estesa
description: Multipath I/O supporta ora i blocchi delle richieste di archiviazione estesa
ms.assetid: 5373D9ED-34AF-4D66-8888-49F1EBF768F4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f558f8088b5066b51447c5f2ea23edd5154d5c10
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/10/2020
ms.locfileid: "104339503"
---
# <a name="multipath-io-now-supports-extended-storage-request-blocks"></a>Multipath I/O supporta ora i blocchi delle richieste di archiviazione estesa

## <a name="platforms"></a>Piattaforme

**Server** : Windows Server 2012 

## <a name="description"></a>Descrizione

In Windows Server 2012, una nuova struttura, il blocco di richieste di archiviazione \_ \_ (SRB esteso) sostituisce \_ il \_ blocco di richieste SCSI (SRB legacy) nello stack di archiviazione principale. SRB estese replicano le funzionalità del SRB legacy, ma sono anche estendibili e scalabili.

Multipath I/O (MPIO) supporta SRB esteso e consente ai moduli specifici del dispositivo (DSM) di specificare anche il supporto per SRB esteso. Tuttavia, per fare in modo che lo stack di archiviazione di un dispositivo a percorsi multipli usi SRB estesi, **tutti i componenti nello stack devono supportare SRB estesi, incluso il DSM**. Si noti che il DSM interno di Microsoft, MSDSl, supporta il SRB esteso.

La \_ struttura ad albero pass- \_ through SCSI non fa \_ parte della struttura pass-through MPIO estesa perché il pass-through SCSI esteso può avere una dimensione variabile, a seconda del debugger della riga di comando (CDB). Al contrario, il pass-through MPIO esteso ha un campo che descrive l'offset dall'inizio della struttura pass-through MPIO estesa alla struttura del pass-through SCSI \_ \_ \_ . Il chiamante deve assicurarsi di allocare un buffer di dimensioni appropriate e impostare correttamente l'offset del pass-through SCSI. Finché il chiamante segue le regole per i pass-through SCSI estesi, non dovrebbe essere necessario alcun lavoro aggiuntivo per poter utilizzare il pass-through MPIO esteso.

> [!Note]  
> Se il DSM non supporta il SRB esteso, MPIO non riuscirà a eseguire le richieste di pass-through MPIO estese che hanno il \_ flag IOCTL MPIO che \_ coinvolgono il \_ \_ flag DSM impostato.

 

## <a name="manifestation"></a>Manifestazione

Se una parte dello stack di archiviazione del dispositivo, incluso DSM, non supporta il SRB esteso, lo stack di archiviazione verrà ripristinato usando SRB legacy.

## <a name="solution"></a>Soluzione

Esistono solo due requisiti MPIO per un DSM per supportare i blocchi delle richieste di archiviazione \_ \_ :

-   Il DSM deve segnalare il tipo come DsmType6
-   Il DSM deve fornire la \_ \_ \_ funzione supportata per il tipo di indirizzo DSM

Se il DSM non segnala DsmType6 o restituisce DsmType6 ma non fornisce la \_ funzione supportata per il tipo di indirizzo DSM \_ \_ , MPIO presuppone che il DSM non supporti SRB estesi.

La \_ \_ funzione supportata per il tipo di indirizzo DSM \_ accetta due parametri, uno dei quali è un tipo di indirizzo. Questo tipo di indirizzo deve essere uno dei valori del tipo di indirizzo di archiviazione \_ \_ \_ \* definito in SRB. h. Il DSM deve restituire TRUE se supporta il tipo di indirizzo specificato e FALSE in caso contrario. La definizione di "supporto" è alla fine il DSM. MPIO usa questa funzione per garantire che il DSM non si comporti in modo non conforme se viene passata una SRB estesa con una \_ struttura dell'indirizzo stor del tipo specificato. Di conseguenza, MPIO chiama in genere questa funzione quando un dispositivo a percorsi multipli viene enumerato, ma la funzione può essere chiamata in qualsiasi momento.

Se un DSM non tocca mai un indirizzo STOR esteso di SRB \_ , può restituire true per qualsiasi valore di tipo di indirizzo di archiviazione valido \_ \_ \_ \* . Esaminare il DSM di esempio in WDK.

**Altre note importanti**

-   DSM che supportano SRB estese devono essere in grado di gestire sia le strutture del \_ blocco di richieste SCSI sia \_ le strutture di blocco delle richieste di archiviazione \_ \_ . Solo perché un DSM segnala che supporta SRB esteso non significa che riceva esclusivamente SRB estese. Può comunque ricevere un numero qualsiasi di SRB legacy oltre ai SRB estesi e pertanto deve essere in grado di gestire entrambe.
-   È stato fornito un file di intestazione in WDK denominato srbhelper. h che contiene funzioni inline per aiutare i driver che devono gestire SRB estesi e legacy. Il DSM di esempio usa questa intestazione per poterla usare come esempio di come usare queste funzioni.
-   Un DSM che non supporta SRB estesi non dovrà mai gestire SRB estesi.
-   È possibile che un MPIO provochi il fallback dello stack di archiviazione nei SRB legacy nel caso in cui il DSM non supporti un determinato tipo di indirizzo di archiviazione \_ \_ \_ \* (ma in caso contrario supporta SRB estesi).
-   "BTL8" è l'unico \_ \_ tipo di indirizzo \_ \* di archiviazione attualmente definito per Windows Server 2012.

 

 





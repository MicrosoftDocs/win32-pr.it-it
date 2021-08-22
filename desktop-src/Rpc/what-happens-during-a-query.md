---
title: Cosa accade durante una query
description: In questa sezione viene descritto come la rete gestisce la query quando un client a 32 bit cerca un nome nel proprio dominio.
ms.assetid: a8a88743-a245-4258-af05-9261c214ab50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7377df4ced562bc166fedbf489724a2a4a042855391db45841b5de5cf5af906
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010429"
---
# <a name="what-happens-during-a-query"></a>Cosa accade durante una query

In questa sezione viene descritto come la rete gestisce la query quando un client a 32 bit cerca un nome nel proprio dominio.

Quando l'applicazione client chiama [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina), il localizzatore che risiede nel computer client tenterà di soddisfare questa richiesta. Se non è presente alcun elemento nella cache, la richiesta tramite RPC verrà inoltrata a un localizzatore master. Se il localizzatore master non trova nulla nella cache, invia la richiesta a tutti i computer del dominio usando una trasmissione di slot di posta elettronica. Se è presente una corrispondenza, il localizzatore in ogni computer risponderà da uno slot di posta elettronica diretto. Ad esempio, se l'interfaccia è stata esportata da un processo in tale computer. Le risposte vengono collate e la RPC viene completata dal localizzatore di processi del client, che risponderà al processo client stesso.

In un dominio, il localizzatore client cerca un localizzatore master nelle posizioni seguenti:

-   Nel controller di dominio primario
-   In ogni controller di dominio di backup

Se non viene trovata una corrispondenza, il localizzatore client si dichiara come il localizzatore master. Di conseguenza, trasmetterà le query se non possono essere soddisfatte in locale.

In un gruppo di lavoro, il localizzatore client gestisce una cache dei computer i cui localizzatori hanno trasmesso. Usa quello che è stato eseguito più a lungo come localizzatore master. Se il computer non è disponibile, viene usato il computer successivo con la trasmissione più lunga e così via. Se il client necessita di un localizzatore master e la cache è vuota, riempie la cache inviando una trasmissione speciale dello slot di posta che richiede ai localizzatori master di rispondere. Se non sono presenti risposte, il localizzatore client si dichiara come il localizzatore master e trasmetterà le query se non possono essere soddisfatte localmente.

Questa modifica si verifica se l'applicazione client è un programma a 16 bit o basato su MS-DOS. In questo caso, nel computer client non è in esecuzione alcun localizzatore e Rpcns1.dll o Rpcnslm.rpc contiene il codice per trovare un localizzatore master. Tutte le richieste vengono inoltrate direttamente al localizzatore master.

Queste linee guida sono valide per i nomi nel dominio del client, ad esempio i nomi per "/.:/ entryname". Se il client richiede un nome da un altro dominio tramite l'uso di "/.../DOMAIN/entryname;", il localizzatore client inoltra la richiesta al dominio specificato che lo trasmetterà se non ha la risposta. Se il dominio non è disponibile o è effettivamente un gruppo di lavoro, la richiesta avrà esito negativo.

> [!Note]  
> Tenere presente quanto segue quando si lavora con le voci nel servizio dei nomi:

 

-   Un client non può usare la sintassi "/.../DOMAIN/entryname" per trovare una voce nel proprio dominio. Usare la sintassi "/.:/ entryname". È tuttavia possibile usare "/.../DOMAIN/entryname" per trovare una voce in un altro dominio.
-   Il nome di dominio in "/.../DOMAIN/entryname" deve essere maiuscolo. Quando si cerca una corrispondenza, il localizzatore fa distinzione tra maiuscole e minuscole.
-   Anche i nomi delle voci del localizzatore supportano la distinzione tra maiuscole e minuscole, ma non devono essere maiuscoli.
-   Quando il client usa "/.:/ entryname", il localizzatore non cerca le voci in altri domini, anche se hanno una relazione di trust con il dominio di accesso.
-   Le trasmissioni non attraversano segmenti LAN (ad esempio, subnet). Di conseguenza, l'utilità del localizzatore è limitata in un'organizzazione con più subnet.

 

 





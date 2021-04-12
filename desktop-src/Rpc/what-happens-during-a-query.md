---
title: Cosa accade durante una query
description: Questa sezione descrive il modo in cui la rete gestisce la query quando un client a 32 bit cerca un nome nel relativo dominio.
ms.assetid: a8a88743-a245-4258-af05-9261c214ab50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e26fb9aaef0aac2ff66260d51f756725566dee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221487"
---
# <a name="what-happens-during-a-query"></a>Cosa accade durante una query

Questa sezione descrive il modo in cui la rete gestisce la query quando un client a 32 bit cerca un nome nel relativo dominio.

Quando l'applicazione client chiama [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina), il localizzatore che risiede nel computer client tenterà di soddisfare la richiesta. Se nella cache non è presente alcun elemento, la richiesta verrà trasmessa da RPC a un localizzatore master. Se il localizzatore master non trova alcun elemento nella cache, Invia la richiesta a tutti i computer nel dominio usando una trasmissione dello slot di posta elettronica. Se esiste una corrispondenza, il localizzatore in ogni computer risponderà da uno slot di posta elettronica diretto. Se, ad esempio, un processo nel computer ha esportato l'interfaccia. Le risposte vengono confrontate e la RPC viene completata dal localizzatore del processo del client, che risponderà al processo client.

In un dominio, il localizzatore client cerca un localizzatore Master nelle posizioni seguenti:

-   Sul controller di dominio primario
-   In ogni controller di dominio di backup

Se non viene trovata alcuna corrispondenza, il localizzatore client dichiara se stesso come localizzatore master. Di conseguenza, le query verranno trasmesse se non possono essere soddisfatte localmente.

In un gruppo di lavoro, il localizzatore client gestisce una cache dei computer i cui localizzatori hanno broadcast. USA quello che ha eseguito il più lungo come localizzatore master. Se il computer non è disponibile, viene usato il computer successivo, con trasmissione prolungata e così via. Se il client necessita di un localizzatore master e la cache è vuota, la cache viene rifornita inviando una trasmissione speciale di slot di posta elettronica che richiede ai localizzatori Master di rispondere. Se non sono presenti risposte, il localizzatore client dichiara se stesso come localizzatore master e trasmette le query se non è possibile soddisfarle localmente.

Questa modifica è stata modificata se l'applicazione client è un programma basato su MS-DOS o a 16 bit. In questo caso, nel computer client non è in esecuzione alcun localizzatore e Rpcns1.dll o Rpcnslm. RPC contiene il codice per trovare un localizzatore master. Tutte le richieste vengono inviate direttamente al localizzatore master.

Queste linee guida sono valide per i nomi nel dominio del client, ad esempio i nomi per "/.:/ entryName ". Se il client richiede un nome da un altro dominio tramite l'uso di "/.../DOMAIN/entryname;", il localizzatore client invia la richiesta al dominio specificato, che lo trasmette se non ha la risposta. Se il dominio non è attivo o è in realtà un gruppo di lavoro, la richiesta avrà esito negativo.

> [!Note]  
> Tenere presente quanto segue quando si utilizzano le voci nel servizio nome:

 

-   Un client non può usare la sintassi "/.../DOMAIN/entryname" per trovare una voce nel relativo dominio. Utilizzare la sintassi "/.:/ entryName ". Tuttavia, è possibile usare "/.../DOMAIN/entryname" per trovare una voce in un altro dominio.
-   Il nome di dominio in "/.../DOMAIN/entryname" deve essere in maiuscolo. Per la ricerca di una corrispondenza, il localizzatore distingue tra maiuscole e minuscole.
-   I nomi di voce del localizzatore fanno distinzione tra maiuscole e minuscole, ma non devono essere in maiuscolo.
-   Quando il client usa il "/.:/ entryName "sintassi, il localizzatore non cercherà le voci in altri domini, anche se hanno una relazione di trust con il dominio di accesso.
-   Le trasmissioni non intervengono tra i segmenti LAN, ad esempio le subnet. Pertanto, l'utilità del localizzatore è limitata all'interno di un'organizzazione con più subnet.

 

 





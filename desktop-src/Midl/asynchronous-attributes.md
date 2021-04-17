---
title: Attributi asincroni
description: Quando un programma richiama una stored procedure in un'interfaccia, la procedura può essere eseguita in modo sincrono o asincrono.
ms.assetid: 3e6c6c13-1524-41b2-96dc-3885eadb847c
keywords:
- IDL MIDL, attributi MIDL, asincrono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00aca2276bf1fa5178f1dca3ae4803544066d983
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299659"
---
# <a name="asynchronous-attributes"></a>Attributi asincroni

Quando un programma richiama una stored procedure in un'interfaccia, la procedura può essere eseguita in modo sincrono o asincrono. Una procedura sincrona fa in modo che il programma chiamante attenda che la procedura venga restituita prima che il programma possa continuare. Una procedura asincrona restituisce immediatamente un valore senza attendere i risultati. Il programma chiamante deve quindi essere risincronizzato con la procedura di interfaccia per ricevere i dati. Per ulteriori informazioni, vedere [RPC asincrono](/windows/desktop/Rpc/asynchronous-rpc).

È possibile utilizzare gli attributi seguenti per fornire supporto per le chiamate asincrone a procedure remote.



| Attributo                         | Utilizzo                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**async**](async.md)            | Quando viene applicato a un parametro di funzione, definisce un handle che consente al chiamante di eseguire una chiamata asincrona e restituire immediatamente un risultato senza attendere i risultati e successivamente risincronizzarlo con la funzione chiamata per ricevere i dati dopo il completamento della chiamata. L'attributo [**Async**](async.md) viene inoltre usato nei file ACF per definire un handle asincrono per una routine o un'intera interfaccia. Per le interfacce COM, questa interfaccia è obsoleta e non può essere usata per le nuove interfacce. |
| [**\_UUID asincrono**](async-uuid.md) | Indica al compilatore MIDL di definire le versioni sincrone e asincrone di un'interfaccia COM.                                                                                                                                                                                                                                                                                                                                                                                      |
| [**Forse**](maybe.md)            | Il client che effettua questa chiamata di procedura remota non prevede alcuna risposta che indichi il recapito o il completamento della chiamata e il recapito non è garantito. Si differenziano dalle operazioni dei **messaggi** in cui non è prevista alcuna risposta, ma il recapito è garantito.                                                                                                                                                                                                                    |
| [**Messaggio**](message.md)        | La chiamata di procedura remota deve essere considerata come un messaggio asincrono dal client al server. Il client effettua la chiamata e restituisce immediatamente un risultato, mentre la chiamata effettiva viene gestita dal trasporto di Accodamento messaggi ([**ncadg \_ mq**](ncadg-mq.md)).                                                                                                                                                                                                                              |



 

 

 
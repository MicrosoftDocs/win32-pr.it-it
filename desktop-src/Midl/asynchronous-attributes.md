---
title: Attributi asincroni
description: Quando un programma richiama una routine in un'interfaccia, la procedura può essere eseguita in modo sincrono o asincrono.
ms.assetid: 3e6c6c13-1524-41b2-96dc-3885eadb847c
keywords:
- IDL MIDL, attributi MIDL , asincroni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14ad045be5c3f5980c99fac0e924181c31ae7859f801608c7bb53fe3d81a2b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807854"
---
# <a name="asynchronous-attributes"></a>Attributi asincroni

Quando un programma richiama una routine in un'interfaccia, la procedura può essere eseguita in modo sincrono o asincrono. Una procedura sincrona fa in modo che il programma chiamante attenda il completamento della procedura prima che il programma possa continuare. Una procedura asincrona viene restituita immediatamente senza attendere i risultati. Il programma chiamante deve in seguito risincronizzare con la procedura di interfaccia per ricevere i dati. Per altre informazioni, vedere [RPC asincrona.](/windows/desktop/Rpc/asynchronous-rpc)

È possibile utilizzare gli attributi seguenti per fornire il supporto per le chiamate asincrone di procedura remota.



| Attributo                         | Utilizzo                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**async**](async.md)            | Se applicato a un parametro di funzione, definisce un handle che consente al chiamante di effettuare una chiamata asincrona e di restituire immediatamente senza attendere i risultati e quindi di risincronizzare con la funzione chiamata per ricevere i dati al termine della chiamata. [**L'attributo async**](async.md) viene usato anche nei file ACF per definire un handle asincrono per una procedura o un'intera interfaccia. Per le interfacce COM, questa interfaccia è obsoleta e non può essere usata per le nuove interfacce. |
| [**async \_ uuid**](async-uuid.md) | Indica al compilatore MIDL di definire versioni sincrone e asincrone di un'interfaccia COM.                                                                                                                                                                                                                                                                                                                                                                                      |
| [**Forse**](maybe.md)            | Il client che effettua questa chiamata di procedura remota non prevede alcuna risposta che indica il recapito o il completamento della chiamata e il recapito non è garantito. Questo comportamento è in **contrasto con le operazioni** di messaggi in cui non è prevista alcuna risposta, ma il recapito è garantito.                                                                                                                                                                                                                    |
| [**Messaggio**](message.md)        | La chiamata di procedura remota deve essere considerata come un messaggio asincrono dal client al server. Il client effettua la chiamata e restituisce immediatamente , mentre la chiamata effettiva viene gestita dal trasporto di accodamento messaggi ([**ncadg \_ mq**](ncadg-mq.md)).                                                                                                                                                                                                                              |



 

 

 
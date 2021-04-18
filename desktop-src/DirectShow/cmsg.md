---
description: La classe CMsgThread fornisce supporto per un thread di lavoro al quale è possibile inviare le richieste in modo asincrono anziché essere inviate direttamente.
ms.assetid: 1cf159c9-80d0-4e3b-88d8-2ba4cd18e768
title: Classe CMsg
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsg
api_type:
- COM
api_location: ''
ms.openlocfilehash: a57a841b9c36a21895099c931acbf18a1e01ea0f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304124"
---
# <a name="cmsg-class"></a>Classe CMsg

La classe [**CMsgThread**](cmsgthread.md) fornisce supporto per un thread di lavoro al quale è possibile inviare le richieste in modo asincrono anziché essere inviate direttamente. La classe [**CAMThread**](camthread.md) fornisce un thread di lavoro a cui è possibile inviare singole richieste. Solo un client può effettuare una richiesta alla volta e il client si blocca fino a quando il thread di lavoro non ha completato la richiesta. Al contrario, la classe **CMsgThread** fornisce un thread di lavoro a cui è possibile inviare un numero qualsiasi di richieste. Le richieste (sotto forma di `CMsg` oggetto) vengono accodate ed eseguite in modo asincrono. Non viene ricevuto alcun valore restituito o di risposta.



| Membri dei dati              | Descrizione                                                                                                                                                                       |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dwFlags                   | Parametro del flag per il codice della richiesta.                                                                                                                                               |
| lpParam                   | Dati richiesti dal thread di lavoro come parametri o valori restituiti. Questi dati non devono essere basati su stack, in quanto verrà fatto riferimento a un po' di tempo dopo il completamento dell'operazione di Accodamento. |
| pEvent                    | Oggetto evento che un thread di lavoro può segnalare per indicare il completamento dell'operazione.                                                                                         |
| uMsg                      | Codice di richiesta definito dal client della classe thread e riconosciuto dalla funzione thread di lavoro sottoposta a override.                                                           |
| Funzioni di membro          | Descrizione                                                                                                                                                                       |
| [**CMsg**](cmsg-cmsg.md) | Costruisce un oggetto [**CMsg**](cmsg-cmsg.md) .                                                                                                                                    |



 

 

 




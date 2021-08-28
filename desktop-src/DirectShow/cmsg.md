---
description: La classe CMsgThread fornisce il supporto per un thread di lavoro a cui le richieste possono essere inviate in modo asincrono anziché direttamente.
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
ms.openlocfilehash: 36d5110cbeda8cbf19c97c3f83ca1431a2cd28c5a07fa70c09e51877e0906a0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016249"
---
# <a name="cmsg-class"></a>Classe CMsg

La [**classe CMsgThread**](cmsgthread.md) fornisce il supporto per un thread di lavoro a cui le richieste possono essere inviate in modo asincrono anziché direttamente. La [**classe CAMThread**](camthread.md) fornisce un thread di lavoro a cui è possibile inviare singole richieste. Solo un client può effettuare una richiesta alla volta e il client si blocca fino a quando il thread di lavoro non ha completato la richiesta. Al contrario, la **classe CMsgThread** fornisce un thread di lavoro in cui è possibile pubblicare un numero qualsiasi di richieste. Le richieste (sotto forma di oggetto) vengono `CMsg` accodati ed eseguiti in ordine, in modo asincrono. Non viene ricevuto alcun valore di risposta o restituito.



| Membri dei dati              | Descrizione                                                                                                                                                                       |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dwFlags                   | Contrassegnare il parametro nel codice della richiesta.                                                                                                                                               |
| lpParam                   | Dati richiesti dal thread di lavoro come parametri o valori restituiti. Questi dati non devono essere basati sullo stack, perché verranno referenziati qualche volta dopo il completamento dell'operazione di accodamento. |
| Pevent                    | Oggetto evento che un thread di lavoro può segnalare per indicare il completamento dell'operazione.                                                                                         |
| Umsg                      | Richiedere il codice definito dal client della classe di thread e riconosciuto dalla funzione del thread di lavoro sottoposta a override.                                                           |
| Funzioni di membro          | Descrizione                                                                                                                                                                       |
| [**CMsg**](cmsg-cmsg.md) | Costruisce un [**oggetto CMsg.**](cmsg-cmsg.md)                                                                                                                                    |



 

 

 




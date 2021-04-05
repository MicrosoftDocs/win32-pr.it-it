---
title: Attributi di chiamata di funzione
description: I programmi possono usare questi attributi sulle singole funzioni all'interno dell'interfaccia e influiscono solo su tale funzione.
ms.assetid: c54dbcd9-46c9-4755-b4a8-0f78068920b7
keywords:
- MIDL, attributi, chiamata di funzione IDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4d53407abf464d7b201c49d9cb2b1d3f3625b9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714083"
---
# <a name="function-call-attributes"></a>Attributi di chiamata di funzione

I programmi possono usare questi attributi sulle singole funzioni all'interno dell'interfaccia e influiscono solo su tale funzione.



| Attributo                        | Utilizzo                                                                                                                                                                                                                                                      |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Messaggio**](message.md)       | La chiamata di procedura remota deve essere considerata come un messaggio asincrono dal client al server. Il client effettua la chiamata e restituisce immediatamente un risultato, mentre la chiamata effettiva viene gestita dal trasporto di Accodamento messaggi ([**ncadg \_ mq**](ncadg-mq.md)). |
| [**Forse**](maybe.md)           | Il client che effettua questa chiamata di procedura remota non prevede alcuna risposta che indichi il recapito o il completamento della chiamata. Si differenziano dalle operazioni dei [**messaggi**](message.md) in cui non è prevista alcuna risposta, ma il recapito è garantito.        |
| [**trasmissione**](broadcast.md)   | La chiamata di procedura remota deve essere inviata a tutti i server della rete. Il client accetta il primo ritorno, le successive risposte degli altri server vengono scartate.                                                                                    |
| [**idempotent**](idempotent.md) | La chiamata non modifica lo stato e restituisce le stesse informazioni ogni volta che viene chiamato con gli stessi parametri di input.                                                                                                                                     |
| [**callback**](callback.md)     | Definisce una funzione che risiede nell'applicazione client, che il server può chiamare per ottenere informazioni dal client.                                                                                                                             |
| [**chiama \_ come**](call-as.md)      | Esegue il mapping di una funzione non a una chiamata di procedura remota.                                                                                                                                                                                                   |
| [**locale**](local.md)           | Definisce una procedura locale per la quale MIDL non genera codice stub.                                                                                                                                                                                   |



 

Sulle interfacce non [**oggetto**](object.md) , è anche possibile applicare l'attributo [**di \_ gestione del contesto**](context-handle.md) a una funzione per specificare le caratteristiche del valore restituito.

 

 





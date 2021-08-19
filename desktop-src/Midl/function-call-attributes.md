---
title: Attributi delle chiamate di funzione
description: I programmi possono usare questi attributi su singole funzioni all'interno dell'interfaccia e influiscono solo su tale funzione.
ms.assetid: c54dbcd9-46c9-4755-b4a8-0f78068920b7
keywords:
- IDL MIDL, attributi, chiamata di funzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a3800b62bb6b94aac330ecf0b06761d62227a4ed6100f2fabdde5b61cd952d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895311"
---
# <a name="function-call-attributes"></a>Attributi delle chiamate di funzione

I programmi possono usare questi attributi su singole funzioni all'interno dell'interfaccia e influiscono solo su tale funzione.



| Attributo                        | Utilizzo                                                                                                                                                                                                                                                      |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Messaggio**](message.md)       | La chiamata di procedura remota deve essere considerata come un messaggio asincrono dal client al server. Il client effettua la chiamata e restituisce immediatamente , mentre la chiamata effettiva viene gestita dal trasporto di accodamento messaggi ([**ncadg \_ mq**](ncadg-mq.md)). |
| [**Forse**](maybe.md)           | Il client che effettua questa chiamata di procedura remota non prevede alcuna risposta che indica il recapito o il completamento della chiamata. Questo comportamento è in [**contrasto con le operazioni**](message.md) di messaggi in cui non è prevista alcuna risposta, ma il recapito è garantito.        |
| [**Trasmissione**](broadcast.md)   | La chiamata di procedura remota deve essere inviata a tutti i server della rete. Il client accetta il primo valore restituito, le risposte successive da altri server vengono eliminate.                                                                                    |
| [**idempotent**](idempotent.md) | La chiamata non modifica lo stato e restituisce le stesse informazioni ogni volta che viene chiamata con gli stessi parametri di input.                                                                                                                                     |
| [**callback**](callback.md)     | Designa una funzione che risiede nell'applicazione client, che il server può chiamare per ottenere informazioni dal client.                                                                                                                             |
| [**call \_ as**](call-as.md)      | Mappe una funzione nonremobile a una chiamata di procedura remota.                                                                                                                                                                                                   |
| [**Locale**](local.md)           | Definisce una routine locale per la quale MIDL non genera codice stub.                                                                                                                                                                                   |



 

Nelle interfacce non [**oggetto**](object.md) è anche possibile applicare l'attributo [**\_ dell'handle**](context-handle.md) di contesto a una funzione per specificare le caratteristiche del valore restituito.

 

 





---
description: Ricezione di una risposta
ms.assetid: 48919608-a102-43e2-9ca0-80b17344b5eb
title: Ricezione di una risposta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e9e05ec392b7db828ad1efd1360c4d4fb232210
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524178"
---
# <a name="receiving-a-response"></a>Ricezione di una risposta

Poiché i componenti in coda sono progettati per funzionare in modo asincrono, le applicazioni client non devono bloccarsi in attesa di una risposta da una richiesta in coda. Tuttavia, è spesso utile per l'applicazione client o un'applicazione correlata nel computer client per ricevere una risposta alla fine. È ad esempio possibile che un client desideri ricevere una notifica quando una transazione richiesta è stata completata correttamente.

Esistono diversi modi in cui un componente in coda Invia una risposta al chiamante in modo asincrono. Ad esempio, potrebbe inviare un messaggio di posta elettronica. In alternativa, il server potrebbe pubblicare eventi a regime di controllo libero a cui il client può eseguire la sottoscrizione.

Un altro modo per ottenere una risposta da un componente in coda eseguito su un server è che il client passi il metodo chiamato un oggetto notifica. Un oggetto notifica è un'istanza di un componente in coda eseguito nel client. Un oggetto di notifica di questo tipo potrebbe essere piuttosto semplice, che contiene solo un numero intero usato per rappresentare un valore di errore o potrebbe essere piuttosto complesso, che contiene tutte le informazioni necessarie per eseguire il rollback di una transazione nel client. In entrambi i casi, il client chiamante passa un oggetto notifica come parametro di input quando si desidera una risposta da un componente in coda eseguito in un server. Poiché l'oggetto notifica viene accodato, il server può chiamare sui relativi metodi per modificarne lo stato, che può essere successivamente letto dal client. In questo scenario, il servizio componenti in coda COM+ viene utilizzato sia sul client che sul server per consentire la comunicazione asincrona in entrambe le direzioni.

 

 




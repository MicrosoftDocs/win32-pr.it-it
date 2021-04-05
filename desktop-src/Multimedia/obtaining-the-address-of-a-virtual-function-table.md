---
title: Acquisizione dell'indirizzo di una tabella di funzioni virtuali
description: Acquisizione dell'indirizzo di una tabella di funzioni virtuali
ms.assetid: c9e9e2df-75e6-4684-a465-6905e76b10a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c0d618e75d2c3a4fcc2550fca7cb90bd2a51d2f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515727"
---
# <a name="obtaining-the-address-of-a-virtual-function-table"></a>Acquisizione dell'indirizzo di una tabella di funzioni virtuali

In un'applicazione scritta nel linguaggio di programmazione C, è possibile recuperare l'indirizzo della struttura **IAVIStreamVtbl** utilizzando la funzione NewBall. Questa funzione restituisce l'indirizzo di una struttura contenente un puntatore a **IAVIStreamVtbl**. Le informazioni che seguono il puntatore **IAVIStreamVtbl** specificano i dati usati internamente da AVIBall. Il gestore del flusso può aggiungere le proprie informazioni dopo il puntatore **IAVIStreamVtbl** . Queste informazioni vengono restituite nelle chiamate successive al gestore del flusso.


```C++
PAVISTREAM WINAPI NewBall(VOID) 
{ 
    PAVIBALL pball; 
    pball = (PAVIBALL) GlobalAllocPtr(GHND, sizeof(AVIBALL)); 
    if (!pball) 
        return 0; 
    pball->lpvtbl = &AVIBallHandler; 
    pball->lpvtbl->Create((PAVISTREAM) pball, 0, 0); 
    return (PAVISTREAM) pball; 
} 
```



 

 





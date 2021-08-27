---
title: Recupero dell'indirizzo di una tabella di funzioni virtuali
description: Recupero dell'indirizzo di una tabella di funzioni virtuali
ms.assetid: c9e9e2df-75e6-4684-a465-6905e76b10a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39a0fbf941114cfff2b930ed329f7a35962b9ef07158fd5fda16a19a73c0f692
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038431"
---
# <a name="obtaining-the-address-of-a-virtual-function-table"></a>Recupero dell'indirizzo di una tabella di funzioni virtuali

In un'applicazione scritta nel linguaggio di programmazione C è possibile recuperare l'indirizzo della **struttura IAVIStreamVtbl** usando la funzione NewBall. Questa funzione restituisce l'indirizzo di una struttura contenente un puntatore a **IAVIStreamVtbl**. Le informazioni che **segue il puntatore IAVIStreamVtbl** specificano i dati usati internamente da AVIBall. Il gestore del flusso può aggiungere le proprie informazioni dopo il **puntatore IAVIStreamVtbl.** Queste informazioni vengono restituite nelle chiamate successive al gestore del flusso.


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



 

 





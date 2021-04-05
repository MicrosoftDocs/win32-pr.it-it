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
# <a name="obtaining-the-address-of-a-virtual-function-table"></a><span data-ttu-id="2565a-103">Acquisizione dell'indirizzo di una tabella di funzioni virtuali</span><span class="sxs-lookup"><span data-stu-id="2565a-103">Obtaining the Address of a Virtual Function Table</span></span>

<span data-ttu-id="2565a-104">In un'applicazione scritta nel linguaggio di programmazione C, è possibile recuperare l'indirizzo della struttura **IAVIStreamVtbl** utilizzando la funzione NewBall.</span><span class="sxs-lookup"><span data-stu-id="2565a-104">In an application written in the C programming language, you can retrieve the address of the **IAVIStreamVtbl** structure by using the NewBall function.</span></span> <span data-ttu-id="2565a-105">Questa funzione restituisce l'indirizzo di una struttura contenente un puntatore a **IAVIStreamVtbl**.</span><span class="sxs-lookup"><span data-stu-id="2565a-105">This function returns the address of a structure containing a pointer to **IAVIStreamVtbl**.</span></span> <span data-ttu-id="2565a-106">Le informazioni che seguono il puntatore **IAVIStreamVtbl** specificano i dati usati internamente da AVIBall.</span><span class="sxs-lookup"><span data-stu-id="2565a-106">Information following the **IAVIStreamVtbl** pointer specifies data used internally by AVIBall.</span></span> <span data-ttu-id="2565a-107">Il gestore del flusso può aggiungere le proprie informazioni dopo il puntatore **IAVIStreamVtbl** .</span><span class="sxs-lookup"><span data-stu-id="2565a-107">Your stream handler can append its own information after the **IAVIStreamVtbl** pointer.</span></span> <span data-ttu-id="2565a-108">Queste informazioni vengono restituite nelle chiamate successive al gestore del flusso.</span><span class="sxs-lookup"><span data-stu-id="2565a-108">This information is returned in subsequent calls to your stream handler.</span></span>


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



 

 





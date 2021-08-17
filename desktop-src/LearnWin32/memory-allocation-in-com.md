---
title: Allocazione di memoria in COM
description: Allocazione di memoria in COM
ms.assetid: b3c318d2-1273-430e-8aca-5bd5c95c138e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a38477f0db860cf768493417470f2da3395e814bc106cf85f975ed11ba2c0b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979981"
---
# <a name="memory-allocation-in-com"></a>Allocazione di memoria in COM

In alcuni casi un metodo alloca un buffer di memoria nell'heap e restituisce l'indirizzo del buffer al chiamante. COM definisce una coppia di funzioni per l'allocazione e il liberare memoria nell'heap.

-   La [**funzione CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) alloca un blocco di memoria.
-   La [**funzione CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) libera un blocco di memoria allocato con [**CoTaskMemAlloc.**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc)

È stato illustrato un esempio di questo modello [nell'esempio della finestra di dialogo Apri](example--the-open-dialog-box.md):


```C++
PWSTR pszFilePath;
hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);
if (SUCCEEDED(hr))
{
    // ...
    CoTaskMemFree(pszFilePath);
}
```



Il [**metodo GetDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) alloca memoria per una stringa. Internamente, il metodo chiama [**CoTaskMemAlloc per**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) allocare la stringa. Quando il metodo viene restituito, *pszFilePath* punta alla posizione di memoria del nuovo buffer. Il chiamante è responsabile della chiamata [**a CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) per liberare la memoria.

Perché COM definisce le proprie funzioni di allocazione della memoria? Uno dei motivi è fornire un livello di astrazione sull'allocatore dell'heap. In caso contrario, alcuni metodi potrebbero chiamare **malloc,** mentre altri potrebbero **chiamare new**. Il programma dovrà quindi chiamare **gratuitamente** in alcuni casi ed eliminare **in** altri e tenere traccia di tutto diventa rapidamente impossibile. Le funzioni di allocazione COM creano un approccio uniforme.

Un'altra considerazione è il fatto che COM è *uno* standard binario, quindi non è associato a un particolare linguaggio di programmazione. Di conseguenza, COM non può basarsi su qualsiasi forma specifica del linguaggio di allocazione di memoria.

## <a name="next"></a>Prossima

[Procedure di scrittura del codice COM](com-coding-practices.md)

 

 

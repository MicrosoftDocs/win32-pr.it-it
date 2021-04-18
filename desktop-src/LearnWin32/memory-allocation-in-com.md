---
title: Allocazione di memoria in COM
description: .
ms.assetid: b3c318d2-1273-430e-8aca-5bd5c95c138e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62227f78287f184b019eee3e498ec8a25f25a03c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299780"
---
# <a name="memory-allocation-in-com"></a>Allocazione di memoria in COM

Talvolta un metodo alloca un buffer di memoria nell'heap e restituisce l'indirizzo del buffer al chiamante. COM definisce una coppia di funzioni per l'allocazione e la liberazione della memoria nell'heap.

-   La funzione [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) alloca un blocco di memoria.
-   La funzione [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) libera un blocco di memoria allocato con [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc).

Un esempio di questo modello è stato visualizzato nell'esempio di finestra di [dialogo Apri](example--the-open-dialog-box.md):


```C++
PWSTR pszFilePath;
hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);
if (SUCCEEDED(hr))
{
    // ...
    CoTaskMemFree(pszFilePath);
}
```



Il metodo [**GetDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) alloca memoria per una stringa. Internamente, il metodo chiama [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) per allocare la stringa. Quando il metodo restituisce un risultato, *pszFilePath* punta alla posizione di memoria del nuovo buffer. Il chiamante è responsabile della chiamata a [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) per liberare la memoria.

Perché COM definisce le proprie funzioni di allocazione della memoria? Uno dei motivi consiste nel fornire un livello di astrazione sull'allocatore dell'heap. In caso contrario, alcuni metodi potrebbero chiamare **malloc** mentre altri chiamano **nuovo**. Il programma dovrebbe quindi chiamare **Free** in alcuni casi ed **eliminarlo** in altri e tenerne traccia, che diventerà rapidamente impossibile. Le funzioni di allocazione COM creano un approccio uniforme.

Un'altra considerazione è il fatto che COM è uno standard *binario* , quindi non è associato a un particolare linguaggio di programmazione. Pertanto, COM non può basarsi su alcuna forma di allocazione di memoria specifica del linguaggio.

## <a name="next"></a>Prossima

[Procedure di codifica COM](com-coding-practices.md)

 

 
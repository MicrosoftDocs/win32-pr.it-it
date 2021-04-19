---
title: IAgentCharacterEx GetAnimationNames
description: IAgentCharacterEx GetAnimationNames
ms.assetid: d565b258-dc12-422b-a13d-aeec56057f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e31dcb7ea34a9f0d833f8c1665a092fe4f3a30e7
ms.sourcegitcommit: baa7cd1709e48672f5f07ff83a9c9d5699c0efcd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/14/2021
ms.locfileid: "106320062"
---
# <a name="iagentcharacterexgetanimationnames"></a>IAgentCharacterEx::GetAnimationNames

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetAnimationNames(
   IUnknown ** punkEnum // address of IUnknown interface
);
```

Recupera i nomi di animazione per un carattere.

-   Restituisce **\_ OK** per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*
</dt> <dd>

Indirizzo dell'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) per la raccolta di animazioni del carattere.

</dd> </dl>

Questa funzione consente di enumerare i nomi delle animazioni per un carattere. Gli elementi della raccolta non hanno proprietà, quindi non è possibile accedere direttamente a singoli elementi. Per accedere alla raccolta, eseguire una query su punkEnum per l'interfaccia IEnumVARIANT:


```c++
IEnumVARIANT pEnum;
VARIANT vAnimName;
DWORD dwRetrieved;

hRes = punkEnum->QueryInterface(IID_IEnumVARIANT, (LPVOID *)&pEnum);

if (SUCCEEDED(hRes)) {

    while (TRUE) {

         hRes = pEnum->Next(1, &vAnimName, &dwRetrieved);

         if (hRes != NOERROR)
            break;

         // vAnimName.bstrVal is the animation name

         VariantClear(&vAnimName);
    } 

    pEnum->Release();
}

punkEnum->Release();
```



> [!Note]  
> Per i caratteri ACF, la raccolta restituisce tutte le animazioni definite per il carattere, aggiungendo quelle che sono state recuperate con il metodo [**Get**](https://www.bing.com/search?q=**Get**) .

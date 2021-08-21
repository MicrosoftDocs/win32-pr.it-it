---
title: IAgentCharacterEx GetAnimationNames
description: IAgentCharacterEx GetAnimationNames
ms.assetid: d565b258-dc12-422b-a13d-aeec56057f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c9cb1bc1b51b0bead2f071e0cd8561ef055ef6b7eb7986b3be969208452331
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478029"
---
# <a name="iagentcharacterexgetanimationnames"></a>IAgentCharacterEx::GetAnimationNames

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetAnimationNames(
   IUnknown ** punkEnum // address of IUnknown interface
);
```

Recupera i nomi delle animazioni per un carattere.

-   Restituisce **S \_ OK** per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*Iunknown*
</dt> <dd>

Indirizzo [**dell'interfaccia IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) per la raccolta di animazioni del carattere.

</dd> </dl>

Questa funzione consente di enumerare i nomi delle animazioni per un carattere. Gli elementi nella raccolta non hanno proprietà, pertanto non è possibile accedere direttamente ai singoli elementi. Per accedere alla raccolta, eseguire una query su punkEnum per l'interfaccia IEnumVARIANT:


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
> Per i caratteri ACF, la raccolta restituisce tutte le animazioni definite per il carattere, aggiungendo a quelle recuperate con il [**metodo Get.**](https://www.bing.com/search?q=**Get**)

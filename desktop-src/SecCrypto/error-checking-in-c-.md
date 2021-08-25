---
description: In C++, ogni metodo di Servizi certificati restituisce direttamente un valore HRESULT che indica se la chiamata al metodo ha avuto esito positivo o negativo. Se la chiamata non è riuscita, il valore restituito indica il motivo per cui non è riuscita.
ms.assetid: 4ab1b5ba-dd19-4802-aa9c-02bd5406681f
title: Controllo degli errori in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc3e374c6f0bd933c2e4de7a477fea02b4e1538a7a1fa9b4de78e45fd896b192
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874071"
---
# <a name="error-checking-in-c"></a>Controllo degli errori in C++

In C++, ogni metodo di Servizi certificati restituisce direttamente un **valore HRESULT** che indica se la chiamata al metodo ha avuto esito positivo o negativo. Se la chiamata non è riuscita, il valore restituito indica il motivo per cui non è riuscita.

Nell'esempio seguente viene illustrato come usare i valori **HRESULT** restituiti per il controllo degli errori. Per codici di errore di esempio, vedere [Valori HRESULT comuni](common-hresult-values.md).


```C++
HRESULT hr;
BSTR strAttributeName;
BSTR strAttributeValue = NULL;

if(!(strAttributeName = SysAllocString(L"TheAttribute")))
{
     printf("Could not allocate memory for attribute name.\n");
     exit(1);
}

hr = pICertServerPolicy->GetRequestAttribute(
                                strAttributeName,
                                &strAttributeValue);
if(S_OK != hr)          // Check to determine whether method failed
{
    if (E_INVALIDARG == hr)
    {
        //... Do something to recover from errors and so on.
    }
}
// Free BSTRs when finished.
if (NULL != strAttributeName)
    SysFreeString(strAttributeName);
if (NULL != strAttributeValue)
    SysFreeString(strAttributeValue);
```



 

 




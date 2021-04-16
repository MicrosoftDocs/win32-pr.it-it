---
description: In C++, ogni metodo di Servizi certificati restituisce direttamente un valore HRESULT che indica se la chiamata al metodo ha avuto esito positivo o negativo. Se la chiamata ha esito negativo, il valore restituito indica il motivo per cui non è riuscito.
ms.assetid: 4ab1b5ba-dd19-4802-aa9c-02bd5406681f
title: Controllo degli errori in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f2a56acd41269ece0f9a5c7de4a2dff1960bb10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528717"
---
# <a name="error-checking-in-c"></a>Controllo degli errori in C++

In C++, ogni metodo di Servizi certificati restituisce direttamente un valore **HRESULT** che indica se la chiamata al metodo ha avuto esito positivo o negativo. Se la chiamata ha esito negativo, il valore restituito indica il motivo per cui non è riuscito.

Nell'esempio seguente viene illustrato come è possibile utilizzare i valori **HRESULT** restituiti per il controllo degli errori. Per i codici di errore di esempio, vedere [valori HRESULT comuni](common-hresult-values.md).


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



 

 




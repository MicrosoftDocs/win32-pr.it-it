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
# <a name="error-checking-in-c"></a><span data-ttu-id="8beaa-104">Controllo degli errori in C++</span><span class="sxs-lookup"><span data-stu-id="8beaa-104">Error Checking in C++</span></span>

<span data-ttu-id="8beaa-105">In C++, ogni metodo di Servizi certificati restituisce direttamente un valore **HRESULT** che indica se la chiamata al metodo ha avuto esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="8beaa-105">In C++, every Certificate Services method directly returns an **HRESULT** value that indicates whether the method call succeeded or failed.</span></span> <span data-ttu-id="8beaa-106">Se la chiamata ha esito negativo, il valore restituito indica il motivo per cui non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="8beaa-106">If the call failed, the return value indicates why it failed.</span></span>

<span data-ttu-id="8beaa-107">Nell'esempio seguente viene illustrato come è possibile utilizzare i valori **HRESULT** restituiti per il controllo degli errori.</span><span class="sxs-lookup"><span data-stu-id="8beaa-107">The following example shows how the returned **HRESULT** values can be used for error checking.</span></span> <span data-ttu-id="8beaa-108">Per i codici di errore di esempio, vedere [valori HRESULT comuni](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="8beaa-108">For example error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>


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



 

 




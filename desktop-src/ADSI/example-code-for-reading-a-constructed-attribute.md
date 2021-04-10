---
title: Codice di esempio per la lettura di un attributo costruito
description: Questo argomento contiene esempi di codice VB e C++ che illustrano come leggere un attributo costruito.
ms.assetid: c4acc848-f89e-4cd1-905a-2ed20443b03c
ms.tgt_platform: multiple
keywords:
- Codice di esempio per la lettura di un attributo costruito ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb69bf99807d87e711d0d54d2c5b228d304149e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855309"
---
# <a name="example-code-for-reading-a-constructed-attribute"></a><span data-ttu-id="285dc-104">Codice di esempio per la lettura di un attributo costruito</span><span class="sxs-lookup"><span data-stu-id="285dc-104">Example Code for Reading a Constructed Attribute</span></span>

<span data-ttu-id="285dc-105">Nell'esempio di codice riportato di seguito viene illustrato un metodo che può essere utilizzato per recuperare un valore di attributo che funzionerà con tutti i tipi di attributi.</span><span class="sxs-lookup"><span data-stu-id="285dc-105">The following code example shows a method that can be used to retrieve an attribute value that will work with all attributes types.</span></span>


```VB
Public Function GetAttribute(oObject As IADs, AttributeName As String) As String
    Const E_ADS_PROPERTY_NOT_FOUND = &H8000500D
    
    On Error Resume Next
    
    ' Attempt to get the attribute value.
    GetAttribute = oObject.Get(AttributeName)
    If (Err.Number = E_ADS_PROPERTY_NOT_FOUND) Then
        ' Reset the error number.
        Err.Number = 0
        
        ' Use IADs.GetInfoEx to explicitly load the attribute value into the cache.
        oObject.GetInfoEx Array(AttributeName), 0
        If Err.Number = 0 Then
            ' Attempt to get the attribute value.
            GetAttribute = oObject.Get(AttributeName)
        End If
    End If
End Function
```



<span data-ttu-id="285dc-106">Nell'esempio di codice riportato di seguito viene illustrato un metodo che può essere utilizzato per recuperare un valore di attributo che funzionerà con tutti i tipi di attributi.</span><span class="sxs-lookup"><span data-stu-id="285dc-106">The following code example shows a method that can be used to retrieve an attribute value that will work with all attributes types.</span></span>


```C++
/***************************************************************************

    GetAttribute()

***************************************************************************/

HRESULT GetAttribute(IADs *pads, BSTR bstrAttribute, VARIANT *pvar)
{
    if(!pads || !pvar)
    {
        return E_INVALIDARG;
    }

    HRESULT hr;
    CComVariant svar;

    // Attempt to get the attribute with IADs.Get.
    hr = pads->Get(bstrAttribute, &svar);
    if(E_ADS_PROPERTY_NOT_FOUND  == hr)
    {
        // Attempt to get the attribute with IADs.GetInfoEx and then IADs.Get.

        CComVariant svarArray;
        hr = ADsBuildVarArrayStr(&(LPWSTR)bstrAttribute, 1, &svarArray);
        if (SUCCEEDED(hr))
        {
            hr = pads->GetInfoEx(svarArray, 0L);
            if(SUCCEEDED(hr))
            {
                hr = pads->Get(bstrAttribute, &svar);
            }
        }

    }

    if(S_OK == hr)
    {
        hr = svar.Detach(pvar);
    }

    return hr;
}
```



 

 





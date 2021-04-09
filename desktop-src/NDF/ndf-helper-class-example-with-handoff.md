---
title: Estensione della classe helper NDF con la consegna
description: Questa classe helper presenta una dipendenza di basso livello di integrità in SimpleFileHelperClass codificata nel primo esempio.
ms.assetid: b59cd855-c68a-4f5c-b145-ceac395ddcc4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b799b795fcf23cbddf268056e23db433566c8a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955462"
---
# <a name="ndf-helper-class-extension-with-handoff"></a>Estensione della classe helper NDF con la consegna

Questa classe helper presenta una dipendenza di basso livello di integrità in SimpleFileHelperClass codificata nel primo esempio.

La seconda classe helper di continuità è una semplice classe helper pass-through che non esegue alcuna diagnosi. Ma genera sempre una ipotesi di integrità più bassa per la SimpleFileHelperClass. Questo è utile per fungere da segnaposto per l'aggiunta futura della funzionalità di diagnostica in questa classe helper. La classe helper uniforme implementa due metodi.

Il metodo LowHealth viene usato per impostare lo stato di diagnosi su DS \_ indeterminato. Questo fa in modo che NDF chiami GetLowerHypotheses.


```C++
#include <windows.h>

HRESULT HandOffTestHelperClass::LowHealth( 
    /* [unique][string][in] */ LPCWSTR pwszInstanceDescription,
    /* [string][out] */ LPWSTR *ppwszDescription,
    /* [out] */ long *pDeferredTime,
    /* [out] */ DIAGNOSIS_STATUS *pStatus) 

{
    *pStatus = DS_INDETERMINATE;
    return S_OK;
}

```



Successivamente, GetLowerHypotheses viene implementato per indicare a NDF la classe helper da diagnosticare.


```C++
#include <windows.h>

HRESULT HandOffTestHelperClass::GetLowerHypotheses( 
ULONG *Count,
HYPOTHESIS **Hypotheses)
{
    HRESULT hr = S_OK;
    HYPOTHESIS *pHypothesis=NULL;
    HELPER_ATTRIBUTE *pAttr=NULL;

    pHypothesis = (PHYPOTHESIS)CoTaskMemAlloc(sizeof(HYPOTHESIS));
    if (pHypothesis == NULL)
    {
        return E_OUTOFMEMORY;
    }
    SecureZeroMemory(pHypothesis, sizeof(HYPOTHESIS));

    pAttr = (PHELPER_ATTRIBUTE)CoTaskMemAlloc(sizeof(HELPER_ATTRIBUTE));
    if (pAttr  == NULL)
    {
       hr = E_OUTOFMEMORY;
       goto Error;
    }
    SecureZeroMemory(pAttr, sizeof(HELPER_ATTRIBUTE));

    //set the helper class name to hand off to
    hr = StringCchCopyWithAlloc(&pHypothesis->pwszClassName, MAX_PATH,
                 L"SimpleFileHelperClass");
    if (FAILED(hr))
    {
        goto Error;
    }

    //populate the attribute
    //set the attribute name
    hr = StringCchCopyWithAlloc(&pAttr->pwszName, MAX_PATH, L"filename");
    if (FAILED(hr))
    {
        goto Error;  
    }

    //set attribute data
    pAttr->type = AT_STRING;
    hr = StringCchCopyWithAlloc(&pAttr->PWStr, MAX_PATH, m_pwszTestFile);
    if (FAILED(hr))
    {
        goto Error;
    }

    //set the attributes to the hypothesis  
    pHypothesis->celt = 1; //number of attributes
    pHypothesis->rgAttributes=pAttr;

    //pass data back
    *pcelt = 1; //one hypothesis
    *pprgHypotheses = pHypothesis;

    return S_OK;

Error:

    if (pAttr)
    {
        if (pAttr->PWStr) 
            CoTaskMemFree(pAttr->PWStr);
        if (pAttr->pwszName) 
            CoTaskMemFree(pAttr->pwszName);
    }

    if (pHypothesis)
    {
        if (pHypothesis->pwszClassName) 
            CoTaskMemFree(pHypothesis->pwszClassName);
        CoTaskMemFree(pHypothesis);
    }
    return hr;
}

```



 

 





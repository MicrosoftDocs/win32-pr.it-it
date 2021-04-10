---
description: In C++, il valore restituito è in genere di tipo HRESULT.
ms.assetid: 7abf1b3e-b94b-4846-a813-5eab5b34324c
title: Valori restituiti in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff7a5417019468945054f24701636fcece1d3d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227489"
---
# <a name="return-values-in-c"></a>Valori restituiti in C++

In C++, il valore restituito è in genere di tipo **HRESULT**. Da questo valore restituito è possibile determinare se il metodo è riuscito o meno e, in caso contrario, qual è l'errore. Servizi certificati in genere restituisce \_ OK per **HRESULT** quando il metodo è stato completato correttamente. I valori a livello di codice che devono essere restituiti vengono restituiti tramite parametri "out" nel metodo. Nell'esempio seguente viene illustrata una chiamata al metodo C++ per recuperare una proprietà della richiesta:


```C++
BSTR      bstrPropName = NULL;
VARIANT   varProp;
HRESULT   hr;

VariantInit(&varProp);

bstrPropName = SysAllocString(L"RequestID");
if (NULL == bstrPropName)
{
    printf("Failed SysAllocString\n");
    // Take application-specific error action.
    exit(1);
}

// Retrieve the request property.
// pCertServerPolicy is a pointer to a previously
// instantiated ICertServerPolicy object.
hr = pCertServerPolicy->GetRequestProperty(bstrPropName,
                                           PROPTYPE_LONG,
                                           &varProp);
if (S_OK != hr)
{
    printf("Failed GetRequestProperty [%x]\n", hr);
    // Take application-specific error action.
    // ...
}
else
{
    // Successfully retrieved property; use varProp as needed.
    // ...
}

// Done processing.
VariantClear(&varProp);
if (NULL != bstrPropName)
    SysFreeString(bstrPropName);
```



Nel frammento di codice precedente, la funzione Success o Failure viene restituita alla variabile **HRESULT** *HR*. È necessario controllare la variabile **HRESULT** per l'esito positivo del \[ codice gestito nel codice dalla condizione (S \_ OK! = HR) \] . Se il metodo viene completato correttamente, il valore della proprietà Request viene restituito nel parametro **Variant** *varProp* .

 

 




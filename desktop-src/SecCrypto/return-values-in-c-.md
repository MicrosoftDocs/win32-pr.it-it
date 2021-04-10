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
# <a name="return-values-in-c"></a><span data-ttu-id="43946-103">Valori restituiti in C++</span><span class="sxs-lookup"><span data-stu-id="43946-103">Return Values in C++</span></span>

<span data-ttu-id="43946-104">In C++, il valore restituito è in genere di tipo **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="43946-104">In C++, the return value is typically of type **HRESULT**.</span></span> <span data-ttu-id="43946-105">Da questo valore restituito è possibile determinare se il metodo è riuscito o meno e, in caso contrario, qual è l'errore.</span><span class="sxs-lookup"><span data-stu-id="43946-105">It is from this return value that it can be determined whether the method succeeded or not, and if not, what the error was.</span></span> <span data-ttu-id="43946-106">Servizi certificati in genere restituisce \_ OK per **HRESULT** quando il metodo è stato completato correttamente.</span><span class="sxs-lookup"><span data-stu-id="43946-106">Certificate Services typically returns S\_OK for the **HRESULT** when the method has completed successfully.</span></span> <span data-ttu-id="43946-107">I valori a livello di codice che devono essere restituiti vengono restituiti tramite parametri "out" nel metodo.</span><span class="sxs-lookup"><span data-stu-id="43946-107">Programmatic values that need to be returned are returned through "out" parameters in the method.</span></span> <span data-ttu-id="43946-108">Nell'esempio seguente viene illustrata una chiamata al metodo C++ per recuperare una proprietà della richiesta:</span><span class="sxs-lookup"><span data-stu-id="43946-108">The following example shows a C++ method call to retrieve a request property:</span></span>


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



<span data-ttu-id="43946-109">Nel frammento di codice precedente, la funzione Success o Failure viene restituita alla variabile **HRESULT** *HR*.</span><span class="sxs-lookup"><span data-stu-id="43946-109">In the preceding code fragment, success or failure is returned to the **HRESULT** variable, *hr*.</span></span> <span data-ttu-id="43946-110">È necessario controllare la variabile **HRESULT** per l'esito positivo del \[ codice gestito nel codice dalla condizione (S \_ OK! = HR) \] .</span><span class="sxs-lookup"><span data-stu-id="43946-110">It is imperative to check the **HRESULT** variable for success \[handled in the code by the condition (S\_OK != hr)\].</span></span> <span data-ttu-id="43946-111">Se il metodo viene completato correttamente, il valore della proprietà Request viene restituito nel parametro **Variant** *varProp* .</span><span class="sxs-lookup"><span data-stu-id="43946-111">If the method completed successfully, the request property value is returned in the **VARIANT** *varProp* parameter.</span></span>

 

 




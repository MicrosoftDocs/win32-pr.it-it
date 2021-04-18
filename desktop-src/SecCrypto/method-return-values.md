---
description: Il valore restituito per i metodi dell'interfaccia C++ è sempre di tipo HRESULT; Questo valore può essere controllato per determinare l'esito positivo o negativo.
ms.assetid: f6478e72-0fe9-4c3b-b08a-f71c9c943910
title: Valori restituiti dal metodo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3871cf00bd48c7fbe1432ec86b503fba7795592
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307690"
---
# <a name="method-return-values"></a><span data-ttu-id="84d6f-103">Valori restituiti dal metodo</span><span class="sxs-lookup"><span data-stu-id="84d6f-103">Method Return Values</span></span>

<span data-ttu-id="84d6f-104">Il valore restituito per i metodi dell'interfaccia C++ è sempre di tipo **HRESULT**; Questo valore può essere controllato per determinare l'esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="84d6f-104">The return value for C++ interface methods is always of type **HRESULT**; this value can be checked to determine success or failure.</span></span> <span data-ttu-id="84d6f-105">L'uso dei parametri "output" consente l'assegnazione di valori alle variabili durante la chiamata al metodo o alla proprietà.</span><span class="sxs-lookup"><span data-stu-id="84d6f-105">The use of "output" parameters allows values to be assigned to variables during the method or property call.</span></span> <span data-ttu-id="84d6f-106">Nell'esempio seguente viene illustrata una chiamata al metodo C++ per enumerare i provider.</span><span class="sxs-lookup"><span data-stu-id="84d6f-106">The following example shows a C++ method call to enumerate providers.</span></span>


```C++
UINT          ucEnumProvIndex = 0;
BSTR          bstrProvider = NULL;
HRESULT       hr;

// pEnroll is previously instantiated CEnroll interface pointer
hr = pEnroll->enumProviders(ucEnumProvIndex, 0, &bstrProvider);
```



<span data-ttu-id="84d6f-107">Nel frammento di codice precedente, l'esito positivo o negativo viene restituito alla variabile "HR".</span><span class="sxs-lookup"><span data-stu-id="84d6f-107">In the preceding code fragment, success or failure is returned to the "hr" variable.</span></span> <span data-ttu-id="84d6f-108">Se la chiamata ha esito positivo, HR verrà impostato su S \_ OK e la variabile bstrProvider conterrà il nome del provider enumerato.</span><span class="sxs-lookup"><span data-stu-id="84d6f-108">If the call was successful, hr will be set to S\_OK and the variable bstrProvider will contain the name of the enumerated provider.</span></span>

<span data-ttu-id="84d6f-109">Una chiamata C++ per recuperare il valore di una proprietà è la seguente.</span><span class="sxs-lookup"><span data-stu-id="84d6f-109">A C++ call to retrieve a property value would be as follows.</span></span>


```C++
BSTR     bstrStoreName = NULL;
HRESULT  hr;

// pEnroll is previously instantiated CEnroll interface pointer

// get the storename
hr = pEnroll->get_CAStoreName( &bstrStoreName );

// (When done using bstrStoreName, free it by calling SysFreeString).
```



<span data-ttu-id="84d6f-110">Una chiamata C++ per impostare un valore della proprietà sarà come segue.</span><span class="sxs-lookup"><span data-stu-id="84d6f-110">A C++ call to set a property value would be as follows.</span></span>


```C++
// bstrNewName previously set to a valid store name
hr = pEnroll->put_CAStoreName( bstrNewName );
```



 

 




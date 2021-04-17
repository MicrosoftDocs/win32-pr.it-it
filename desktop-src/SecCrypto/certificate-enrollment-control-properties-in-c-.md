---
description: Restituisce un valore HRESULT. In questo HRESULT, un valore di S \_ OK indica che il metodo è stato eseguito correttamente.
ms.assetid: 6722a74a-1ec1-4c71-84c6-fb103aca149f
title: Proprietà del controllo di registrazione certificati in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76525f26f318178f122cc0feee6221bbd948bba0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525831"
---
# <a name="certificate-enrollment-control-properties-in-c"></a><span data-ttu-id="7c35d-104">Proprietà del controllo di registrazione certificati in C++</span><span class="sxs-lookup"><span data-stu-id="7c35d-104">Certificate Enrollment Control Properties in C++</span></span>

<span data-ttu-id="7c35d-105">Quando si imposta o Recupera una proprietà del controllo di registrazione certificati in C++, la chiamata al metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="7c35d-105">When you set or retrieve a Certificate Enrollment Control property in C++, the method call returns an **HRESULT**.</span></span> <span data-ttu-id="7c35d-106">In questo **HRESULT**, un valore di S \_ OK indica che il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="7c35d-106">In this an **HRESULT**, a value of S\_OK indicates that the method was successfully executed.</span></span>

<span data-ttu-id="7c35d-107">I programmi scritti in C++ possono recuperare le proprietà del controllo di registrazione certificati per chiamate al metodo nel formato seguente.</span><span class="sxs-lookup"><span data-stu-id="7c35d-107">Programs written in C++ can retrieve the Certificate Enrollment Control properties by method calls in the following form.</span></span>


```C++
#include <windows.h>

HRESULT get_propertyName( datatype * pPropValue);
```



<span data-ttu-id="7c35d-108">Dove *PropertyName* specifica il nome della proprietà a cui si accede e *pPropValue* è un puntatore a una variabile con il tipo di dati appropriato.</span><span class="sxs-lookup"><span data-stu-id="7c35d-108">Where *propertyName* specifies the name of the property being accessed, and *pPropValue* is a pointer to a variable of the appropriate data type.</span></span> <span data-ttu-id="7c35d-109">Al termine di questa chiamata al metodo, *pPropValue* punterà alla variabile che contiene il valore della proprietà *PropertyName* .</span><span class="sxs-lookup"><span data-stu-id="7c35d-109">After successful completion of this method call, *pPropValue* will point to the variable that contains the value of the *propertyName* property.</span></span>

<span data-ttu-id="7c35d-110">Ad esempio, per recuperare il valore per la proprietà **RootStoreType** , usare il codice seguente.</span><span class="sxs-lookup"><span data-stu-id="7c35d-110">For example, to retrieve the value for the **RootStoreType** property, you use the following code.</span></span>


```C++
// Get the store type.
// hr is an HRESULT.
// bstrStoreType is a BSTR variable.
hr = pEnroll->get_RootStoreType( &bstrStoreType );
```



<span data-ttu-id="7c35d-111">I programmi scritti in C++ possono impostare le proprietà del controllo di registrazione dei certificati chiamando i metodi nel formato seguente.</span><span class="sxs-lookup"><span data-stu-id="7c35d-111">Programs written in C++ can set the Certificate Enrollment Control properties by calling methods in the following form.</span></span>


```C++
#include <windows.h>

HRESULT put_propertyName( datatype PropValue);
```



<span data-ttu-id="7c35d-112">Dove *PropertyName* specifica il nome della proprietà a cui si accede e *PropValue* è un valore del tipo di dati appropriato.</span><span class="sxs-lookup"><span data-stu-id="7c35d-112">Where *propertyName* specifies the name of the property being accessed, and *PropValue* is a value of the appropriate data type.</span></span> <span data-ttu-id="7c35d-113">Al termine di questa chiamata al metodo, il nuovo valore della proprietà *PropertyName* sarà *PropValue*.</span><span class="sxs-lookup"><span data-stu-id="7c35d-113">After successful completion of this method call, the new value of the *propertyName* property will be *PropValue*.</span></span>

<span data-ttu-id="7c35d-114">Ad esempio, per impostare il valore della proprietà per **RootStoreType**, è possibile usare il codice seguente.</span><span class="sxs-lookup"><span data-stu-id="7c35d-114">For example, to set the property value for the **RootStoreType**, the following code could be used.</span></span>


```C++
// Set the store type.
// bstrNewType previously set to a valid store type
hr = pEnroll->put_RootStoreType( bstrNewType );
```



 

 




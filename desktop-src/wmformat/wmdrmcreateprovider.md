---
title: Funzione WMDRMCreateProvider (wmdrmsdk. h)
description: La funzione WMDRMCreateProvider crea un class factory in grado di creare gli altri oggetti delle API estese del client Windows Media DRM.
ms.assetid: 25ec2fbf-136a-4f40-b2d3-f35b42178c60
keywords:
- Formato Windows Media della funzione WMDRMCreateProvider
topic_type:
- apiref
api_name:
- WMDRMCreateProvider
api_location:
- Wmdrmsdk.dll
- Ext-MS-Win-mm-wmdrmsdk-l1-1-0.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cdf7a102d969ce916f8a5692d994c183305409a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325533"
---
# <a name="wmdrmcreateprovider-function"></a><span data-ttu-id="f20c3-104">WMDRMCreateProvider (funzione)</span><span class="sxs-lookup"><span data-stu-id="f20c3-104">WMDRMCreateProvider function</span></span>

<span data-ttu-id="f20c3-105">La funzione **WMDRMCreateProvider** crea un class factory in grado di creare gli altri oggetti delle API estese del client Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="f20c3-105">The **WMDRMCreateProvider** function creates a class factory that can create the other objects of the Windows Media DRM Client Extended APIs.</span></span> <span data-ttu-id="f20c3-106">Questa funzione non richiede una libreria stub di Microsoft e crea oggetti che non supportano le funzionalità DRM protette.</span><span class="sxs-lookup"><span data-stu-id="f20c3-106">This function does not require a stub library from Microsoft and creates objects that do not support the protected DRM features.</span></span>

## <a name="syntax"></a><span data-ttu-id="f20c3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f20c3-107">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE WMDRMCreateProvider(
  _Out_ IWMDRMProvider **ppDRMProvider
);
```



## <a name="parameters"></a><span data-ttu-id="f20c3-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f20c3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f20c3-109">*ppDRMProvider* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f20c3-109">*ppDRMProvider* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f20c3-110">Riceve un puntatore all'interfaccia [**IWMDRMProvider**](iwmdrmprovider.md) dell'oggetto appena creato.</span><span class="sxs-lookup"><span data-stu-id="f20c3-110">Receives a pointer to the [**IWMDRMProvider**](iwmdrmprovider.md) interface of the newly created object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f20c3-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f20c3-111">Return value</span></span>

<span data-ttu-id="f20c3-112">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f20c3-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f20c3-113">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="f20c3-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f20c3-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f20c3-114">Return code</span></span>                                                                          | <span data-ttu-id="f20c3-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f20c3-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f20c3-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f20c3-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f20c3-117">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="f20c3-117">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f20c3-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f20c3-118">Requirements</span></span>



| <span data-ttu-id="f20c3-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f20c3-119">Requirement</span></span> | <span data-ttu-id="f20c3-120">Valore</span><span class="sxs-lookup"><span data-stu-id="f20c3-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f20c3-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f20c3-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f20c3-122"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="f20c3-122"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="f20c3-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="f20c3-123">Library</span></span><br/> | <dl> <span data-ttu-id="f20c3-124"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f20c3-124"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |
| <span data-ttu-id="f20c3-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f20c3-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="f20c3-126"><dt>Wmdrmsdk.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f20c3-126"><dt>Wmdrmsdk.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f20c3-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f20c3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f20c3-128">**Funzioni**</span><span class="sxs-lookup"><span data-stu-id="f20c3-128">**Functions**</span></span>](drm-functions.md)
</dt> <dt>

[<span data-ttu-id="f20c3-129">**WMDRMCreateProtectedProvider**</span><span class="sxs-lookup"><span data-stu-id="f20c3-129">**WMDRMCreateProtectedProvider**</span></span>](wmdrmcreateprotectedprovider.md)
</dt> </dl>

 

 






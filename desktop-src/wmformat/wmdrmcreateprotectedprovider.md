---
title: Funzione WMDRMCreateProtectedProvider (wmdrmsdk. h)
description: La funzione WMDRMCreateProtectedProvider crea un class factory in grado di creare gli altri oggetti delle API estese del client Windows Media DRM.
ms.assetid: 0882062f-48a2-43bc-8853-a8a3d6bc2f52
keywords:
- Formato Windows Media della funzione WMDRMCreateProtectedProvider
topic_type:
- apiref
api_name:
- WMDRMCreateProtectedProvider
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1f046de906c7753fa200de5075cf2064721940b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324816"
---
# <a name="wmdrmcreateprotectedprovider-function"></a><span data-ttu-id="98732-104">WMDRMCreateProtectedProvider (funzione)</span><span class="sxs-lookup"><span data-stu-id="98732-104">WMDRMCreateProtectedProvider function</span></span>

<span data-ttu-id="98732-105">La funzione **WMDRMCreateProtectedProvider** crea un class factory in grado di creare gli altri oggetti delle API estese del client Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="98732-105">The **WMDRMCreateProtectedProvider** function creates a class factory that can create the other objects of the Windows Media DRM Client Extended APIs.</span></span> <span data-ttu-id="98732-106">Questa funzione richiede una libreria stub di Microsoft e crea oggetti che supportano le funzionalità DRM protette.</span><span class="sxs-lookup"><span data-stu-id="98732-106">This function requires a stub library from Microsoft and creates objects that support the protected DRM features.</span></span>

## <a name="syntax"></a><span data-ttu-id="98732-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="98732-107">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE WMDRMCreateProtectedProvider(
  _Out_ IWMDRMProvider **ppDRMProvider
);
```



## <a name="parameters"></a><span data-ttu-id="98732-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="98732-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98732-109">*ppDRMProvider* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="98732-109">*ppDRMProvider* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="98732-110">Riceve un puntatore all'interfaccia [**IWMDRMProvider**](iwmdrmprovider.md) dell'oggetto appena creato.</span><span class="sxs-lookup"><span data-stu-id="98732-110">Receives a pointer to the [**IWMDRMProvider**](iwmdrmprovider.md) interface of the newly created object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98732-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="98732-111">Return value</span></span>

<span data-ttu-id="98732-112">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="98732-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="98732-113">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="98732-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="98732-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="98732-114">Return code</span></span>                                                                          | <span data-ttu-id="98732-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="98732-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="98732-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="98732-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="98732-117">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="98732-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="98732-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="98732-118">Remarks</span></span>

<span data-ttu-id="98732-119">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="98732-119">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="98732-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98732-120">Requirements</span></span>



| <span data-ttu-id="98732-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="98732-121">Requirement</span></span> | <span data-ttu-id="98732-122">Valore</span><span class="sxs-lookup"><span data-stu-id="98732-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="98732-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="98732-123">Header</span></span><br/> | <dl> <span data-ttu-id="98732-124"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="98732-124"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98732-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="98732-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98732-126">**Funzioni**</span><span class="sxs-lookup"><span data-stu-id="98732-126">**Functions**</span></span>](drm-functions.md)
</dt> <dt>

[<span data-ttu-id="98732-127">**WMDRMCreateProvider**</span><span class="sxs-lookup"><span data-stu-id="98732-127">**WMDRMCreateProvider**</span></span>](wmdrmcreateprovider.md)
</dt> </dl>

 

 






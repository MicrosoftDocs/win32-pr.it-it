---
title: Funzione WMDRMStartup (wmdrmsdk. h)
description: La funzione WMDRMStartup Inizializza le risorse usate dalle API estese del client Windows Media DRM.
ms.assetid: 2fd26bcc-8106-4356-933a-d4cf3536f4fb
keywords:
- Formato Windows Media della funzione WMDRMStartup
topic_type:
- apiref
api_name:
- WMDRMStartup
api_location:
- Wmdrmsdk.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c152a5160750f3c1943b455a8877b4615781b6ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330875"
---
# <a name="wmdrmstartup-function"></a><span data-ttu-id="3c1a4-104">WMDRMStartup (funzione)</span><span class="sxs-lookup"><span data-stu-id="3c1a4-104">WMDRMStartup function</span></span>

<span data-ttu-id="3c1a4-105">La funzione **WMDRMStartup** Inizializza le risorse usate dalle API estese del client Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="3c1a4-105">The **WMDRMStartup** function initializes resources used by the Windows Media DRM Client Extended APIs.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c1a4-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3c1a4-106">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE WMDRMStartup(void);
```



## <a name="parameters"></a><span data-ttu-id="3c1a4-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="3c1a4-107">Parameters</span></span>

<span data-ttu-id="3c1a4-108">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="3c1a4-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3c1a4-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3c1a4-109">Return value</span></span>

<span data-ttu-id="3c1a4-110">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="3c1a4-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3c1a4-111">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="3c1a4-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3c1a4-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="3c1a4-112">Return code</span></span>                                                                          | <span data-ttu-id="3c1a4-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c1a4-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="3c1a4-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3c1a4-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="3c1a4-115">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="3c1a4-115">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3c1a4-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="3c1a4-116">Remarks</span></span>

<span data-ttu-id="3c1a4-117">Per ogni chiamata di questa funzione, è necessario chiamare [**WMDRMShutdown**](wmdrmshutdown.md) per rilasciare le risorse utilizzate.</span><span class="sxs-lookup"><span data-stu-id="3c1a4-117">For every call of this function, you must call [**WMDRMShutdown**](wmdrmshutdown.md) to release the resources used.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c1a4-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c1a4-118">Requirements</span></span>



| <span data-ttu-id="3c1a4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c1a4-119">Requirement</span></span> | <span data-ttu-id="3c1a4-120">Valore</span><span class="sxs-lookup"><span data-stu-id="3c1a4-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c1a4-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3c1a4-121">Header</span></span><br/>  | <dl> <span data-ttu-id="3c1a4-122"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c1a4-122"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="3c1a4-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="3c1a4-123">Library</span></span><br/> | <dl> <span data-ttu-id="3c1a4-124"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c1a4-124"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |
| <span data-ttu-id="3c1a4-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3c1a4-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="3c1a4-126"><dt>Wmdrmsdk.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c1a4-126"><dt>Wmdrmsdk.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c1a4-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3c1a4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c1a4-128">**Funzioni**</span><span class="sxs-lookup"><span data-stu-id="3c1a4-128">**Functions**</span></span>](drm-functions.md)
</dt> </dl>

 

 






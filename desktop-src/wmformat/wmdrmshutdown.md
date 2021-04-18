---
title: Funzione WMDRMShutdown (wmdrmsdk. h)
description: La funzione WMDRMShutdown rilascia le risorse usate dalle API estese del client Windows Media DRM.
ms.assetid: fa99a07a-2f07-464b-b7a2-e8f3110389b5
keywords:
- Formato Windows Media della funzione WMDRMShutdown
topic_type:
- apiref
api_name:
- WMDRMShutdown
api_location:
- Wmdrmsdk.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eb49049a593699a4071eefea9c5cf7c61571fc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324809"
---
# <a name="wmdrmshutdown-function"></a><span data-ttu-id="c9b39-104">WMDRMShutdown (funzione)</span><span class="sxs-lookup"><span data-stu-id="c9b39-104">WMDRMShutdown function</span></span>

<span data-ttu-id="c9b39-105">La funzione **WMDRMShutdown** rilascia le risorse usate dalle API estese del client Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="c9b39-105">The **WMDRMShutdown** function releases resources used by the Windows Media DRM Client Extended APIs.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9b39-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c9b39-106">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE WMDRMShutdown(void);
```



## <a name="parameters"></a><span data-ttu-id="c9b39-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="c9b39-107">Parameters</span></span>

<span data-ttu-id="c9b39-108">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="c9b39-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c9b39-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c9b39-109">Return value</span></span>

<span data-ttu-id="c9b39-110">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c9b39-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c9b39-111">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="c9b39-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c9b39-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c9b39-112">Return code</span></span>                                                                          | <span data-ttu-id="c9b39-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9b39-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="c9b39-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c9b39-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="c9b39-115">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="c9b39-115">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c9b39-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="c9b39-116">Remarks</span></span>

<span data-ttu-id="c9b39-117">Per evitare perdite di memoria, è necessario chiamare questa funzione per ogni chiamata della funzione [**WMDRMStartup**](wmdrmstartup.md) .</span><span class="sxs-lookup"><span data-stu-id="c9b39-117">To avoid memory leaks, you must call this function for every call of the [**WMDRMStartup**](wmdrmstartup.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9b39-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c9b39-118">Requirements</span></span>



| <span data-ttu-id="c9b39-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9b39-119">Requirement</span></span> | <span data-ttu-id="c9b39-120">Valore</span><span class="sxs-lookup"><span data-stu-id="c9b39-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9b39-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c9b39-121">Header</span></span><br/>  | <dl> <span data-ttu-id="c9b39-122"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9b39-122"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="c9b39-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="c9b39-123">Library</span></span><br/> | <dl> <span data-ttu-id="c9b39-124"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c9b39-124"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |
| <span data-ttu-id="c9b39-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c9b39-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="c9b39-126"><dt>Wmdrmsdk.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9b39-126"><dt>Wmdrmsdk.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9b39-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c9b39-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9b39-128">**Funzioni**</span><span class="sxs-lookup"><span data-stu-id="c9b39-128">**Functions**</span></span>](drm-functions.md)
</dt> </dl>

 

 






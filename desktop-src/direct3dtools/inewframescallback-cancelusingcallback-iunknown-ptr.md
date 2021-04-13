---
description: Callback che notifica all'host una richiesta annullata.
MS-HAID: vspixengine.INewFramesCallback\_CancelUsingCallback\_IUnknown\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo INewFramesCallback:: CancelUsingCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 291B2F85-1437-4704-8971-4B7C25B693F8
api_name:
- INewFramesCallback.CancelUsingCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 863219cd37078fbde1e7ef8b2da7677a31e12872
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482653"
---
# <a name="span-idvspixengineinewframescallback_cancelusingcallback_iunknown_ptrspaninewframescallbackcancelusingcallback-method"></a><span data-ttu-id="6bd62-103"><span id="vspixengine.inewframescallback_cancelusingcallback_iunknown_ptr"></span>Metodo INewFramesCallback:: CancelUsingCallback</span><span class="sxs-lookup"><span data-stu-id="6bd62-103"><span id="vspixengine.inewframescallback_cancelusingcallback_iunknown_ptr"></span>INewFramesCallback::CancelUsingCallback method</span></span>

<span data-ttu-id="6bd62-104">Callback che notifica all'host una richiesta annullata.</span><span class="sxs-lookup"><span data-stu-id="6bd62-104">A callback that notifies the host of a canceled request.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bd62-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6bd62-105">Syntax</span></span>


```C++
HRESULT CancelUsingCallback(
   IUnknown * requestCallback
);
```

## <a name="parameters"></a><span data-ttu-id="6bd62-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6bd62-106">Parameters</span></span>

<span data-ttu-id="6bd62-107">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="6bd62-107">*requestCallback* </span></span>  
<span data-ttu-id="6bd62-108">Indirizzo della richiesta annullata.</span><span class="sxs-lookup"><span data-stu-id="6bd62-108">The address of the cancelled request.</span></span>

## <a name="return-value"></a><span data-ttu-id="6bd62-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6bd62-109">Return value</span></span>

<span data-ttu-id="6bd62-110">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6bd62-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6bd62-111">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6bd62-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bd62-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6bd62-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="6bd62-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6bd62-113">Header</span></span></p></td><td><span data-ttu-id="6bd62-114">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="6bd62-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="6bd62-115"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="6bd62-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="6bd62-116">**INewFramesCallback**</span><span class="sxs-lookup"><span data-stu-id="6bd62-116">**INewFramesCallback**</span></span>](/windows/desktop/direct3dtools/inewframescallback)

 

 

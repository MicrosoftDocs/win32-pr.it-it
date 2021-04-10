---
description: Attendere l'arresto del motore specificato (chiamata di blocco).
MS-HAID: vspixengine.IServerConnectionCallback\_WaitForShutdown\_IPixEngine\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IServerConnectionCallback:: WaitForShutdown'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B70229D5-3C41-4B50-8336-A1271A9EBE81
api_name:
- IServerConnectionCallback.WaitForShutdown
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d98bd5f398748e6e62a099bcc2be94b5e5f27bc8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125355"
---
# <a name="span-idvspixengineiserverconnectioncallback_waitforshutdown_ipixengine_ptrspaniserverconnectioncallbackwaitforshutdown-method"></a><span data-ttu-id="78fa1-103"><span id="vspixengine.iserverconnectioncallback_waitforshutdown_ipixengine_ptr"></span>Metodo IServerConnectionCallback:: WaitForShutdown</span><span class="sxs-lookup"><span data-stu-id="78fa1-103"><span id="vspixengine.iserverconnectioncallback_waitforshutdown_ipixengine_ptr"></span>IServerConnectionCallback::WaitForShutdown method</span></span>

<span data-ttu-id="78fa1-104">Attendere l'arresto del motore specificato (chiamata di blocco).</span><span class="sxs-lookup"><span data-stu-id="78fa1-104">Wait for shutdown of the specified engine (Blocking call).</span></span>

## <a name="syntax"></a><span data-ttu-id="78fa1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="78fa1-105">Syntax</span></span>


```C++
HRESULT WaitForShutdown(
   IPixEngine * pEngine
);
```

## <a name="parameters"></a><span data-ttu-id="78fa1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="78fa1-106">Parameters</span></span>

<span data-ttu-id="78fa1-107">*pEngine* </span><span class="sxs-lookup"><span data-stu-id="78fa1-107">*pEngine* </span></span>  
<span data-ttu-id="78fa1-108">Motore da arrestare.</span><span class="sxs-lookup"><span data-stu-id="78fa1-108">The engine to shut down.</span></span>

## <a name="return-value"></a><span data-ttu-id="78fa1-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="78fa1-109">Return value</span></span>

<span data-ttu-id="78fa1-110">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="78fa1-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="78fa1-111">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="78fa1-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="78fa1-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="78fa1-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="78fa1-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="78fa1-113">Header</span></span></p></td><td><span data-ttu-id="78fa1-114">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="78fa1-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="78fa1-115"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="78fa1-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="78fa1-116">**IServerConnectionCallback**</span><span class="sxs-lookup"><span data-stu-id="78fa1-116">**IServerConnectionCallback**</span></span>](/windows/desktop/direct3dtools/iserverconnectioncallback)

 

 

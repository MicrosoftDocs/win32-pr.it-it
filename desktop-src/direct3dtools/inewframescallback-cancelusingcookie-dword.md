---
description: Callback che notifica all'host di una richiesta annullata usando un cookie che identifica in modo univoco la richiesta.
MS-HAID: vspixengine.INewFramesCallback\_CancelUsingCookie\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo INewFramesCallback:: CancelUsingCookie'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 36176554-BB4F-40CB-AB7B-4957DA84BAA8
api_name:
- INewFramesCallback.CancelUsingCookie
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: dfbbbda1a11244088dccad640be348da1e4d8313
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481284"
---
# <a name="span-idvspixengineinewframescallback_cancelusingcookie_dwordspaninewframescallbackcancelusingcookie-method"></a><span data-ttu-id="a1bf6-103"><span id="vspixengine.inewframescallback_cancelusingcookie_dword"></span>Metodo INewFramesCallback:: CancelUsingCookie</span><span class="sxs-lookup"><span data-stu-id="a1bf6-103"><span id="vspixengine.inewframescallback_cancelusingcookie_dword"></span>INewFramesCallback::CancelUsingCookie method</span></span>

<span data-ttu-id="a1bf6-104">Callback che notifica all'host di una richiesta annullata usando un cookie che identifica in modo univoco la richiesta.</span><span class="sxs-lookup"><span data-stu-id="a1bf6-104">A callback that notifies the host of a canceled request by using a cookie that uniquely identifies the request.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1bf6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a1bf6-105">Syntax</span></span>


```C++
HRESULT CancelUsingCallback(
   IUnknown * requestCallback
);
```

## <a name="parameters"></a><span data-ttu-id="a1bf6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a1bf6-106">Parameters</span></span>

<span data-ttu-id="a1bf6-107">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="a1bf6-107">*requestCookie* </span></span>  
<span data-ttu-id="a1bf6-108">Cookie che idenfies in modo univoco la richiesta annullata.</span><span class="sxs-lookup"><span data-stu-id="a1bf6-108">The cookie which uniquely idenfies the cancelled request.</span></span>

## <a name="return-value"></a><span data-ttu-id="a1bf6-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a1bf6-109">Return value</span></span>

<span data-ttu-id="a1bf6-110">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a1bf6-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a1bf6-111">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a1bf6-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1bf6-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1bf6-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="a1bf6-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a1bf6-113">Header</span></span></p></td><td><span data-ttu-id="a1bf6-114">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="a1bf6-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="a1bf6-115"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="a1bf6-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="a1bf6-116">**INewFramesCallback**</span><span class="sxs-lookup"><span data-stu-id="a1bf6-116">**INewFramesCallback**</span></span>](/windows/desktop/direct3dtools/inewframescallback)

 

 

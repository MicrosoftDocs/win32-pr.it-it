---
title: Metodo IAMWMBufferPass senotify
description: Il metodo senotify viene usato dalle applicazioni per fornire il filtro WM ASF Writer o WM ASF Reader con un puntatore all'interfaccia IAMWMBufferPassCallback dell'applicazione.
ms.assetid: b0fff344-a20c-4cfc-828b-c6fc49d990ea
keywords:
- Metodo senotify-formato Windows Media
- Metodo senotify, formato Windows Media, interfaccia IAMWMBufferPass
- Interfaccia IAMWMBufferPass Windows Media Format, metodo senotify
topic_type:
- apiref
api_name:
- IAMWMBufferPass.SetNotify
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9739952792fcfa49da1b5656db513c3af41a419c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399558"
---
# <a name="iamwmbufferpasssetnotify-method"></a><span data-ttu-id="c78c9-106">Metodo IAMWMBufferPass:: senotify</span><span class="sxs-lookup"><span data-stu-id="c78c9-106">IAMWMBufferPass::SetNotify method</span></span>

<span data-ttu-id="c78c9-107">Il metodo **senotify** viene usato dalle applicazioni per fornire il filtro WM ASF Writer o [WM ASF Reader](wm-asf-reader-filter.md) con un puntatore all'interfaccia [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c78c9-107">The **SetNotify** method is used by applications to provide the WM ASF Writer or [WM ASF Reader](wm-asf-reader-filter.md) filter with a pointer to the application's [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="c78c9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c78c9-108">Syntax</span></span>


```C++
HRESULT SetNotify(
  [in] IAMWMBufferPassCallback *pCallback
);
```



## <a name="parameters"></a><span data-ttu-id="c78c9-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c78c9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c78c9-110">*pCallback* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c78c9-110">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c78c9-111">Puntatore all'interfaccia **IAMWMBufferPassCallback** dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c78c9-111">Pointer to the application's **IAMWMBufferPassCallback** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c78c9-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c78c9-112">Return value</span></span>

<span data-ttu-id="c78c9-113">Se il metodo ha esito positivo, restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c78c9-113">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="c78c9-114">Se ha esito negativo, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c78c9-114">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c78c9-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="c78c9-115">Remarks</span></span>

<span data-ttu-id="c78c9-116">Chiamare questo metodo prima di inserire il grafico del filtro nello stato di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="c78c9-116">Call this method before putting the filter graph into the run state.</span></span>

## <a name="see-also"></a><span data-ttu-id="c78c9-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c78c9-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c78c9-118">**Interfaccia IAMWMBufferPass**</span><span class="sxs-lookup"><span data-stu-id="c78c9-118">**IAMWMBufferPass Interface**</span></span>](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass)
</dt> </dl>

 

 
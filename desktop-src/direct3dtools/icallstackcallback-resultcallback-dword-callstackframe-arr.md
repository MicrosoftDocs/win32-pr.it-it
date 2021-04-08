---
description: Funzione di callback utilizzata per notificare all'host le informazioni sullo stack di chiamate.
MS-HAID: vspixengine.ICallStackCallback\_ResultCallback\_DWORD\_CallStackFrame\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo ICallStackCallback:: ResultCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9C083298-6FD5-4414-8E0C-625F6A144668
api_name:
- ICallStackCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4bd77ea22fd31b31081d72707b1fd7a2efbda607
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876626"
---
# <a name="span-idvspixengineicallstackcallback_resultcallback_dword_callstackframe_arrspanicallstackcallbackresultcallback-method"></a><span data-ttu-id="c5caf-103"><span id="vspixengine.icallstackcallback_resultcallback_dword_callstackframe_arr"></span>Metodo ICallStackCallback:: ResultCallback</span><span class="sxs-lookup"><span data-stu-id="c5caf-103"><span id="vspixengine.icallstackcallback_resultcallback_dword_callstackframe_arr"></span>ICallStackCallback::ResultCallback method</span></span>

<span data-ttu-id="c5caf-104">Funzione di callback utilizzata per notificare all'host le informazioni sullo stack di chiamate.</span><span class="sxs-lookup"><span data-stu-id="c5caf-104">A callback function used to notify the host of call stack information.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5caf-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c5caf-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD             count,
   CallStackFrame [] count0_callStackFrameBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="c5caf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c5caf-106">Parameters</span></span>

<span data-ttu-id="c5caf-107">*conteggio* </span><span class="sxs-lookup"><span data-stu-id="c5caf-107">*count* </span></span>  
<span data-ttu-id="c5caf-108">Numero di framebuffer stack restituiti.</span><span class="sxs-lookup"><span data-stu-id="c5caf-108">The number of callstack framebuffers returned.</span></span>

<span data-ttu-id="c5caf-109">*\_callStackFrameBuffer count0* </span><span class="sxs-lookup"><span data-stu-id="c5caf-109">*count0\_callStackFrameBuffer* </span></span>  
<span data-ttu-id="c5caf-110">Informazioni stack.</span><span class="sxs-lookup"><span data-stu-id="c5caf-110">The callstack information.</span></span>

## <a name="return-value"></a><span data-ttu-id="c5caf-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c5caf-111">Return value</span></span>

<span data-ttu-id="c5caf-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c5caf-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c5caf-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c5caf-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5caf-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c5caf-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c5caf-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c5caf-115">Header</span></span></p></td><td><span data-ttu-id="c5caf-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="c5caf-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="c5caf-117"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="c5caf-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="c5caf-118">**ICallStackCallback**</span><span class="sxs-lookup"><span data-stu-id="c5caf-118">**ICallStackCallback**</span></span>](/windows/desktop/direct3dtools/icallstackcallback)

 

 

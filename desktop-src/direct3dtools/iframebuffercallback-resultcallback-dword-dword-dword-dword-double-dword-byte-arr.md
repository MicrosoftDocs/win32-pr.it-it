---
description: Callback che notifica all'host le informazioni sul framebuffer restituite dalla richiesta associata.
MS-HAID: vspixengine.IFrameBufferCallback\_ResultCallback\_DWORD\_DWORD\_DWORD\_DWORD\_double\_DWORD\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IFrameBufferCallback:: ResultCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F0276125-2DA9-45BC-A295-BD67C21EE601
api_name:
- IFrameBufferCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5433c7bbf5fe67455b60fd754eecb2c2877c5d6f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124617"
---
# <a name="span-idvspixengineiframebuffercallback_resultcallback_dword_dword_dword_dword_double_dword_byte_arrspaniframebuffercallbackresultcallback-method"></a><span data-ttu-id="39b58-103"><span id="vspixengine.iframebuffercallback_resultcallback_dword_dword_dword_dword_double_dword_byte_arr"></span>Metodo IFrameBufferCallback:: ResultCallback</span><span class="sxs-lookup"><span data-stu-id="39b58-103"><span id="vspixengine.iframebuffercallback_resultcallback_dword_dword_dword_dword_double_dword_byte_arr"></span>IFrameBufferCallback::ResultCallback method</span></span>

<span data-ttu-id="39b58-104">Callback che notifica all'host le informazioni sul framebuffer restituite dalla richiesta associata.</span><span class="sxs-lookup"><span data-stu-id="39b58-104">A callback that notifies the host of framebuffer information returned by the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="39b58-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="39b58-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD   frameNumber,
   DWORD   width,
   DWORD   height,
   DWORD   renderTargetPtr,
   double  frameDuraction,
   DWORD   size,
   BYTE [] count5_buffer
);
```

## <a name="parameters"></a><span data-ttu-id="39b58-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="39b58-106">Parameters</span></span>

<span data-ttu-id="39b58-107">*NumeroFrame* </span><span class="sxs-lookup"><span data-stu-id="39b58-107">*frameNumber* </span></span>  
<span data-ttu-id="39b58-108">Numero di frame.</span><span class="sxs-lookup"><span data-stu-id="39b58-108">The frame number.</span></span>

<span data-ttu-id="39b58-109">*Larghezza* </span><span class="sxs-lookup"><span data-stu-id="39b58-109">*width* </span></span>  
<span data-ttu-id="39b58-110">Larghezza del frame.</span><span class="sxs-lookup"><span data-stu-id="39b58-110">The width of the frame.</span></span>

<span data-ttu-id="39b58-111">*altezza* </span><span class="sxs-lookup"><span data-stu-id="39b58-111">*height* </span></span>  
<span data-ttu-id="39b58-112">Altezza del frame.</span><span class="sxs-lookup"><span data-stu-id="39b58-112">The height of the frame.</span></span>

<span data-ttu-id="39b58-113">*renderTargetPtr* </span><span class="sxs-lookup"><span data-stu-id="39b58-113">*renderTargetPtr* </span></span>  
<span data-ttu-id="39b58-114">Destinazione di rendering da cui provengono i risultati.</span><span class="sxs-lookup"><span data-stu-id="39b58-114">The render target that the results come from.</span></span> <span data-ttu-id="39b58-115">Si tratta sempre di uno slot specificato dalla richiesta del buffer del frame oppure, in caso contrario, della prima Bount di RTV per l'origine di output.</span><span class="sxs-lookup"><span data-stu-id="39b58-115">It is always a slot specified by the frame buffer request, or if not a draw call, then the first RTV bount to the output source.</span></span>

<span data-ttu-id="39b58-116">*frameDuraction* </span><span class="sxs-lookup"><span data-stu-id="39b58-116">*frameDuraction* </span></span>  
<span data-ttu-id="39b58-117">Non usato.</span><span class="sxs-lookup"><span data-stu-id="39b58-117">Not used.</span></span>

<span data-ttu-id="39b58-118">*dimensioni* </span><span class="sxs-lookup"><span data-stu-id="39b58-118">*size* </span></span>  
<span data-ttu-id="39b58-119">Dimensioni in byte del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="39b58-119">The size of the output buffer in bytes.</span></span>

<span data-ttu-id="39b58-120">*\_buffer count5* </span><span class="sxs-lookup"><span data-stu-id="39b58-120">*count5\_buffer* </span></span>  
<span data-ttu-id="39b58-121">Contenuto della destinazione di rendering nel formato R8G8B8A8 \_ UNORM.</span><span class="sxs-lookup"><span data-stu-id="39b58-121">The contents of the render target in R8G8B8A8\_UNORM format.</span></span>

## <a name="return-value"></a><span data-ttu-id="39b58-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="39b58-122">Return value</span></span>

<span data-ttu-id="39b58-123">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="39b58-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="39b58-124">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="39b58-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="39b58-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39b58-125">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="39b58-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="39b58-126">Header</span></span></p></td><td><span data-ttu-id="39b58-127">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="39b58-127">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="39b58-128"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="39b58-128"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="39b58-129">**IFrameBufferCallback**</span><span class="sxs-lookup"><span data-stu-id="39b58-129">**IFrameBufferCallback**</span></span>](/windows/desktop/direct3dtools/iframebuffercallback)

 

 

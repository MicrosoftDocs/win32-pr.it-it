---
description: La funzione GetFrameFromFrameHandle restituisce un puntatore a un frame da un handle di frame.
ms.assetid: 790fe5fe-a857-4947-a471-d0538c0f0d61
title: Funzione GetFrameFromFrameHandle (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameFromFrameHandle
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ce8151b2f4c81c61dea5969ff52e9ddf2d6615a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305908"
---
# <a name="getframefromframehandle-function"></a><span data-ttu-id="852be-103">GetFrameFromFrameHandle (funzione)</span><span class="sxs-lookup"><span data-stu-id="852be-103">GetFrameFromFrameHandle function</span></span>

<span data-ttu-id="852be-104">La funzione **GetFrameFromFrameHandle** restituisce un puntatore a un frame da un handle di frame.</span><span class="sxs-lookup"><span data-stu-id="852be-104">The **GetFrameFromFrameHandle** function returns a pointer to a frame from a frame handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="852be-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="852be-105">Syntax</span></span>


```C++
ULPFRAME WINAPI GetFrameFromFrameHandle(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="852be-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="852be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="852be-107">*hFrame* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="852be-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="852be-108">Handle per il frame.</span><span class="sxs-lookup"><span data-stu-id="852be-108">Handle to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="852be-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="852be-109">Return value</span></span>

<span data-ttu-id="852be-110">Se la funzione ha esito positivo, il valore restituito è un puntatore al frame.</span><span class="sxs-lookup"><span data-stu-id="852be-110">If the function is successful, the return value is a pointer to the frame.</span></span>

<span data-ttu-id="852be-111">Se la funzione ha esito negativo, il valore restituito è 0.</span><span class="sxs-lookup"><span data-stu-id="852be-111">If the function is unsuccessful, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="852be-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="852be-112">Remarks</span></span>

<span data-ttu-id="852be-113">La funzione **GetFrameFromFrameHandle** recupera i dati che non possono essere recuperati dalle altre funzioni helper fornite da Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="852be-113">The **GetFrameFromFrameHandle** function retrieves data that cannot be retrieved by the other helper functions that Network Monitor provides.</span></span> <span data-ttu-id="852be-114">Quando possibile, utilizzare le funzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="852be-114">Use the following functions whenever possible.</span></span>

<dl>

[<span data-ttu-id="852be-115">**GetFrameDstAddressOffset**</span><span class="sxs-lookup"><span data-stu-id="852be-115">**GetFrameDstAddressOffset**</span></span>](getframedstaddressoffset.md)  
[<span data-ttu-id="852be-116">**GetFrameSrcAddressOffset**</span><span class="sxs-lookup"><span data-stu-id="852be-116">**GetFrameSrcAddressOffset**</span></span>](getframesrcaddressoffset.md)  
[<span data-ttu-id="852be-117">**GetFrameCaptureHandle**</span><span class="sxs-lookup"><span data-stu-id="852be-117">**GetFrameCaptureHandle**</span></span>](getframecapturehandle.md)  
[<span data-ttu-id="852be-118">**GetFrameDestAddress**</span><span class="sxs-lookup"><span data-stu-id="852be-118">**GetFrameDestAddress**</span></span>](getframedestaddress.md)  
[<span data-ttu-id="852be-119">**GetFrameSourceAddress**</span><span class="sxs-lookup"><span data-stu-id="852be-119">**GetFrameSourceAddress**</span></span>](getframesourceaddress.md)  
[<span data-ttu-id="852be-120">**GetFrameMacHeaderLength**</span><span class="sxs-lookup"><span data-stu-id="852be-120">**GetFrameMacHeaderLength**</span></span>](getframemacheaderlength.md)  
[<span data-ttu-id="852be-121">**GetFrameLength**</span><span class="sxs-lookup"><span data-stu-id="852be-121">**GetFrameLength**</span></span>](getframelength.md)  
[<span data-ttu-id="852be-122">**GetFrameStoredLength**</span><span class="sxs-lookup"><span data-stu-id="852be-122">**GetFrameStoredLength**</span></span>](getframestoredlength.md)  
[<span data-ttu-id="852be-123">**GetFrameMacType**</span><span class="sxs-lookup"><span data-stu-id="852be-123">**GetFrameMacType**</span></span>](getframemactype.md)  
[<span data-ttu-id="852be-124">**GetFrameNumber**</span><span class="sxs-lookup"><span data-stu-id="852be-124">**GetFrameNumber**</span></span>](getframenumber.md)  
[<span data-ttu-id="852be-125">**GetFrameTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="852be-125">**GetFrameTimeStamp**</span></span>](getframetimestamp.md)  
</dl>

<span data-ttu-id="852be-126">Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **GetFrameFromFrameHandle** .</span><span class="sxs-lookup"><span data-stu-id="852be-126">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameFromFrameHandle** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="852be-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="852be-127">Requirements</span></span>



| <span data-ttu-id="852be-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="852be-128">Requirement</span></span> | <span data-ttu-id="852be-129">Valore</span><span class="sxs-lookup"><span data-stu-id="852be-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="852be-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="852be-130">Minimum supported client</span></span><br/> | <span data-ttu-id="852be-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="852be-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="852be-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="852be-132">Minimum supported server</span></span><br/> | <span data-ttu-id="852be-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="852be-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="852be-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="852be-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="852be-135"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="852be-135"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="852be-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="852be-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="852be-137"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="852be-137"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="852be-138">DLL</span><span class="sxs-lookup"><span data-stu-id="852be-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="852be-139"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="852be-139"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 





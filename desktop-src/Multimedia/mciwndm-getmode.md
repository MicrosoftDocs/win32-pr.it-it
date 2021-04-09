---
title: Messaggio di MCIWNDM_GETMODE (VFW. h)
description: Il \_ messaggio MCIWNDM GetMode recupera la modalità operativa corrente di un dispositivo MCI. I dispositivi MCI hanno diverse modalità operative, indicate da costanti. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndGetMode.
ms.assetid: cc327281-434e-4047-9e15-c04a10953f47
keywords:
- MCIWNDM_GETMODE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_GETMODE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5daefea2c550a1d0cf807ae03840c38ae8b2567c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104118947"
---
# <a name="mciwndm_getmode-message"></a><span data-ttu-id="133e4-106">\_Messaggio GETMODE MCIWNDM</span><span class="sxs-lookup"><span data-stu-id="133e4-106">MCIWNDM\_GETMODE message</span></span>

<span data-ttu-id="133e4-107">Il messaggio **MCIWNDM \_ GetMode** recupera la modalità operativa corrente di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="133e4-107">The **MCIWNDM\_GETMODE** message retrieves the current operating mode of an MCI device.</span></span> <span data-ttu-id="133e4-108">I dispositivi MCI hanno diverse modalità operative, indicate da costanti.</span><span class="sxs-lookup"><span data-stu-id="133e4-108">MCI devices have several operating modes, which are designated by constants.</span></span> <span data-ttu-id="133e4-109">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndGetMode**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode) .</span><span class="sxs-lookup"><span data-stu-id="133e4-109">You can send this message explicitly or by using the [**MCIWndGetMode**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode) macro.</span></span>


```C++
MCIWNDM_GETMODE 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a><span data-ttu-id="133e4-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="133e4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="133e4-111"><span id="len"></span><span id="LEN"></span>*Len*</span><span class="sxs-lookup"><span data-stu-id="133e4-111"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="133e4-112">Dimensione, in byte, del buffer.</span><span class="sxs-lookup"><span data-stu-id="133e4-112">Size, in bytes, of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="133e4-113"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="133e4-113"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="133e4-114">Puntatore al buffer definito dall'applicazione utilizzato per restituire la modalità.</span><span class="sxs-lookup"><span data-stu-id="133e4-114">Pointer to the application-defined buffer used to return the mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="133e4-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="133e4-115">Return Value</span></span>

<span data-ttu-id="133e4-116">Restituisce un Integer che corrisponde alla costante MCI che definisce la modalità.</span><span class="sxs-lookup"><span data-stu-id="133e4-116">Returns an integer corresponding to the MCI constant defining the mode.</span></span>

## <a name="remarks"></a><span data-ttu-id="133e4-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="133e4-117">Remarks</span></span>

<span data-ttu-id="133e4-118">Se la stringa con terminazione null che descrive la modalità è più lunga del buffer, viene troncata.</span><span class="sxs-lookup"><span data-stu-id="133e4-118">If the null-terminated string describing the mode is longer than the buffer, it is truncated.</span></span>

<span data-ttu-id="133e4-119">Non tutti i dispositivi possono funzionare in ogni modalità.</span><span class="sxs-lookup"><span data-stu-id="133e4-119">Not all devices can operate in every mode.</span></span> <span data-ttu-id="133e4-120">Ad esempio, il dispositivo MCIAVI è un dispositivo di riproduzione; non supporta la modalità di registrazione.</span><span class="sxs-lookup"><span data-stu-id="133e4-120">For example, the MCIAVI device is a playback device; it doesn't support the recording mode.</span></span> <span data-ttu-id="133e4-121">È possibile recuperare le modalità seguenti utilizzando **MCIWNDM \_ GetMode**.</span><span class="sxs-lookup"><span data-stu-id="133e4-121">The following modes can be retrieved by using **MCIWNDM\_GETMODE**.</span></span>



| <span data-ttu-id="133e4-122">Modalità operativa</span><span class="sxs-lookup"><span data-stu-id="133e4-122">Operating mode</span></span> | <span data-ttu-id="133e4-123">Costante MCI</span><span class="sxs-lookup"><span data-stu-id="133e4-123">MCI constant</span></span>          |
|----------------|-----------------------|
| <span data-ttu-id="133e4-124">non pronto</span><span class="sxs-lookup"><span data-stu-id="133e4-124">not ready</span></span>      | <span data-ttu-id="133e4-125">\_modalità MCI \_ non \_ pronta</span><span class="sxs-lookup"><span data-stu-id="133e4-125">MCI\_MODE\_NOT\_READY</span></span> |
| <span data-ttu-id="133e4-126">apre</span><span class="sxs-lookup"><span data-stu-id="133e4-126">open</span></span>           | <span data-ttu-id="133e4-127">\_modalità MCI \_ aperta</span><span class="sxs-lookup"><span data-stu-id="133e4-127">MCI\_MODE\_OPEN</span></span>       |
| <span data-ttu-id="133e4-128">in pausa</span><span class="sxs-lookup"><span data-stu-id="133e4-128">paused</span></span>         | <span data-ttu-id="133e4-129">\_sospensione della modalità MCI \_</span><span class="sxs-lookup"><span data-stu-id="133e4-129">MCI\_MODE\_PAUSE</span></span>      |
| <span data-ttu-id="133e4-130">riproduzione in corso</span><span class="sxs-lookup"><span data-stu-id="133e4-130">playing</span></span>        | <span data-ttu-id="133e4-131">\_riproduzione in modalità MCI \_</span><span class="sxs-lookup"><span data-stu-id="133e4-131">MCI\_MODE\_PLAY</span></span>       |
| <span data-ttu-id="133e4-132">registrazione</span><span class="sxs-lookup"><span data-stu-id="133e4-132">recording</span></span>      | <span data-ttu-id="133e4-133">\_record in modalità MCI \_</span><span class="sxs-lookup"><span data-stu-id="133e4-133">MCI\_MODE\_RECORD</span></span>     |
| <span data-ttu-id="133e4-134">ricerca</span><span class="sxs-lookup"><span data-stu-id="133e4-134">seeking</span></span>        | <span data-ttu-id="133e4-135">\_ricerca in modalità MCI \_</span><span class="sxs-lookup"><span data-stu-id="133e4-135">MCI\_MODE\_SEEK</span></span>       |
| <span data-ttu-id="133e4-136">Arrestato</span><span class="sxs-lookup"><span data-stu-id="133e4-136">stopped</span></span>        | <span data-ttu-id="133e4-137">\_arresto modalità \_ MCI</span><span class="sxs-lookup"><span data-stu-id="133e4-137">MCI\_MODE\_STOP</span></span>       |



 

## <a name="requirements"></a><span data-ttu-id="133e4-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="133e4-138">Requirements</span></span>



| <span data-ttu-id="133e4-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="133e4-139">Requirement</span></span> | <span data-ttu-id="133e4-140">Valore</span><span class="sxs-lookup"><span data-stu-id="133e4-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="133e4-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="133e4-141">Minimum supported client</span></span><br/> | <span data-ttu-id="133e4-142">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="133e4-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="133e4-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="133e4-143">Minimum supported server</span></span><br/> | <span data-ttu-id="133e4-144">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="133e4-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="133e4-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="133e4-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="133e4-146"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="133e4-146"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="133e4-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="133e4-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="133e4-148">**MCIWndGetMode**</span><span class="sxs-lookup"><span data-stu-id="133e4-148">**MCIWndGetMode**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode)
</dt> </dl>

 

 






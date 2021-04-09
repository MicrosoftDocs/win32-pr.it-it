---
title: Messaggio di MCIWNDM_GETTIMEFORMAT (VFW. h)
description: Il \_ messaggio MCIWNDM GETTIMEFORMAT Recupera il formato dell'ora corrente di un dispositivo MCI in due formati come valore numerico e come stringa. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndGetTimeFormat.
ms.assetid: 01844872-5444-4f3b-92a3-64f80b94d3a0
keywords:
- MCIWNDM_GETTIMEFORMAT messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_GETTIMEFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a09f969c009ff23bc0951ed2efbc0dbf7aa95dda
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740239"
---
# <a name="mciwndm_gettimeformat-message"></a><span data-ttu-id="e0416-105">\_Messaggio MCIWNDM GETTIMEFORMAT</span><span class="sxs-lookup"><span data-stu-id="e0416-105">MCIWNDM\_GETTIMEFORMAT message</span></span>

<span data-ttu-id="e0416-106">Il messaggio **MCIWNDM \_ GETTIMEFORMAT** Recupera il formato dell'ora corrente di un dispositivo MCI in due formati: come valore numerico e come stringa.</span><span class="sxs-lookup"><span data-stu-id="e0416-106">The **MCIWNDM\_GETTIMEFORMAT** message retrieves the current time format of an MCI device in two forms: as a numerical value and as a string.</span></span> <span data-ttu-id="e0416-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) .</span><span class="sxs-lookup"><span data-stu-id="e0416-107">You can send this message explicitly or by using the [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) macro.</span></span>


```C++
MCIWNDM_GETTIMEFORMAT 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a><span data-ttu-id="e0416-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e0416-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0416-109"><span id="len"></span><span id="LEN"></span>*Len*</span><span class="sxs-lookup"><span data-stu-id="e0416-109"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="e0416-110">Dimensione, in byte, del buffer.</span><span class="sxs-lookup"><span data-stu-id="e0416-110">Size, in bytes, of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="e0416-111"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="e0416-111"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="e0416-112">Puntatore a un buffer per contenere il formato stringa a terminazione null del formato ora.</span><span class="sxs-lookup"><span data-stu-id="e0416-112">Pointer to a buffer to contain the null-terminated string form of the time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0416-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e0416-113">Return Value</span></span>

<span data-ttu-id="e0416-114">Restituisce un Integer che corrisponde alla costante MCI che definisce il formato dell'ora.</span><span class="sxs-lookup"><span data-stu-id="e0416-114">Returns an integer corresponding to the MCI constant defining the time format.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0416-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="e0416-115">Remarks</span></span>

<span data-ttu-id="e0416-116">Se la stringa di formato dell'ora è più lunga del buffer restituito, MCIWnd tronca la stringa.</span><span class="sxs-lookup"><span data-stu-id="e0416-116">If the time format string is longer than the return buffer, MCIWnd truncates the string.</span></span>

<span data-ttu-id="e0416-117">Un dispositivo MCI può supportare uno o più dei seguenti formati di ora.</span><span class="sxs-lookup"><span data-stu-id="e0416-117">An MCI device can support one or more of the following time formats.</span></span>



| <span data-ttu-id="e0416-118">Formato ora</span><span class="sxs-lookup"><span data-stu-id="e0416-118">Time format</span></span>                      | <span data-ttu-id="e0416-119">Costante MCI</span><span class="sxs-lookup"><span data-stu-id="e0416-119">MCI constant</span></span>               |
|----------------------------------|----------------------------|
| <span data-ttu-id="e0416-120">Byte</span><span class="sxs-lookup"><span data-stu-id="e0416-120">Bytes</span></span>                            | <span data-ttu-id="e0416-121">\_byte in formato MCI \_</span><span class="sxs-lookup"><span data-stu-id="e0416-121">MCI\_FORMAT\_BYTES</span></span>         |
| <span data-ttu-id="e0416-122">Frame</span><span class="sxs-lookup"><span data-stu-id="e0416-122">Frames</span></span>                           | <span data-ttu-id="e0416-123">\_frame di formato MCI \_</span><span class="sxs-lookup"><span data-stu-id="e0416-123">MCI\_FORMAT\_FRAMES</span></span>        |
| <span data-ttu-id="e0416-124">Ore, minuti, secondi</span><span class="sxs-lookup"><span data-stu-id="e0416-124">Hours, minutes, seconds</span></span>          | <span data-ttu-id="e0416-125">\_formato MCI \_ HMS</span><span class="sxs-lookup"><span data-stu-id="e0416-125">MCI\_FORMAT\_HMS</span></span>           |
| <span data-ttu-id="e0416-126">Millisecondi</span><span class="sxs-lookup"><span data-stu-id="e0416-126">Milliseconds</span></span>                     | <span data-ttu-id="e0416-127">\_ \_ millisecondi formato MCI</span><span class="sxs-lookup"><span data-stu-id="e0416-127">MCI\_FORMAT\_MILLISECONDS</span></span>  |
| <span data-ttu-id="e0416-128">Minuti, secondi, fotogrammi</span><span class="sxs-lookup"><span data-stu-id="e0416-128">Minutes, seconds, frames</span></span>         | <span data-ttu-id="e0416-129">\_MSF formato \_ MCI</span><span class="sxs-lookup"><span data-stu-id="e0416-129">MCI\_FORMAT\_MSF</span></span>           |
| <span data-ttu-id="e0416-130">Esempi</span><span class="sxs-lookup"><span data-stu-id="e0416-130">Samples</span></span>                          | <span data-ttu-id="e0416-131">\_esempi di formato MCI \_</span><span class="sxs-lookup"><span data-stu-id="e0416-131">MCI\_FORMAT\_SAMPLES</span></span>       |
| <span data-ttu-id="e0416-132">SMPTE 24</span><span class="sxs-lookup"><span data-stu-id="e0416-132">SMPTE 24</span></span>                         | <span data-ttu-id="e0416-133">\_Formato MCI \_ \_ 24</span><span class="sxs-lookup"><span data-stu-id="e0416-133">MCI\_FORMAT\_SMPTE\_24</span></span>     |
| <span data-ttu-id="e0416-134">SMPTE 25</span><span class="sxs-lookup"><span data-stu-id="e0416-134">SMPTE 25</span></span>                         | <span data-ttu-id="e0416-135">\_Formato MCI \_ \_ 25</span><span class="sxs-lookup"><span data-stu-id="e0416-135">MCI\_FORMAT\_SMPTE\_25</span></span>     |
| <span data-ttu-id="e0416-136">Rilascio SMPTE 30</span><span class="sxs-lookup"><span data-stu-id="e0416-136">SMPTE 30 drop</span></span>                    | <span data-ttu-id="e0416-137">\_Formato MCI \_ \_ 30DROP</span><span class="sxs-lookup"><span data-stu-id="e0416-137">MCI\_FORMAT\_SMPTE\_30DROP</span></span> |
| <span data-ttu-id="e0416-138">SMPTE 30 (non-drop)</span><span class="sxs-lookup"><span data-stu-id="e0416-138">SMPTE 30 (non-drop)</span></span>              | <span data-ttu-id="e0416-139">\_Formato MCI \_ \_ 30</span><span class="sxs-lookup"><span data-stu-id="e0416-139">MCI\_FORMAT\_SMPTE\_30</span></span>     |
| <span data-ttu-id="e0416-140">Tracce, minuti, secondi, frame</span><span class="sxs-lookup"><span data-stu-id="e0416-140">Tracks, minutes, seconds, frames</span></span> | <span data-ttu-id="e0416-141">\_formato MCI \_ TMSF</span><span class="sxs-lookup"><span data-stu-id="e0416-141">MCI\_FORMAT\_TMSF</span></span>          |



 

## <a name="requirements"></a><span data-ttu-id="e0416-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0416-142">Requirements</span></span>



| <span data-ttu-id="e0416-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0416-143">Requirement</span></span> | <span data-ttu-id="e0416-144">Valore</span><span class="sxs-lookup"><span data-stu-id="e0416-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e0416-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e0416-145">Minimum supported client</span></span><br/> | <span data-ttu-id="e0416-146">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e0416-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e0416-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e0416-147">Minimum supported server</span></span><br/> | <span data-ttu-id="e0416-148">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e0416-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e0416-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e0416-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0416-150"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0416-150"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0416-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e0416-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0416-152">**MCIWndGetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="e0416-152">**MCIWndGetTimeFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat)
</dt> </dl>

 

 






---
title: Messaggio di MCIWNDM_SETTIMEFORMAT (VFW. h)
description: Il \_ messaggio MCIWNDM SETTIMEFORMAT imposta il formato dell'ora di un dispositivo MCI. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndSetTimeFormat.
ms.assetid: 7de82094-6d35-44fd-88e7-ebd18a558cfd
keywords:
- MCIWNDM_SETTIMEFORMAT messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_SETTIMEFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcec1f0db5accad93211bf1eb6f1c9297e2b9f33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517415"
---
# <a name="mciwndm_settimeformat-message"></a><span data-ttu-id="ed131-105">\_Messaggio MCIWNDM SETTIMEFORMAT</span><span class="sxs-lookup"><span data-stu-id="ed131-105">MCIWNDM\_SETTIMEFORMAT message</span></span>

<span data-ttu-id="ed131-106">Il messaggio **MCIWNDM \_ SETTIMEFORMAT** imposta il formato dell'ora di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="ed131-106">The **MCIWNDM\_SETTIMEFORMAT** message sets the time format of an MCI device.</span></span> <span data-ttu-id="ed131-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndSetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat) .</span><span class="sxs-lookup"><span data-stu-id="ed131-107">You can send this message explicitly or by using the [**MCIWndSetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat) macro.</span></span>


```C++
MCIWNDM_SETTIMEFORMAT 
wParam = 0; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a><span data-ttu-id="ed131-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ed131-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed131-109"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="ed131-109"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="ed131-110">Puntatore a un buffer contenente la stringa con terminazione null che indica il formato dell'ora.</span><span class="sxs-lookup"><span data-stu-id="ed131-110">Pointer to a buffer containing the null-terminated string indicating the time format.</span></span> <span data-ttu-id="ed131-111">Specificare "frame" per impostare il formato dell'ora su frame oppure "MS" per impostare il formato dell'ora su millisecondi.</span><span class="sxs-lookup"><span data-stu-id="ed131-111">Specify "frames" to set the time format to frames, or "ms" to set the time format to milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed131-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ed131-112">Return Value</span></span>

<span data-ttu-id="ed131-113">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="ed131-113">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed131-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="ed131-114">Remarks</span></span>

<span data-ttu-id="ed131-115">Un'applicazione può specificare formati di ora diversi da frame o millisecondi purché i formati siano supportati dal dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="ed131-115">An application can specify time formats other than frames or milliseconds as long as the formats are supported by the MCI device.</span></span> <span data-ttu-id="ed131-116">I formati non continui, ad esempio Tracks e SMPTE, possono causare un comportamento anomalo del TrackBar.</span><span class="sxs-lookup"><span data-stu-id="ed131-116">Noncontinuous formats, such as tracks and SMPTE, can cause the trackbar to behave erratically.</span></span> <span data-ttu-id="ed131-117">Per questi formati temporali, potrebbe essere necessario disattivare la barra degli strumenti usando la macro [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) e specificando lo \_ stile della finestra NOPLAYBAR MCIWNDF.</span><span class="sxs-lookup"><span data-stu-id="ed131-117">For these time formats, you might want to turn off the toolbar by using the [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) macro and specifying the MCIWNDF\_NOPLAYBAR window style.</span></span>

<span data-ttu-id="ed131-118">Se si desidera impostare il formato dell'ora su frame o millisecondi, è possibile utilizzare anche la macro [**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) o [**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) .</span><span class="sxs-lookup"><span data-stu-id="ed131-118">If you want to set the time format to frames or milliseconds, you can also use the [**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) or [**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) macro.</span></span> <span data-ttu-id="ed131-119">Per un elenco dei formati di ora, vedere la macro [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) .</span><span class="sxs-lookup"><span data-stu-id="ed131-119">For a list of time formats, see the [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed131-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed131-120">Requirements</span></span>



| <span data-ttu-id="ed131-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed131-121">Requirement</span></span> | <span data-ttu-id="ed131-122">Valore</span><span class="sxs-lookup"><span data-stu-id="ed131-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ed131-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed131-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ed131-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ed131-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ed131-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed131-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ed131-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ed131-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ed131-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ed131-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed131-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed131-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed131-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ed131-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed131-130">**MCIWndChangeStyles**</span><span class="sxs-lookup"><span data-stu-id="ed131-130">**MCIWndChangeStyles**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles)
</dt> <dt>

[<span data-ttu-id="ed131-131">**MCIWndGetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="ed131-131">**MCIWndGetTimeFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat)
</dt> <dt>

[<span data-ttu-id="ed131-132">**MCIWndSetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="ed131-132">**MCIWndSetTimeFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat)
</dt> <dt>

[<span data-ttu-id="ed131-133">**MCIWndUseFrames**</span><span class="sxs-lookup"><span data-stu-id="ed131-133">**MCIWndUseFrames**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes)
</dt> <dt>

[<span data-ttu-id="ed131-134">**MCIWndUseTime**</span><span class="sxs-lookup"><span data-stu-id="ed131-134">**MCIWndUseTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime)
</dt> </dl>

 

 






---
title: Messaggio di MCIWNDM_SETREPEAT (VFW. h)
description: Il \_ messaggio MCIWNDM di rerepeat imposta il flag di ripetizione associato alla riproduzione continua.
ms.assetid: 9a8da201-9ce8-4b6c-8b76-cd9e1356c75d
keywords:
- MCIWNDM_SETREPEAT messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_SETREPEAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aeae2ac3cb57f8ddbb2343ee3f42d30fa8def370
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874141"
---
# <a name="mciwndm_setrepeat-message"></a><span data-ttu-id="33c18-104">MCIWNDM \_ messaggio di ripetizione</span><span class="sxs-lookup"><span data-stu-id="33c18-104">MCIWNDM\_SETREPEAT message</span></span>

<span data-ttu-id="33c18-105">Il messaggio **MCIWNDM di \_ rerepeat** imposta il flag di ripetizione associato alla riproduzione continua.</span><span class="sxs-lookup"><span data-stu-id="33c18-105">The **MCIWNDM\_SETREPEAT** message sets the repeat flag associated with continuous playback.</span></span> <span data-ttu-id="33c18-106">Il **messaggio \_ MCIWNDM** viene utilizzato insieme al comando [MCI \_ Play](mci-play.md) per fornire un ciclo di riproduzione continuo.</span><span class="sxs-lookup"><span data-stu-id="33c18-106">The **MCIWNDM\_SETREPEAT** message works in conjunction with the [MCI\_PLAY](mci-play.md) command to provide a continuous playback loop.</span></span> <span data-ttu-id="33c18-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) .</span><span class="sxs-lookup"><span data-stu-id="33c18-107">You can send this message explicitly or by using the [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) macro.</span></span>


```C++
MCIWNDM_SETREPEAT 
wParam = 0; 
lParam = (LPARAM) (BOOL) f; 
```



## <a name="parameters"></a><span data-ttu-id="33c18-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="33c18-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33c18-109"><span id="f"></span><span id="F"></span>*f*</span><span class="sxs-lookup"><span data-stu-id="33c18-109"><span id="f"></span><span id="F"></span>*f*</span></span>
</dt> <dd>

<span data-ttu-id="33c18-110">Nuovo stato del flag di ripetizione.</span><span class="sxs-lookup"><span data-stu-id="33c18-110">New state of the repeat flag.</span></span> <span data-ttu-id="33c18-111">Specificare **true** per attivare la riproduzione continua.</span><span class="sxs-lookup"><span data-stu-id="33c18-111">Specify **TRUE** to turn on continuous playback.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33c18-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="33c18-112">Return Value</span></span>

<span data-ttu-id="33c18-113">Restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="33c18-113">Returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="33c18-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="33c18-114">Remarks</span></span>

<span data-ttu-id="33c18-115">Attualmente, MCIAVI è l'unico dispositivo che supporta la riproduzione continua.</span><span class="sxs-lookup"><span data-stu-id="33c18-115">Currently, MCIAVI is the only device that supports continuous playback.</span></span>

## <a name="requirements"></a><span data-ttu-id="33c18-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="33c18-116">Requirements</span></span>



| <span data-ttu-id="33c18-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="33c18-117">Requirement</span></span> | <span data-ttu-id="33c18-118">Valore</span><span class="sxs-lookup"><span data-stu-id="33c18-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="33c18-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33c18-119">Minimum supported client</span></span><br/> | <span data-ttu-id="33c18-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="33c18-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="33c18-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33c18-121">Minimum supported server</span></span><br/> | <span data-ttu-id="33c18-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="33c18-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="33c18-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="33c18-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="33c18-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="33c18-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33c18-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33c18-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33c18-126">\_riproduzione MCI</span><span class="sxs-lookup"><span data-stu-id="33c18-126">MCI\_PLAY</span></span>](mci-play.md)
</dt> <dt>

[<span data-ttu-id="33c18-127">**MCIWndSetRepeat**</span><span class="sxs-lookup"><span data-stu-id="33c18-127">**MCIWndSetRepeat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat)
</dt> </dl>

 

 






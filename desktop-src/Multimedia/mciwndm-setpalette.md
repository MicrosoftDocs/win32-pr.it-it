---
title: Messaggio di MCIWNDM_SETPALETTE (VFW. h)
description: Il \_ messaggio MCIWNDM SEtavolozza Invia un handle della tavolozza al dispositivo MCI associato alla finestra MCIWnd. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndSetPalette.
ms.assetid: d2399cb7-d83c-465c-b02f-e6a016c28ae3
keywords:
- MCIWNDM_SETPALETTE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_SETPALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba7e354082de4fc15f4179555a8b635b9426af90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477830"
---
# <a name="mciwndm_setpalette-message"></a><span data-ttu-id="11e9f-105">\_Messaggio MCIWNDM SEpalette</span><span class="sxs-lookup"><span data-stu-id="11e9f-105">MCIWNDM\_SETPALETTE message</span></span>

<span data-ttu-id="11e9f-106">Il messaggio **MCIWNDM \_ setavolozza** Invia un handle della tavolozza al dispositivo MCI associato alla finestra MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="11e9f-106">The **MCIWNDM\_SETPALETTE** message sends a palette handle to the MCI device associated with the MCIWnd window.</span></span> <span data-ttu-id="11e9f-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndSetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette) .</span><span class="sxs-lookup"><span data-stu-id="11e9f-107">You can send this message explicitly or by using the [**MCIWndSetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette) macro.</span></span>


```C++
MCIWNDM_SETPALETTE 
wParam = (WPARAM) (HPALETTE) hpal; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="11e9f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="11e9f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11e9f-109"><span id="hpal"></span><span id="HPAL"></span>*hpal*</span><span class="sxs-lookup"><span data-stu-id="11e9f-109"><span id="hpal"></span><span id="HPAL"></span>*hpal*</span></span>
</dt> <dd>

<span data-ttu-id="11e9f-110">Handle tavolozza.</span><span class="sxs-lookup"><span data-stu-id="11e9f-110">Palette handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11e9f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="11e9f-111">Return Value</span></span>

<span data-ttu-id="11e9f-112">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="11e9f-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="11e9f-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="11e9f-113">Requirements</span></span>



| <span data-ttu-id="11e9f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="11e9f-114">Requirement</span></span> | <span data-ttu-id="11e9f-115">Valore</span><span class="sxs-lookup"><span data-stu-id="11e9f-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="11e9f-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="11e9f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="11e9f-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="11e9f-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="11e9f-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="11e9f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="11e9f-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="11e9f-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="11e9f-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="11e9f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="11e9f-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="11e9f-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11e9f-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="11e9f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11e9f-123">**MCIWndSetPalette**</span><span class="sxs-lookup"><span data-stu-id="11e9f-123">**MCIWndSetPalette**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette)
</dt> </dl>

 

 






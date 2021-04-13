---
title: Messaggio di WM_CAP_DRIVER_GET_CAPS (VFW. h)
description: Il \_ messaggio WM Cap \_ driver \_ get \_ Caps restituisce le funzionalità hardware del driver di acquisizione attualmente connesso a una finestra di acquisizione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capDriverGetCaps.
ms.assetid: 898a800c-1109-47cd-bcc9-cb61d86a4a2e
keywords:
- WM_CAP_DRIVER_GET_CAPS messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_GET_CAPS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 027e530be82c76afebc343ceebe4905daef9b126
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518958"
---
# <a name="wm_cap_driver_get_caps-message"></a><span data-ttu-id="9104f-105">\_ \_ \_ Messaggio Caps Get driver di WM Cap \_</span><span class="sxs-lookup"><span data-stu-id="9104f-105">WM\_CAP\_DRIVER\_GET\_CAPS message</span></span>

<span data-ttu-id="9104f-106">Il messaggio **WM \_ Cap \_ driver \_ get \_ Caps** restituisce le funzionalità hardware del driver di acquisizione attualmente connesso a una finestra di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="9104f-106">The **WM\_CAP\_DRIVER\_GET\_CAPS** message returns the hardware capabilities of the capture driver currently connected to a capture window.</span></span> <span data-ttu-id="9104f-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) .</span><span class="sxs-lookup"><span data-stu-id="9104f-107">You can send this message explicitly or by using the [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) macro.</span></span>


```C++
WM_CAP_DRIVER_GET_CAPS 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPDRIVERCAPS) (psCaps); 
```



## <a name="parameters"></a><span data-ttu-id="9104f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9104f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9104f-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="9104f-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="9104f-110">Dimensione, in byte, della struttura a cui fa riferimento **s**.</span><span class="sxs-lookup"><span data-stu-id="9104f-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="9104f-111"><span id="psCaps"></span><span id="pscaps"></span><span id="PSCAPS"></span>*psCaps*</span><span class="sxs-lookup"><span data-stu-id="9104f-111"><span id="psCaps"></span><span id="pscaps"></span><span id="PSCAPS"></span>*psCaps*</span></span>
</dt> <dd>

<span data-ttu-id="9104f-112">Puntatore alla struttura [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) per contenere le funzionalità hardware.</span><span class="sxs-lookup"><span data-stu-id="9104f-112">Pointer to the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure to contain the hardware capabilities.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9104f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9104f-113">Return Value</span></span>

<span data-ttu-id="9104f-114">Restituisce **true** se l'operazione ha esito positivo o **false** se la finestra di acquisizione non è connessa a un driver di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="9104f-114">Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.</span></span>

## <a name="remarks"></a><span data-ttu-id="9104f-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="9104f-115">Remarks</span></span>

<span data-ttu-id="9104f-116">Le funzionalità restituite in [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) sono costanti per un determinato driver di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="9104f-116">The capabilities returned in [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) are constant for a given capture driver.</span></span> <span data-ttu-id="9104f-117">Le applicazioni devono recuperare queste informazioni una volta quando il driver di acquisizione viene connesso per la prima volta a una finestra di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="9104f-117">Applications need to retrieve this information once when the capture driver is first connected to a capture window.</span></span>

## <a name="requirements"></a><span data-ttu-id="9104f-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9104f-118">Requirements</span></span>



| <span data-ttu-id="9104f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9104f-119">Requirement</span></span> | <span data-ttu-id="9104f-120">Valore</span><span class="sxs-lookup"><span data-stu-id="9104f-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9104f-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9104f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9104f-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9104f-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="9104f-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9104f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9104f-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9104f-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9104f-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9104f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9104f-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="9104f-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9104f-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9104f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9104f-128">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="9104f-128">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="9104f-129">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="9104f-129">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 






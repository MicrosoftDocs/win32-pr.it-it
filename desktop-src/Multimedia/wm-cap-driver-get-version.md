---
title: Messaggio di WM_CAP_DRIVER_GET_VERSION (VFW. h)
description: Il \_ messaggio WM Cap \_ driver \_ get \_ Version restituisce le informazioni sulla versione del driver di acquisizione connesso a una finestra di acquisizione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capDriverGetVersion.
ms.assetid: 762ebe7e-0d09-46ea-ab17-86061f0bd8f9
keywords:
- WM_CAP_DRIVER_GET_VERSION messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_GET_VERSION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ced70f2d0159ef4bbad3f2d7a8027c30b2c71a5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302346"
---
# <a name="wm_cap_driver_get_version-message"></a><span data-ttu-id="6c10d-105">\_Messaggio di \_ versione del driver WM Cap \_ get \_</span><span class="sxs-lookup"><span data-stu-id="6c10d-105">WM\_CAP\_DRIVER\_GET\_VERSION message</span></span>

<span data-ttu-id="6c10d-106">Il messaggio **WM \_ Cap \_ driver \_ get \_ Version** restituisce le informazioni sulla versione del driver di acquisizione connesso a una finestra di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="6c10d-106">The **WM\_CAP\_DRIVER\_GET\_VERSION** message returns the version information of the capture driver connected to a capture window.</span></span> <span data-ttu-id="6c10d-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capDriverGetVersion**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion) .</span><span class="sxs-lookup"><span data-stu-id="6c10d-107">You can send this message explicitly or by using the [**capDriverGetVersion**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion) macro.</span></span>


```C++
WM_CAP_DRIVER_GET_VERSION 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szVer); 
```



## <a name="parameters"></a><span data-ttu-id="6c10d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6c10d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c10d-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="6c10d-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="6c10d-110">Dimensione, in byte, del buffer definito dall'applicazione a cui fa riferimento **szVer**.</span><span class="sxs-lookup"><span data-stu-id="6c10d-110">Size, in bytes, of the application-defined buffer referenced by **szVer**.</span></span>

</dd> <dt>

<span data-ttu-id="6c10d-111"><span id="szVer"></span><span id="szver"></span><span id="SZVER"></span>*szVer*</span><span class="sxs-lookup"><span data-stu-id="6c10d-111"><span id="szVer"></span><span id="szver"></span><span id="SZVER"></span>*szVer*</span></span>
</dt> <dd>

<span data-ttu-id="6c10d-112">Puntatore a un buffer definito dall'applicazione utilizzato per restituire le informazioni sulla versione come stringa con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="6c10d-112">Pointer to an application-defined buffer used to return the version information as a null-terminated string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c10d-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6c10d-113">Return Value</span></span>

<span data-ttu-id="6c10d-114">Restituisce **true** se l'operazione ha esito positivo o **false** se la finestra di acquisizione non è connessa a un driver di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="6c10d-114">Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c10d-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="6c10d-115">Remarks</span></span>

<span data-ttu-id="6c10d-116">Le informazioni sulla versione sono una stringa di testo recuperata dall'area delle risorse del driver.</span><span class="sxs-lookup"><span data-stu-id="6c10d-116">The version information is a text string retrieved from the driver's resource area.</span></span> <span data-ttu-id="6c10d-117">Le applicazioni devono allocare circa 40 byte per questa stringa.</span><span class="sxs-lookup"><span data-stu-id="6c10d-117">Applications should allocate approximately 40 bytes for this string.</span></span> <span data-ttu-id="6c10d-118">Se le informazioni sulla versione non sono disponibili, viene restituita una stringa **null** .</span><span class="sxs-lookup"><span data-stu-id="6c10d-118">If version information is not available, a **NULL** string is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c10d-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6c10d-119">Requirements</span></span>



| <span data-ttu-id="6c10d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c10d-120">Requirement</span></span> | <span data-ttu-id="6c10d-121">Valore</span><span class="sxs-lookup"><span data-stu-id="6c10d-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6c10d-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c10d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6c10d-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6c10d-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6c10d-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c10d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6c10d-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6c10d-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6c10d-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6c10d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c10d-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c10d-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c10d-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6c10d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c10d-129">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="6c10d-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="6c10d-130">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="6c10d-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 






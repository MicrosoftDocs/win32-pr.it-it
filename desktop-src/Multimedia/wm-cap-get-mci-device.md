---
title: Messaggio di WM_CAP_GET_MCI_DEVICE (VFW. h)
description: Il \_ messaggio WM Cap \_ get \_ MCI \_ Device Recupera il nome di un dispositivo MCI precedentemente impostato con il \_ messaggio di dispositivo WM Cap \_ set \_ MCI \_ . È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capGetMCIDeviceName.
ms.assetid: c5d7d955-ab6a-4959-b79e-9ff35a282ba2
keywords:
- WM_CAP_GET_MCI_DEVICE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_GET_MCI_DEVICE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0960ff9aa1366802611f444383212c4bcc45bcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475071"
---
# <a name="wm_cap_get_mci_device-message"></a><span data-ttu-id="56492-105">\_Messaggio del dispositivo WM Cap \_ get \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="56492-105">WM\_CAP\_GET\_MCI\_DEVICE message</span></span>

<span data-ttu-id="56492-106">Il messaggio **WM \_ Cap \_ get \_ MCI \_ Device** Recupera il nome di un dispositivo MCI precedentemente impostato con il messaggio di [**\_ dispositivo WM Cap \_ set \_ MCI \_**](wm-cap-set-mci-device.md) .</span><span class="sxs-lookup"><span data-stu-id="56492-106">The **WM\_CAP\_GET\_MCI\_DEVICE** message retrieves the name of an MCI device previously set with the [**WM\_CAP\_SET\_MCI\_DEVICE**](wm-cap-set-mci-device.md) message.</span></span> <span data-ttu-id="56492-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capGetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capgetmcidevicename) .</span><span class="sxs-lookup"><span data-stu-id="56492-107">You can send this message explicitly or by using the [**capGetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capgetmcidevicename) macro.</span></span>


```C++
WM_CAP_GET_MCI_DEVICE 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="56492-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="56492-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56492-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="56492-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="56492-110">Lunghezza, in byte, del buffer a cui fa riferimento **szName**.</span><span class="sxs-lookup"><span data-stu-id="56492-110">Length, in bytes, of the buffer referenced by **szName**.</span></span>

</dd> <dt>

<span data-ttu-id="56492-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="56492-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="56492-112">Puntatore a una stringa con terminazione null che contiene il nome del dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="56492-112">Pointer to a null-terminated string that contains the MCI device name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56492-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="56492-113">Return Value</span></span>

<span data-ttu-id="56492-114">Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="56492-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="56492-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56492-115">Requirements</span></span>



| <span data-ttu-id="56492-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="56492-116">Requirement</span></span> | <span data-ttu-id="56492-117">Valore</span><span class="sxs-lookup"><span data-stu-id="56492-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="56492-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56492-118">Minimum supported client</span></span><br/> | <span data-ttu-id="56492-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="56492-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="56492-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56492-120">Minimum supported server</span></span><br/> | <span data-ttu-id="56492-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="56492-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="56492-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="56492-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="56492-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="56492-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56492-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="56492-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56492-125">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="56492-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="56492-126">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="56492-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 






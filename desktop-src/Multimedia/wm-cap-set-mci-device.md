---
title: Messaggio di WM_CAP_SET_MCI_DEVICE (VFW. h)
description: Il \_ messaggio del dispositivo WM Cap \_ set \_ MCI \_ specifica il nome del dispositivo video MCI da usare per l'acquisizione dei dati. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capSetMCIDeviceName.
ms.assetid: 83fdf567-ceb2-45aa-8529-433a5c64ac0a
keywords:
- WM_CAP_SET_MCI_DEVICE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_SET_MCI_DEVICE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86187f3357bf72866e05b497332454c10bcd2fd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740055"
---
# <a name="wm_cap_set_mci_device-message"></a><span data-ttu-id="f3ae1-105">Messaggio di set di WM \_ Cap \_ set \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="f3ae1-105">WM\_CAP\_SET\_MCI\_DEVICE message</span></span>

<span data-ttu-id="f3ae1-106">Il messaggio del **\_ dispositivo WM Cap \_ set \_ MCI \_** specifica il nome del dispositivo video MCI da usare per l'acquisizione dei dati.</span><span class="sxs-lookup"><span data-stu-id="f3ae1-106">The **WM\_CAP\_SET\_MCI\_DEVICE** message specifies the name of the MCI video device to be used to capture data.</span></span> <span data-ttu-id="f3ae1-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capSetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capsetmcidevicename) .</span><span class="sxs-lookup"><span data-stu-id="f3ae1-107">You can send this message explicitly or by using the [**capSetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capsetmcidevicename) macro.</span></span>


```C++
WM_CAP_SET_MCI_DEVICE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="f3ae1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f3ae1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3ae1-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="f3ae1-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="f3ae1-110">Puntatore a una stringa con terminazione null che contiene il nome del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3ae1-110">Pointer to a null-terminated string containing the name of the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3ae1-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f3ae1-111">Return Value</span></span>

<span data-ttu-id="f3ae1-112">Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f3ae1-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3ae1-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="f3ae1-113">Remarks</span></span>

<span data-ttu-id="f3ae1-114">Questo messaggio archivia il nome del dispositivo MCI in una struttura interna.</span><span class="sxs-lookup"><span data-stu-id="f3ae1-114">This message stores the MCI device name in an internal structure.</span></span> <span data-ttu-id="f3ae1-115">Non apre né accede al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3ae1-115">It does not open or access the device.</span></span> <span data-ttu-id="f3ae1-116">Il nome del dispositivo predefinito è **null**.</span><span class="sxs-lookup"><span data-stu-id="f3ae1-116">The default device name is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3ae1-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f3ae1-117">Requirements</span></span>



| <span data-ttu-id="f3ae1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3ae1-118">Requirement</span></span> | <span data-ttu-id="f3ae1-119">Valore</span><span class="sxs-lookup"><span data-stu-id="f3ae1-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f3ae1-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3ae1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f3ae1-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f3ae1-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f3ae1-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3ae1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f3ae1-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f3ae1-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f3ae1-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f3ae1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3ae1-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3ae1-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3ae1-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f3ae1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3ae1-127">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="f3ae1-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="f3ae1-128">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="f3ae1-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 






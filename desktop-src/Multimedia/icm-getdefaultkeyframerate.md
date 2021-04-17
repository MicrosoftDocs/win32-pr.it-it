---
title: Messaggio di ICM_GETDEFAULTKEYFRAMERATE (VFW. h)
description: Il \_ messaggio MCI GETDEFAULTKEYFRAMERATE esegue una query su un driver di compressione video per la spaziatura dei fotogrammi chiave predefinita o preferita. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICGetDefaulteyFrameRate.
ms.assetid: 2ebe37cc-3ec2-4b52-bd8f-71c44b704647
keywords:
- ICM_GETDEFAULTKEYFRAMERATE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_GETDEFAULTKEYFRAMERATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64f2796ca1c2de10222330217a0e1deb7883baa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400680"
---
# <a name="icm_getdefaultkeyframerate-message"></a><span data-ttu-id="3876a-105">\_Messaggio GETDEFAULTKEYFRAMERATE ICM</span><span class="sxs-lookup"><span data-stu-id="3876a-105">ICM\_GETDEFAULTKEYFRAMERATE message</span></span>

<span data-ttu-id="3876a-106">Il messaggio **MCI \_ GETDEFAULTKEYFRAMERATE** esegue una query su un driver di compressione video per la spaziatura dei fotogrammi chiave predefinita o preferita.</span><span class="sxs-lookup"><span data-stu-id="3876a-106">The **ICM\_GETDEFAULTKEYFRAMERATE** message queries a video compression driver for its default (or preferred) key-frame spacing.</span></span> <span data-ttu-id="3876a-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICGetDefaulteyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) .</span><span class="sxs-lookup"><span data-stu-id="3876a-107">You can send this message explicitly or by using the [**ICGetDefaulteyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) macro.</span></span>


```C++
ICM_GETDEFAULTKEYFRAMERATE 
wParam = (DWORD_PTR) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="3876a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3876a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3876a-109"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span><span class="sxs-lookup"><span data-stu-id="3876a-109"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span></span>
</dt> <dd>

<span data-ttu-id="3876a-110">Indirizzo per contenere la spaziatura dei fotogrammi chiave preferita.</span><span class="sxs-lookup"><span data-stu-id="3876a-110">Address to contain the preferred key-frame spacing.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3876a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3876a-111">Return Value</span></span>

<span data-ttu-id="3876a-112">Restituisce ICERR \_ OK se il driver supporta questo messaggio o ICERR non \_ supportato in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="3876a-112">Returns ICERR\_OK if the driver supports this message or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3876a-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3876a-113">Requirements</span></span>



| <span data-ttu-id="3876a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3876a-114">Requirement</span></span> | <span data-ttu-id="3876a-115">Valore</span><span class="sxs-lookup"><span data-stu-id="3876a-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3876a-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3876a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3876a-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3876a-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3876a-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3876a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3876a-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3876a-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3876a-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3876a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3876a-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="3876a-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3876a-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3876a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3876a-123">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="3876a-123">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="3876a-124">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="3876a-124">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 






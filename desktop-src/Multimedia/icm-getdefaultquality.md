---
title: Messaggio di ICM_GETDEFAULTQUALITY (VFW. h)
description: Il \_ messaggio MCI GETDEFAULTQUALITY esegue una query su un driver di compressione video per fornire l'impostazione di qualità predefinita. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICGetDefaultQuality.
ms.assetid: bba7f451-52c2-4684-a7c9-e4b05cb946c5
keywords:
- ICM_GETDEFAULTQUALITY messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_GETDEFAULTQUALITY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4350539851ca720e3538d297f955a56fedfc4a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475700"
---
# <a name="icm_getdefaultquality-message"></a><span data-ttu-id="6e197-105">\_Messaggio GETDEFAULTQUALITY ICM</span><span class="sxs-lookup"><span data-stu-id="6e197-105">ICM\_GETDEFAULTQUALITY message</span></span>

<span data-ttu-id="6e197-106">Il messaggio **MCI \_ GETDEFAULTQUALITY** esegue una query su un driver di compressione video per fornire l'impostazione di qualità predefinita.</span><span class="sxs-lookup"><span data-stu-id="6e197-106">The **ICM\_GETDEFAULTQUALITY** message queries a video compression driver to provide its default quality setting.</span></span> <span data-ttu-id="6e197-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) .</span><span class="sxs-lookup"><span data-stu-id="6e197-107">You can send this message explicitly or by using the [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) macro.</span></span>


```C++
ICM_GETDEFAULTQUALITY 
wParam = (DWORD_PTR) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="6e197-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6e197-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e197-109"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span><span class="sxs-lookup"><span data-stu-id="6e197-109"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span></span>
</dt> <dd>

<span data-ttu-id="6e197-110">Indirizzo per contenere il valore di qualità predefinito.</span><span class="sxs-lookup"><span data-stu-id="6e197-110">Address to contain the default quality value.</span></span> <span data-ttu-id="6e197-111">I valori di qualità variano da 0 a 10.000.</span><span class="sxs-lookup"><span data-stu-id="6e197-111">Quality values range from 0 to 10,000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e197-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6e197-112">Return Value</span></span>

<span data-ttu-id="6e197-113">Restituisce ICERR \_ OK se il driver supporta questo messaggio o ICERR non \_ supportato in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="6e197-113">Returns ICERR\_OK if the driver supports this message or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e197-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6e197-114">Requirements</span></span>



| <span data-ttu-id="6e197-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e197-115">Requirement</span></span> | <span data-ttu-id="6e197-116">Valore</span><span class="sxs-lookup"><span data-stu-id="6e197-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6e197-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e197-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6e197-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6e197-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6e197-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e197-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6e197-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6e197-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6e197-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6e197-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e197-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e197-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e197-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6e197-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e197-124">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="6e197-124">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="6e197-125">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="6e197-125">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 






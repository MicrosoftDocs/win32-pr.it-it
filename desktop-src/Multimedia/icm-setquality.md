---
title: Messaggio di ICM_SETQUALITY (VFW. h)
description: Il \_ messaggio MCI di qualità fornisce un driver di compressione video con un livello di qualità da usare durante la compressione.
ms.assetid: 487ff1de-7178-440a-b38d-0b82a30d7297
keywords:
- ICM_SETQUALITY messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_SETQUALITY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a1523996ad336e64d4b34143cc26cd8d0937d5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400944"
---
# <a name="icm_setquality-message"></a><span data-ttu-id="27d73-104">\_Messaggio di qualità MCI</span><span class="sxs-lookup"><span data-stu-id="27d73-104">ICM\_SETQUALITY message</span></span>

<span data-ttu-id="27d73-105">Il messaggio **MCI di \_ qualità** fornisce un driver di compressione video con un livello di qualità da usare durante la compressione.</span><span class="sxs-lookup"><span data-stu-id="27d73-105">The **ICM\_SETQUALITY** message provides a video compression driver with a quality level to use during compression.</span></span>


```C++
ICM_SETQUALITY 
wParam = (DWORD) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="27d73-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="27d73-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27d73-107"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span><span class="sxs-lookup"><span data-stu-id="27d73-107"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span></span>
</dt> <dd>

<span data-ttu-id="27d73-108">Nuovo valore di qualità.</span><span class="sxs-lookup"><span data-stu-id="27d73-108">New quality value.</span></span> <span data-ttu-id="27d73-109">I valori di qualità variano da 0 a 10.000.</span><span class="sxs-lookup"><span data-stu-id="27d73-109">Quality values range from 0 to 10,000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27d73-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="27d73-110">Return Value</span></span>

<span data-ttu-id="27d73-111">Restituisce ICERR \_ OK se il driver supporta questo messaggio o ICERR non \_ supportato in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="27d73-111">Returns ICERR\_OK if the driver supports this message or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="27d73-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="27d73-112">Requirements</span></span>



| <span data-ttu-id="27d73-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="27d73-113">Requirement</span></span> | <span data-ttu-id="27d73-114">Valore</span><span class="sxs-lookup"><span data-stu-id="27d73-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="27d73-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27d73-115">Minimum supported client</span></span><br/> | <span data-ttu-id="27d73-116">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="27d73-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="27d73-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27d73-117">Minimum supported server</span></span><br/> | <span data-ttu-id="27d73-118">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="27d73-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="27d73-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="27d73-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="27d73-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="27d73-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27d73-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="27d73-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27d73-122">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="27d73-122">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="27d73-123">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="27d73-123">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 






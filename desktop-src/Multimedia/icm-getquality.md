---
title: Messaggio di ICM_GETQUALITY (VFW. h)
description: Il \_ messaggio ICM getquality esegue una query su un driver di compressione video per restituire la relativa impostazione della qualità corrente.
ms.assetid: 8da99a26-7b2a-4118-89e1-7485915cbdc9
keywords:
- ICM_GETQUALITY messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_GETQUALITY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c4fa2a26e1fe5fa111585ce0a59422a2fe9b072
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964989"
---
# <a name="icm_getquality-message"></a><span data-ttu-id="a7b93-104">\_Messaggio ICM GETquality</span><span class="sxs-lookup"><span data-stu-id="a7b93-104">ICM\_GETQUALITY message</span></span>

<span data-ttu-id="a7b93-105">Il messaggio **ICM \_ getquality** esegue una query su un driver di compressione video per restituire la relativa impostazione della qualità corrente.</span><span class="sxs-lookup"><span data-stu-id="a7b93-105">The **ICM\_GETQUALITY** message queries a video compression driver to return its current quality setting.</span></span>


```C++
ICM_GETQUALITY 
wParam = (DWORD) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="a7b93-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a7b93-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7b93-107"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span><span class="sxs-lookup"><span data-stu-id="a7b93-107"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span></span>
</dt> <dd>

<span data-ttu-id="a7b93-108">Indirizzo per contenere il valore di qualità corrente.</span><span class="sxs-lookup"><span data-stu-id="a7b93-108">Address to contain the current quality value.</span></span> <span data-ttu-id="a7b93-109">I valori di qualità variano da 0 a 10.000.</span><span class="sxs-lookup"><span data-stu-id="a7b93-109">Quality values range from 0 to 10,000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7b93-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a7b93-110">Return Value</span></span>

<span data-ttu-id="a7b93-111">Restituisce ICERR \_ OK se il driver supporta questo messaggio o ICERR non \_ supportato in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a7b93-111">Returns ICERR\_OK if the driver supports this message or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7b93-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a7b93-112">Requirements</span></span>



| <span data-ttu-id="a7b93-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7b93-113">Requirement</span></span> | <span data-ttu-id="a7b93-114">Valore</span><span class="sxs-lookup"><span data-stu-id="a7b93-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a7b93-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7b93-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a7b93-116">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a7b93-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="a7b93-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7b93-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a7b93-118">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a7b93-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a7b93-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a7b93-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7b93-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7b93-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7b93-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a7b93-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7b93-122">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="a7b93-122">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="a7b93-123">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="a7b93-123">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 






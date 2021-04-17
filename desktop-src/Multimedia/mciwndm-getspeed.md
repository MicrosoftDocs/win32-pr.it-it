---
title: Messaggio di MCIWNDM_GETSPEED (VFW. h)
description: Il \_ messaggio getspeed di MCIWNDM recupera la velocità di riproduzione di un dispositivo MCI. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndGetSpeed.
ms.assetid: d10a8f88-e85e-449b-8655-bb0832031d59
keywords:
- MCIWNDM_GETSPEED messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_GETSPEED
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c84a8ebb3e97d4543f68f3a237add8eed7706ae2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478928"
---
# <a name="mciwndm_getspeed-message"></a><span data-ttu-id="e6289-105">\_Messaggio GETSPEED MCIWNDM</span><span class="sxs-lookup"><span data-stu-id="e6289-105">MCIWNDM\_GETSPEED message</span></span>

<span data-ttu-id="e6289-106">Il **messaggio \_ getspeed di MCIWNDM** recupera la velocità di riproduzione di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="e6289-106">The **MCIWNDM\_GETSPEED** message retrieves the playback speed of an MCI device.</span></span> <span data-ttu-id="e6289-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndGetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed) .</span><span class="sxs-lookup"><span data-stu-id="e6289-107">You can send this message explicitly or by using the [**MCIWndGetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed) macro.</span></span>


```C++
MCIWNDM_GETSPEED 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="e6289-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e6289-108">Return Value</span></span>

<span data-ttu-id="e6289-109">Restituisce la velocità di riproduzione in caso di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="e6289-109">Returns the playback speed if successful.</span></span> <span data-ttu-id="e6289-110">Il valore della velocità normale è 1000.</span><span class="sxs-lookup"><span data-stu-id="e6289-110">The value for normal speed is 1000.</span></span> <span data-ttu-id="e6289-111">Valori più elevati indicano velocità più elevate, i valori più piccoli indicano velocità più lente.</span><span class="sxs-lookup"><span data-stu-id="e6289-111">Larger values indicate faster speeds, smaller values indicate slower speeds.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6289-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e6289-112">Requirements</span></span>



| <span data-ttu-id="e6289-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6289-113">Requirement</span></span> | <span data-ttu-id="e6289-114">Valore</span><span class="sxs-lookup"><span data-stu-id="e6289-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e6289-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6289-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e6289-116">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e6289-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e6289-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6289-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e6289-118">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e6289-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e6289-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e6289-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6289-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6289-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6289-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e6289-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6289-122">**MCIWndGetSpeed**</span><span class="sxs-lookup"><span data-stu-id="e6289-122">**MCIWndGetSpeed**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed)
</dt> </dl>

 

 






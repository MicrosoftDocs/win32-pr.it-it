---
title: Messaggio di MCIWNDM_SETSPEED (VFW. h)
description: Il \_ messaggio MCIWNDM sespeed imposta la velocità di riproduzione di un dispositivo MCI. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndSetSpeed.
ms.assetid: 7658dd25-dc68-4bd1-b995-df06b509be16
keywords:
- MCIWNDM_SETSPEED messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_SETSPEED
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 282bb3a2e135b674605be55aaccaa455d30edbcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964525"
---
# <a name="mciwndm_setspeed-message"></a><span data-ttu-id="d5509-105">\_Messaggio di velocità MCIWNDM</span><span class="sxs-lookup"><span data-stu-id="d5509-105">MCIWNDM\_SETSPEED message</span></span>

<span data-ttu-id="d5509-106">Il messaggio **MCIWNDM \_ sespeed** imposta la velocità di riproduzione di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="d5509-106">The **MCIWNDM\_SETSPEED** message sets the playback speed of an MCI device.</span></span> <span data-ttu-id="d5509-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndSetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed) .</span><span class="sxs-lookup"><span data-stu-id="d5509-107">You can send this message explicitly or by using the [**MCIWndSetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed) macro.</span></span>


```C++
MCIWNDM_SETSPEED 
wParam = 0; 
lParam = (LPARAM) (UINT) iSpeed; 
```



## <a name="parameters"></a><span data-ttu-id="d5509-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d5509-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5509-109"><span id="iSpeed"></span><span id="ispeed"></span><span id="ISPEED"></span>*iSpeed*</span><span class="sxs-lookup"><span data-stu-id="d5509-109"><span id="iSpeed"></span><span id="ispeed"></span><span id="ISPEED"></span>*iSpeed*</span></span>
</dt> <dd>

<span data-ttu-id="d5509-110">Velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="d5509-110">Playback speed.</span></span> <span data-ttu-id="d5509-111">Specificare 1000 per la velocità normale, i valori maggiori per le velocità più elevate e i valori più bassi per le velocità più lente.</span><span class="sxs-lookup"><span data-stu-id="d5509-111">Specify 1000 for normal speed, larger values for faster speeds, and smaller values for slower speeds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5509-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d5509-112">Return Value</span></span>

<span data-ttu-id="d5509-113">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="d5509-113">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5509-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d5509-114">Requirements</span></span>



| <span data-ttu-id="d5509-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5509-115">Requirement</span></span> | <span data-ttu-id="d5509-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d5509-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d5509-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5509-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d5509-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d5509-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d5509-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5509-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d5509-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d5509-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d5509-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d5509-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5509-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5509-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5509-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d5509-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5509-124">**MCIWndSetSpeed**</span><span class="sxs-lookup"><span data-stu-id="d5509-124">**MCIWndSetSpeed**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed)
</dt> </dl>

 

 






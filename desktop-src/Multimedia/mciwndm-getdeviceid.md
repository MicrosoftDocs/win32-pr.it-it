---
title: Messaggio di MCIWNDM_GETDEVICEID (VFW. h)
description: Il \_ messaggio MCIWNDM GETDEVICEID recupera l'identificatore del dispositivo MCI attualmente aperto da usare con la funzione mciSendCommand. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndGetDeviceID.
ms.assetid: 188f15fa-579a-438e-a812-9a2b684127c0
keywords:
- MCIWNDM_GETDEVICEID messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_GETDEVICEID
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f2271b18dcf8f295594031ab2c7c80dd8dec06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047973"
---
# <a name="mciwndm_getdeviceid-message"></a><span data-ttu-id="3e26d-105">\_Messaggio MCIWNDM GETDEVICEID</span><span class="sxs-lookup"><span data-stu-id="3e26d-105">MCIWNDM\_GETDEVICEID message</span></span>

<span data-ttu-id="3e26d-106">Il messaggio **MCIWNDM \_ GETDEVICEID** recupera l'identificatore del dispositivo MCI attualmente aperto da usare con la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="3e26d-106">The **MCIWNDM\_GETDEVICEID** message retrieves the identifier of the currently open MCI device to use with the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span> <span data-ttu-id="3e26d-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) .</span><span class="sxs-lookup"><span data-stu-id="3e26d-107">You can send this message explicitly or by using the [**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) macro.</span></span>


```C++
MCIWNDM_GETDEVICEID 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="3e26d-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3e26d-108">Return Value</span></span>

<span data-ttu-id="3e26d-109">Restituisce l'identificatore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3e26d-109">Returns the device identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e26d-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e26d-110">Requirements</span></span>



| <span data-ttu-id="3e26d-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e26d-111">Requirement</span></span> | <span data-ttu-id="3e26d-112">Valore</span><span class="sxs-lookup"><span data-stu-id="3e26d-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3e26d-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e26d-113">Minimum supported client</span></span><br/> | <span data-ttu-id="3e26d-114">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3e26d-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3e26d-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e26d-115">Minimum supported server</span></span><br/> | <span data-ttu-id="3e26d-116">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3e26d-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3e26d-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3e26d-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e26d-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e26d-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e26d-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e26d-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="3e26d-120">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3e26d-120">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3e26d-121">**MCIWndGetDeviceID**</span><span class="sxs-lookup"><span data-stu-id="3e26d-121">**MCIWndGetDeviceID**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid)
</dt> </dl>

 


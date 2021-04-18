---
title: Messaggio di MCIWNDM_CAN_PLAY (VFW. h)
description: MCIWNDM è in \_ grado \_ di riprodurre il messaggio determina se un dispositivo MCI può riprodurre un file di dati o un contenuto di un altro tipo. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndCanPlay.
ms.assetid: dbb742b0-b8ab-4b80-96da-c4823a4747c9
keywords:
- MCIWNDM_CAN_PLAY messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_PLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 043a0fc15260f7448df8d009a6b468616244269d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302626"
---
# <a name="mciwndm_can_play-message"></a><span data-ttu-id="27c20-105">MCIWNDM è in \_ grado di \_ riprodurre il messaggio</span><span class="sxs-lookup"><span data-stu-id="27c20-105">MCIWNDM\_CAN\_PLAY message</span></span>

<span data-ttu-id="27c20-106">MCIWNDM è in **\_ grado di \_ riprodurre** il messaggio determina se un dispositivo MCI può riprodurre un file di dati o un contenuto di un altro tipo.</span><span class="sxs-lookup"><span data-stu-id="27c20-106">The **MCIWNDM\_CAN\_PLAY** message determines if an MCI device can play a data file or content of some other kind.</span></span> <span data-ttu-id="27c20-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndCanPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay) .</span><span class="sxs-lookup"><span data-stu-id="27c20-107">You can send this message explicitly or by using the [**MCIWndCanPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay) macro.</span></span>


```C++
MCIWNDM_CAN_PLAY 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="27c20-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="27c20-108">Return Value</span></span>

<span data-ttu-id="27c20-109">Restituisce **true** se il dispositivo supporta la riproduzione dei dati o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="27c20-109">Returns **TRUE** if the device supports playing the data or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="27c20-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="27c20-110">Requirements</span></span>



| <span data-ttu-id="27c20-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="27c20-111">Requirement</span></span> | <span data-ttu-id="27c20-112">Valore</span><span class="sxs-lookup"><span data-stu-id="27c20-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="27c20-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27c20-113">Minimum supported client</span></span><br/> | <span data-ttu-id="27c20-114">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="27c20-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="27c20-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27c20-115">Minimum supported server</span></span><br/> | <span data-ttu-id="27c20-116">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="27c20-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="27c20-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="27c20-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="27c20-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="27c20-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27c20-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="27c20-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27c20-120">**MCIWndCanPlay**</span><span class="sxs-lookup"><span data-stu-id="27c20-120">**MCIWndCanPlay**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay)
</dt> </dl>

 

 






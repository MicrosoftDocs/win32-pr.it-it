---
title: Messaggio di MCIWNDM_PLAYREVERSE (VFW. h)
description: Il \_ messaggio MCIWNDM PLAYREVERSE riproduce il contenuto corrente nella direzione inversa, a partire dalla posizione corrente fino all'inizio del contenuto o fino a quando un altro comando interrompe la riproduzione.
ms.assetid: 93a22454-eca6-453f-abbe-6cf20198dbad
keywords:
- MCIWNDM_PLAYREVERSE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_PLAYREVERSE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84b0a2e230e3c57e8314e455be5dfbc5cea2c013
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104118946"
---
# <a name="mciwndm_playreverse-message"></a><span data-ttu-id="ed567-104">\_Messaggio MCIWNDM PLAYREVERSE</span><span class="sxs-lookup"><span data-stu-id="ed567-104">MCIWNDM\_PLAYREVERSE message</span></span>

<span data-ttu-id="ed567-105">Il messaggio **MCIWNDM \_ PLAYREVERSE** riproduce il contenuto corrente nella direzione inversa, a partire dalla posizione corrente fino all'inizio del contenuto o fino a quando un altro comando interrompe la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="ed567-105">The **MCIWNDM\_PLAYREVERSE** message plays the current content in the reverse direction, beginning at the current position and ending at the beginning of the content or until another command stops playback.</span></span> <span data-ttu-id="ed567-106">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse) .</span><span class="sxs-lookup"><span data-stu-id="ed567-106">You can send this message explicitly or by using the [**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse) macro.</span></span>


```C++
MCIWNDM_PLAYREVERSE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="ed567-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ed567-107">Return Value</span></span>

<span data-ttu-id="ed567-108">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="ed567-108">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed567-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed567-109">Requirements</span></span>



| <span data-ttu-id="ed567-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed567-110">Requirement</span></span> | <span data-ttu-id="ed567-111">Valore</span><span class="sxs-lookup"><span data-stu-id="ed567-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ed567-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed567-112">Minimum supported client</span></span><br/> | <span data-ttu-id="ed567-113">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ed567-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ed567-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed567-114">Minimum supported server</span></span><br/> | <span data-ttu-id="ed567-115">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ed567-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ed567-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ed567-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed567-117"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed567-117"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed567-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ed567-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed567-119">**MCIWndPlayReverse**</span><span class="sxs-lookup"><span data-stu-id="ed567-119">**MCIWndPlayReverse**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse)
</dt> </dl>

 

 






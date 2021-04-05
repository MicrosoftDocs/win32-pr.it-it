---
title: Messaggio di MCIWNDM_PLAYTO (VFW. h)
description: Il \_ messaggio MCIWNDM PlayToSpazio riproduce il contenuto di un dispositivo MCI dalla posizione corrente fino al percorso finale specificato oppure fino a quando un altro comando non interrompe la riproduzione.
ms.assetid: ed940ee7-7b96-47da-99d3-6697f8a2e3d5
keywords:
- MCIWNDM_PLAYTO messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_PLAYTO
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf0104204dc0306615ead91be036459cdf3c11d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120938"
---
# <a name="mciwndm_playto-message"></a><span data-ttu-id="41be8-104">\_Messaggio MCIWNDM PlayToSpazio</span><span class="sxs-lookup"><span data-stu-id="41be8-104">MCIWNDM\_PLAYTO message</span></span>

<span data-ttu-id="41be8-105">Il messaggio **MCIWNDM \_ PlayToSpazio** riproduce il contenuto di un dispositivo MCI dalla posizione corrente fino al percorso finale specificato oppure fino a quando un altro comando non interrompe la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="41be8-105">The **MCIWNDM\_PLAYTO** message plays the content of an MCI device from the current position to the specified ending location or until another command stops playback.</span></span> <span data-ttu-id="41be8-106">Se il percorso finale specificato si trova oltre la fine del contenuto, la riproduzione si interrompe alla fine del contenuto.</span><span class="sxs-lookup"><span data-stu-id="41be8-106">If the specified ending location is beyond the end of the content, playback stops at the end of the content.</span></span> <span data-ttu-id="41be8-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) .</span><span class="sxs-lookup"><span data-stu-id="41be8-107">You can send this message explicitly or by using the [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) macro.</span></span>


```C++
MCIWNDM_PLAYTO 
wParam = 0; 
lParam = (LPARAM) (LONG) lEnd; 
```



## <a name="parameters"></a><span data-ttu-id="41be8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="41be8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41be8-109"><span id="lEnd"></span><span id="lend"></span><span id="LEND"></span>*Prestare*</span><span class="sxs-lookup"><span data-stu-id="41be8-109"><span id="lEnd"></span><span id="lend"></span><span id="LEND"></span>*lEnd*</span></span>
</dt> <dd>

<span data-ttu-id="41be8-110">Posizione finale.</span><span class="sxs-lookup"><span data-stu-id="41be8-110">Ending location.</span></span> <span data-ttu-id="41be8-111">Le unità per la posizione finale dipendono dal formato dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="41be8-111">The units for the ending location depend on the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41be8-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="41be8-112">Return Value</span></span>

<span data-ttu-id="41be8-113">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="41be8-113">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="41be8-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="41be8-114">Remarks</span></span>

<span data-ttu-id="41be8-115">Questa macro viene definita mediante le macro [**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) e [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) , che a loro volta utilizzano il comando [MCI \_ Seek](mci-seek.md) e il messaggio **MCIWNDM \_ PlayToSpazio** .</span><span class="sxs-lookup"><span data-stu-id="41be8-115">This macro is defined using the [**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) and [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) macros, which in turn use the [MCI\_SEEK](mci-seek.md) command and the **MCIWNDM\_PLAYTO** message.</span></span>

<span data-ttu-id="41be8-116">È anche possibile specificare una posizione iniziale e finale per la riproduzione usando la macro [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) .</span><span class="sxs-lookup"><span data-stu-id="41be8-116">You can also specify both a starting and ending location for playback by using the [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="41be8-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41be8-117">Requirements</span></span>



| <span data-ttu-id="41be8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="41be8-118">Requirement</span></span> | <span data-ttu-id="41be8-119">Valore</span><span class="sxs-lookup"><span data-stu-id="41be8-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="41be8-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41be8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="41be8-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="41be8-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="41be8-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41be8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="41be8-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="41be8-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="41be8-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="41be8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="41be8-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="41be8-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41be8-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="41be8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41be8-127">\_ricerca MCI</span><span class="sxs-lookup"><span data-stu-id="41be8-127">MCI\_SEEK</span></span>](mci-seek.md)
</dt> <dt>

[<span data-ttu-id="41be8-128">**MCIWndPlayFromTo**</span><span class="sxs-lookup"><span data-stu-id="41be8-128">**MCIWndPlayFromTo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)
</dt> <dt>

[<span data-ttu-id="41be8-129">**MCIWndPlayTo**</span><span class="sxs-lookup"><span data-stu-id="41be8-129">**MCIWndPlayTo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto)
</dt> <dt>

[<span data-ttu-id="41be8-130">**MCIWndSeek**</span><span class="sxs-lookup"><span data-stu-id="41be8-130">**MCIWndSeek**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndseek)
</dt> </dl>

 

 






---
title: Messaggio di MCIWNDM_PLAYFROM (VFW. h)
description: Il \_ messaggio MCIWNDM PLAYFROM riproduce il contenuto di un dispositivo MCI dal percorso specificato alla fine del contenuto o fino a quando un altro comando interrompe la riproduzione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndPlayFrom.
ms.assetid: 1c47f8eb-2a1b-4671-a9f8-fd6d59a5c7c6
keywords:
- MCIWNDM_PLAYFROM messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_PLAYFROM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c0fa1b3f4b3359e1609b3ba12009fe5879c304a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963872"
---
# <a name="mciwndm_playfrom-message"></a><span data-ttu-id="6a25c-105">\_Messaggio MCIWNDM PLAYFROM</span><span class="sxs-lookup"><span data-stu-id="6a25c-105">MCIWNDM\_PLAYFROM message</span></span>

<span data-ttu-id="6a25c-106">Il messaggio **MCIWNDM \_ PLAYFROM** riproduce il contenuto di un dispositivo MCI dal percorso specificato alla fine del contenuto o fino a quando un altro comando interrompe la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="6a25c-106">The **MCIWNDM\_PLAYFROM** message plays the content of an MCI device from the specified location to the end of the content or until another command stops playback.</span></span> <span data-ttu-id="6a25c-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) .</span><span class="sxs-lookup"><span data-stu-id="6a25c-107">You can send this message explicitly or by using the [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) macro.</span></span>


```C++
MCIWNDM_PLAYFROM 
wParam = 0; 
lParam = (LPARAM) (LONG) lPos; 
```



## <a name="parameters"></a><span data-ttu-id="6a25c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6a25c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a25c-109"><span id="lPos"></span><span id="lpos"></span><span id="LPOS"></span>*lPos*</span><span class="sxs-lookup"><span data-stu-id="6a25c-109"><span id="lPos"></span><span id="lpos"></span><span id="LPOS"></span>*lPos*</span></span>
</dt> <dd>

<span data-ttu-id="6a25c-110">Posizione iniziale.</span><span class="sxs-lookup"><span data-stu-id="6a25c-110">Starting location.</span></span> <span data-ttu-id="6a25c-111">Le unità per la posizione iniziale dipendono dal formato dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="6a25c-111">The units for the starting location depend on the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a25c-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6a25c-112">Return Value</span></span>

<span data-ttu-id="6a25c-113">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="6a25c-113">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a25c-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="6a25c-114">Remarks</span></span>

<span data-ttu-id="6a25c-115">È anche possibile specificare una posizione iniziale e finale per la riproduzione usando la macro [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) .</span><span class="sxs-lookup"><span data-stu-id="6a25c-115">You can also specify both a starting and ending location for playback by using the [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a25c-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a25c-116">Requirements</span></span>



| <span data-ttu-id="6a25c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a25c-117">Requirement</span></span> | <span data-ttu-id="6a25c-118">Valore</span><span class="sxs-lookup"><span data-stu-id="6a25c-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6a25c-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a25c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6a25c-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6a25c-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6a25c-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a25c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6a25c-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6a25c-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6a25c-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6a25c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a25c-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a25c-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a25c-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6a25c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a25c-126">**MCIWndPlayFrom**</span><span class="sxs-lookup"><span data-stu-id="6a25c-126">**MCIWndPlayFrom**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom)
</dt> <dt>

[<span data-ttu-id="6a25c-127">**MCIWndPlayFromTo**</span><span class="sxs-lookup"><span data-stu-id="6a25c-127">**MCIWndPlayFromTo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)
</dt> </dl>

 

 






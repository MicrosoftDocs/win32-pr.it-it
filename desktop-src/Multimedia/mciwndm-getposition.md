---
title: Messaggio di MCIWNDM_GETPOSITION (VFW. h)
description: Il \_ messaggio MCIWNDM GetPosition Recupera il valore numerico della posizione corrente all'interno del contenuto del dispositivo MCI.
ms.assetid: 6dc5d3bd-8515-4514-a2a5-c1bee07f7acf
keywords:
- MCIWNDM_GETPOSITION messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_GETPOSITION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2e7468b0e3698a72d3dce82bbd1591d59940d9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873421"
---
# <a name="mciwndm_getposition-message"></a><span data-ttu-id="77d83-104">\_Messaggio GETPOSITION MCIWNDM</span><span class="sxs-lookup"><span data-stu-id="77d83-104">MCIWNDM\_GETPOSITION message</span></span>

<span data-ttu-id="77d83-105">Il messaggio **MCIWNDM \_ GetPosition** Recupera il valore numerico della posizione corrente all'interno del contenuto del dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="77d83-105">The **MCIWNDM\_GETPOSITION** message retrieves the numerical value of the current position within the content of the MCI device.</span></span> <span data-ttu-id="77d83-106">Questa macro fornisce anche la posizione corrente in formato stringa in un buffer definito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="77d83-106">This macro also provides the current position in string form in an application-defined buffer.</span></span> <span data-ttu-id="77d83-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) o [**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring) .</span><span class="sxs-lookup"><span data-stu-id="77d83-107">You can send this message explicitly or by using the [**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) or [**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring) macro.</span></span>


```C++
MCIWNDM_GETPOSITION 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPTSTR) lp; 
```



## <a name="parameters"></a><span data-ttu-id="77d83-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="77d83-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77d83-109"><span id="len"></span><span id="LEN"></span>*Len*</span><span class="sxs-lookup"><span data-stu-id="77d83-109"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="77d83-110">Dimensione, in byte, del buffer.</span><span class="sxs-lookup"><span data-stu-id="77d83-110">Size, in bytes, of the buffer.</span></span> <span data-ttu-id="77d83-111">Se la stringa con terminazione null è più lunga del buffer, viene troncata.</span><span class="sxs-lookup"><span data-stu-id="77d83-111">If the null-terminated string is longer than the buffer, it is truncated.</span></span> <span data-ttu-id="77d83-112">Usare zero per impedire il recupero della posizione sotto forma di stringa.</span><span class="sxs-lookup"><span data-stu-id="77d83-112">Use zero to inhibit retrieval of the position as a string.</span></span>

</dd> <dt>

<span data-ttu-id="77d83-113"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="77d83-113"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="77d83-114">Puntatore a un buffer definito dall'applicazione utilizzato per restituire la posizione.</span><span class="sxs-lookup"><span data-stu-id="77d83-114">Pointer to an application-defined buffer used to return the position.</span></span> <span data-ttu-id="77d83-115">Usare zero per impedire il recupero della posizione sotto forma di stringa.</span><span class="sxs-lookup"><span data-stu-id="77d83-115">Use zero to inhibit retrieval of the position as a string.</span></span> <span data-ttu-id="77d83-116">Se il dispositivo supporta le tracce, le informazioni sulla posizione della stringa vengono restituite nel formato TT: MM: SS: FF, dove TT corrisponde a Tracks, MM e SS corrispondono a minuti e secondi e FF corrisponde ai frame.</span><span class="sxs-lookup"><span data-stu-id="77d83-116">If the device supports tracks, the string position information is returned in the form TT:MM:SS:FF where TT corresponds to tracks, MM and SS correspond to minutes and seconds, and FF corresponds to frames.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77d83-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="77d83-117">Return Value</span></span>

<span data-ttu-id="77d83-118">Restituisce un intero corrispondente alla posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="77d83-118">Returns an integer corresponding to the current position.</span></span> <span data-ttu-id="77d83-119">Le unità per il valore di posizione dipendono dal formato dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="77d83-119">The units for the position value depend on the current time format.</span></span>

## <a name="requirements"></a><span data-ttu-id="77d83-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="77d83-120">Requirements</span></span>



| <span data-ttu-id="77d83-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="77d83-121">Requirement</span></span> | <span data-ttu-id="77d83-122">Valore</span><span class="sxs-lookup"><span data-stu-id="77d83-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="77d83-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="77d83-123">Minimum supported client</span></span><br/> | <span data-ttu-id="77d83-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="77d83-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="77d83-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="77d83-125">Minimum supported server</span></span><br/> | <span data-ttu-id="77d83-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="77d83-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="77d83-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="77d83-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="77d83-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="77d83-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77d83-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="77d83-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77d83-130">**MCIWndGetPosition**</span><span class="sxs-lookup"><span data-stu-id="77d83-130">**MCIWndGetPosition**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition)
</dt> <dt>

[<span data-ttu-id="77d83-131">**MCIWndGetPositionString**</span><span class="sxs-lookup"><span data-stu-id="77d83-131">**MCIWndGetPositionString**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring)
</dt> </dl>

 

 






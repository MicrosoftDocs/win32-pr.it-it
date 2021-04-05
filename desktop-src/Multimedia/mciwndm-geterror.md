---
title: Messaggio di MCIWNDM_GETERROR (VFW. h)
description: Il \_ messaggio MCIWNDM GetError recupera l'ultimo errore MCI rilevato. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndGetError.
ms.assetid: f110a9b3-5b05-4bf0-85d1-b49ce7396222
keywords:
- MCIWNDM_GETERROR messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_GETERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c2977bb079351824b48da21f4ba3cc2dc5afe7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873422"
---
# <a name="mciwndm_geterror-message"></a><span data-ttu-id="5e366-105">\_Messaggio GETERROR MCIWNDM</span><span class="sxs-lookup"><span data-stu-id="5e366-105">MCIWNDM\_GETERROR message</span></span>

<span data-ttu-id="5e366-106">Il messaggio **MCIWNDM \_ GetError** recupera l'ultimo errore MCI rilevato.</span><span class="sxs-lookup"><span data-stu-id="5e366-106">The **MCIWNDM\_GETERROR** message retrieves the last MCI error encountered.</span></span> <span data-ttu-id="5e366-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror) .</span><span class="sxs-lookup"><span data-stu-id="5e366-107">You can send this message explicitly or by using the [**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror) macro.</span></span>


```C++
MCIWNDM_GETERROR 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a><span data-ttu-id="5e366-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5e366-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e366-109"><span id="len"></span><span id="LEN"></span>*Len*</span><span class="sxs-lookup"><span data-stu-id="5e366-109"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="5e366-110">Dimensione, in byte, del buffer degli errori.</span><span class="sxs-lookup"><span data-stu-id="5e366-110">Size, in bytes, of the error buffer.</span></span>

</dd> <dt>

<span data-ttu-id="5e366-111"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="5e366-111"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="5e366-112">Puntatore a un buffer definito dall'applicazione utilizzato per restituire la stringa di errore.</span><span class="sxs-lookup"><span data-stu-id="5e366-112">Pointer to an application-defined buffer used to return the error string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e366-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5e366-113">Return Value</span></span>

<span data-ttu-id="5e366-114">Restituisce il valore di errore integer in caso di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="5e366-114">Returns the integer error value if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e366-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="5e366-115">Remarks</span></span>

<span data-ttu-id="5e366-116">Se *LP* è un puntatore valido, nel buffer viene restituita una stringa con terminazione null corrispondente all'errore.</span><span class="sxs-lookup"><span data-stu-id="5e366-116">If *lp* is a valid pointer, a null-terminated string corresponding to the error is returned in its buffer.</span></span> <span data-ttu-id="5e366-117">Se la stringa di errore è più lunga del buffer, MCIWnd lo tronca.</span><span class="sxs-lookup"><span data-stu-id="5e366-117">If the error string is longer than the buffer, MCIWnd truncates it.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e366-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5e366-118">Requirements</span></span>



| <span data-ttu-id="5e366-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e366-119">Requirement</span></span> | <span data-ttu-id="5e366-120">Valore</span><span class="sxs-lookup"><span data-stu-id="5e366-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5e366-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e366-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5e366-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5e366-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5e366-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e366-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5e366-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5e366-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5e366-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5e366-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e366-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e366-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e366-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5e366-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e366-128">**MCIWndGetError**</span><span class="sxs-lookup"><span data-stu-id="5e366-128">**MCIWndGetError**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror)
</dt> </dl>

 

 






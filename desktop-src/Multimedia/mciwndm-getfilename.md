---
title: Messaggio di MCIWNDM_GETFILENAME (VFW. h)
description: Il \_ messaggio MCIWNDM GETfilename Recupera il nome file attualmente usato da un dispositivo MCI. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndGetFileName.
ms.assetid: d61b1b6d-0fae-4732-993c-41e08a4e05be
keywords:
- MCIWNDM_GETFILENAME messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_GETFILENAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 232a1d829b5cdd6da23e7dd3fb0294b95ca79f4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517427"
---
# <a name="mciwndm_getfilename-message"></a><span data-ttu-id="784f3-105">MCIWNDM \_ messaggio GETfilename</span><span class="sxs-lookup"><span data-stu-id="784f3-105">MCIWNDM\_GETFILENAME message</span></span>

<span data-ttu-id="784f3-106">Il messaggio **MCIWNDM \_ GetFileName** Recupera il nome file attualmente usato da un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="784f3-106">The **MCIWNDM\_GETFILENAME** message retrieves the filename currently used by an MCI device.</span></span> <span data-ttu-id="784f3-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndGetFileName**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) .</span><span class="sxs-lookup"><span data-stu-id="784f3-107">You can send this message explicitly or by using the [**MCIWndGetFileName**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) macro.</span></span>


```C++
MCIWNDM_GETFILENAME 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a><span data-ttu-id="784f3-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="784f3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="784f3-109"><span id="len"></span><span id="LEN"></span>*Len*</span><span class="sxs-lookup"><span data-stu-id="784f3-109"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="784f3-110">Dimensione, in byte, del buffer.</span><span class="sxs-lookup"><span data-stu-id="784f3-110">Size, in bytes, of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="784f3-111"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="784f3-111"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="784f3-112">Puntatore a un buffer definito dall'applicazione per restituire il nome file.</span><span class="sxs-lookup"><span data-stu-id="784f3-112">Pointer to an application-defined buffer to return the filename.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="784f3-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="784f3-113">Return Value</span></span>

<span data-ttu-id="784f3-114">Restituisce zero se ha esito positivo o 1 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="784f3-114">Returns zero if successful or 1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="784f3-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="784f3-115">Remarks</span></span>

<span data-ttu-id="784f3-116">Se la stringa con terminazione null che contiene il nome del file è più lunga del buffer, MCIWnd tronca il nome del file.</span><span class="sxs-lookup"><span data-stu-id="784f3-116">If the null-terminated string containing the filename is longer than the buffer, MCIWnd truncates the filename.</span></span>

## <a name="requirements"></a><span data-ttu-id="784f3-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="784f3-117">Requirements</span></span>



| <span data-ttu-id="784f3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="784f3-118">Requirement</span></span> | <span data-ttu-id="784f3-119">Valore</span><span class="sxs-lookup"><span data-stu-id="784f3-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="784f3-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="784f3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="784f3-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="784f3-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="784f3-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="784f3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="784f3-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="784f3-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="784f3-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="784f3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="784f3-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="784f3-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="784f3-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="784f3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="784f3-127">**MCIWndGetFileName**</span><span class="sxs-lookup"><span data-stu-id="784f3-127">**MCIWndGetFileName**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename)
</dt> </dl>

 

 






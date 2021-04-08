---
title: Messaggio di MCIWNDM_RETURNSTRING (VFW. h)
description: Il \_ messaggio MCIWNDM RETURNSTRING recupera la risposta al comando di stringa MCI più recente inviato a un dispositivo MCI.
ms.assetid: 36a5222c-a63c-4b8c-ad0c-a00477e95b96
keywords:
- MCIWNDM_RETURNSTRING messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_RETURNSTRING
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b99307bd7d61a70db594d0a696cceccd6d246a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048336"
---
# <a name="mciwndm_returnstring-message"></a><span data-ttu-id="7ae18-104">\_Messaggio MCIWNDM RETURNSTRING</span><span class="sxs-lookup"><span data-stu-id="7ae18-104">MCIWNDM\_RETURNSTRING message</span></span>

<span data-ttu-id="7ae18-105">Il messaggio **MCIWNDM \_ RETURNSTRING** recupera la risposta al comando di stringa MCI più recente inviato a un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="7ae18-105">The **MCIWNDM\_RETURNSTRING** message retrieves the reply to the most recent MCI string command sent to an MCI device.</span></span> <span data-ttu-id="7ae18-106">Le informazioni nella risposta vengono fornite come stringa con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="7ae18-106">Information in the reply is supplied as a null-terminated string.</span></span> <span data-ttu-id="7ae18-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring) .</span><span class="sxs-lookup"><span data-stu-id="7ae18-107">You can send this message explicitly or by using the [**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring) macro.</span></span>


```C++
MCIWNDM_RETURNSTRING 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a><span data-ttu-id="7ae18-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7ae18-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ae18-109"><span id="len"></span><span id="LEN"></span>*Len*</span><span class="sxs-lookup"><span data-stu-id="7ae18-109"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="7ae18-110">Dimensione, in byte, del buffer.</span><span class="sxs-lookup"><span data-stu-id="7ae18-110">Size, in bytes, of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="7ae18-111"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="7ae18-111"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="7ae18-112">Puntatore a un buffer definito dall'applicazione per contenere la stringa con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="7ae18-112">Pointer to an application-defined buffer to contain the null-terminated string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ae18-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7ae18-113">Return Value</span></span>

<span data-ttu-id="7ae18-114">Restituisce un Integer che corrisponde alla stringa MCI.</span><span class="sxs-lookup"><span data-stu-id="7ae18-114">Returns an integer corresponding to the MCI string.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ae18-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="7ae18-115">Remarks</span></span>

<span data-ttu-id="7ae18-116">Se la stringa con terminazione null è più lunga del buffer, la stringa viene troncata.</span><span class="sxs-lookup"><span data-stu-id="7ae18-116">If the null-terminated string is longer than the buffer, the string is truncated.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ae18-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ae18-117">Requirements</span></span>



| <span data-ttu-id="7ae18-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ae18-118">Requirement</span></span> | <span data-ttu-id="7ae18-119">Valore</span><span class="sxs-lookup"><span data-stu-id="7ae18-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7ae18-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ae18-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7ae18-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7ae18-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7ae18-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ae18-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7ae18-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7ae18-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7ae18-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7ae18-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ae18-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ae18-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ae18-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7ae18-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ae18-127">**MCIWndReturnString**</span><span class="sxs-lookup"><span data-stu-id="7ae18-127">**MCIWndReturnString**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring)
</dt> </dl>

 

 






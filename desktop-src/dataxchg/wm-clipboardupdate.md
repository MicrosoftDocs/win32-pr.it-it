---
title: Messaggio WM_CLIPBOARDUPDATE (winuser. h)
description: Inviato quando il contenuto degli Appunti viene modificato.
ms.assetid: 1508aa22-9cf0-40a2-8cb0-ce7c8671df2c
keywords:
- Scambio di dati del messaggio WM_CLIPBOARDUPDATE
topic_type:
- apiref
api_name:
- WM_CLIPBOARDUPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303110f0d094cfed336a9f92006b3720a0ccc83b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120042"
---
# <a name="wm_clipboardupdate-message"></a><span data-ttu-id="8153c-104">\_Messaggio CLIPBOARDUPDATE WM</span><span class="sxs-lookup"><span data-stu-id="8153c-104">WM\_CLIPBOARDUPDATE message</span></span>

<span data-ttu-id="8153c-105">Inviato quando il contenuto degli Appunti viene modificato.</span><span class="sxs-lookup"><span data-stu-id="8153c-105">Sent when the contents of the clipboard have changed.</span></span>


```C++
#define WM_CLIPBOARDUPDATE              0x031D
```



## <a name="parameters"></a><span data-ttu-id="8153c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8153c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8153c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8153c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8153c-108">Questo parametro non viene utilizzato e deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="8153c-108">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8153c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8153c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8153c-110">Questo parametro non viene utilizzato e deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="8153c-110">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8153c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8153c-111">Return value</span></span>

<span data-ttu-id="8153c-112">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="8153c-112">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8153c-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="8153c-113">Remarks</span></span>

<span data-ttu-id="8153c-114">Per registrare una finestra per la ricezione di questo messaggio, usare la funzione [**AddClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener) .</span><span class="sxs-lookup"><span data-stu-id="8153c-114">To register a window to receive this message, use the [**AddClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8153c-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8153c-115">Requirements</span></span>



| <span data-ttu-id="8153c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8153c-116">Requirement</span></span> | <span data-ttu-id="8153c-117">Valore</span><span class="sxs-lookup"><span data-stu-id="8153c-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8153c-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8153c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8153c-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8153c-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8153c-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8153c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8153c-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8153c-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8153c-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8153c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8153c-123"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8153c-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8153c-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8153c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8153c-125">**AddClipboardFormatListener**</span><span class="sxs-lookup"><span data-stu-id="8153c-125">**AddClipboardFormatListener**</span></span>](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener)
</dt> <dt>

[<span data-ttu-id="8153c-126">**RemoveClipboardFormatListener**</span><span class="sxs-lookup"><span data-stu-id="8153c-126">**RemoveClipboardFormatListener**</span></span>](/windows/desktop/api/Winuser/nf-winuser-removeclipboardformatlistener)
</dt> <dt>

[<span data-ttu-id="8153c-127">**GetClipboardSequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="8153c-127">**GetClipboardSequenceNumber**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber)
</dt> </dl>

 

 






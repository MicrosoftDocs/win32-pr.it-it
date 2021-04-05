---
title: Messaggio WM_SIZECLIPBOARD (winuser. h)
description: Inviato al proprietario degli Appunti da una finestra del visualizzatore degli Appunti quando gli Appunti contengono dati nel \_ formato CF OWNERDISPLAY e le dimensioni dell'area client del Visualizzatore Appunti sono state modificate.
ms.assetid: 95991d03-8677-4dde-b72a-082dec4834b3
keywords:
- Scambio di dati del messaggio WM_SIZECLIPBOARD
topic_type:
- apiref
api_name:
- WM_SIZECLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 235de630b20757a571b1917a975d1425bee06cde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741863"
---
# <a name="wm_sizeclipboard-message"></a><span data-ttu-id="3d189-104">\_Messaggio SIZECLIPBOARD WM</span><span class="sxs-lookup"><span data-stu-id="3d189-104">WM\_SIZECLIPBOARD message</span></span>

<span data-ttu-id="3d189-105">Inviato al proprietario degli Appunti da una finestra del visualizzatore degli Appunti quando gli Appunti contengono dati nel formato [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) e le dimensioni dell'area client del Visualizzatore Appunti sono state modificate.</span><span class="sxs-lookup"><span data-stu-id="3d189-105">Sent to the clipboard owner by a clipboard viewer window when the clipboard contains data in the [**CF\_OWNERDISPLAY**](standard-clipboard-formats.md) format and the clipboard viewer's client area has changed size.</span></span>


```C++
#define WM_SIZECLIPBOARD                0x030B
```



## <a name="parameters"></a><span data-ttu-id="3d189-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3d189-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d189-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3d189-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3d189-108">Handle per la finestra del visualizzatore degli Appunti.</span><span class="sxs-lookup"><span data-stu-id="3d189-108">A handle to the clipboard viewer window.</span></span>

</dd> <dt>

<span data-ttu-id="3d189-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3d189-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3d189-110">Handle per un oggetto memoria globale che contiene una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="3d189-110">A handle to a global memory object that contains a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="3d189-111">La struttura specifica le nuove dimensioni dell'area client del visualizzatore degli Appunti.</span><span class="sxs-lookup"><span data-stu-id="3d189-111">The structure specifies the new dimensions of the clipboard viewer's client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d189-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3d189-112">Return value</span></span>

<span data-ttu-id="3d189-113">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="3d189-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d189-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="3d189-114">Remarks</span></span>

<span data-ttu-id="3d189-115">Quando la finestra Visualizzatore Appunti sta per essere distrutta o ridimensionata, viene inviato un messaggio **WM \_ SIZECLIPBOARD** con un rettangolo null (0, 0, 0, 0) come nuova dimensione.</span><span class="sxs-lookup"><span data-stu-id="3d189-115">When the clipboard viewer window is about to be destroyed or resized, a **WM\_SIZECLIPBOARD** message is sent with a null rectangle (0, 0, 0, 0) as the new size.</span></span> <span data-ttu-id="3d189-116">Ciò consente al proprietario degli Appunti di liberare le risorse di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="3d189-116">This permits the clipboard owner to free its display resources.</span></span>

<span data-ttu-id="3d189-117">Il proprietario degli Appunti deve usare la funzione [**funzione GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock) per bloccare l'oggetto Memory che contiene [**Rect**](/previous-versions//dd162897(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3d189-117">The clipboard owner must use the [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock) function to lock the memory object that contains [**RECT**](/previous-versions//dd162897(v=vs.85)).</span></span> <span data-ttu-id="3d189-118">Prima di restituire, il proprietario degli Appunti deve sbloccare l'oggetto utilizzando la funzione [**funzione GlobalUnlock**](/windows/desktop/api/winbase/nf-winbase-globalunlock) .</span><span class="sxs-lookup"><span data-stu-id="3d189-118">Before returning, the clipboard owner must unlock the object by using the [**GlobalUnlock**](/windows/desktop/api/winbase/nf-winbase-globalunlock) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d189-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d189-119">Requirements</span></span>



| <span data-ttu-id="3d189-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d189-120">Requirement</span></span> | <span data-ttu-id="3d189-121">Valore</span><span class="sxs-lookup"><span data-stu-id="3d189-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d189-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d189-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3d189-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3d189-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3d189-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d189-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3d189-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3d189-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3d189-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3d189-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d189-127"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3d189-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d189-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3d189-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="3d189-129">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="3d189-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3d189-130">Appunti</span><span class="sxs-lookup"><span data-stu-id="3d189-130">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 


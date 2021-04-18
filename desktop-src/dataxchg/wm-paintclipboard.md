---
title: Messaggio WM_PAINTCLIPBOARD (winuser. h)
description: Inviato al proprietario degli Appunti da una finestra del visualizzatore degli Appunti quando gli Appunti contengono dati nel \_ formato CF OWNERDISPLAY e l'area client del Visualizzatore Appunti deve essere ridisegnata.
ms.assetid: 85aeefa5-e3d9-4689-a068-47b59ec7b571
keywords:
- Scambio di dati del messaggio WM_PAINTCLIPBOARD
topic_type:
- apiref
api_name:
- WM_PAINTCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8148af6b513fd1fa956d48f22dc86e618544b073
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301437"
---
# <a name="wm_paintclipboard-message"></a><span data-ttu-id="5b416-104">\_Messaggio PAINTCLIPBOARD WM</span><span class="sxs-lookup"><span data-stu-id="5b416-104">WM\_PAINTCLIPBOARD message</span></span>

<span data-ttu-id="5b416-105">Inviato al proprietario degli Appunti da una finestra del visualizzatore degli Appunti quando gli Appunti contengono dati nel formato [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) e l'area client del Visualizzatore Appunti deve essere ridisegnata.</span><span class="sxs-lookup"><span data-stu-id="5b416-105">Sent to the clipboard owner by a clipboard viewer window when the clipboard contains data in the [**CF\_OWNERDISPLAY**](standard-clipboard-formats.md) format and the clipboard viewer's client area needs repainting.</span></span>


```C++
#define WM_PAINTCLIPBOARD               0x0309
```



## <a name="parameters"></a><span data-ttu-id="5b416-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5b416-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b416-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5b416-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b416-108">Handle per la finestra del visualizzatore degli Appunti.</span><span class="sxs-lookup"><span data-stu-id="5b416-108">A handle to the clipboard viewer window.</span></span>

</dd> <dt>

<span data-ttu-id="5b416-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5b416-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b416-110">Handle per un oggetto memoria globale che contiene una struttura [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) .</span><span class="sxs-lookup"><span data-stu-id="5b416-110">A handle to a global memory object that contains a [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) structure.</span></span> <span data-ttu-id="5b416-111">La struttura definisce la parte dell'area client da disegnare.</span><span class="sxs-lookup"><span data-stu-id="5b416-111">The structure defines the part of the client area to paint.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b416-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5b416-112">Return value</span></span>

<span data-ttu-id="5b416-113">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="5b416-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b416-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="5b416-114">Remarks</span></span>

<span data-ttu-id="5b416-115">Per determinare se l'intera area client o solo una parte di essa debba essere ridisegnata, il proprietario degli Appunti deve confrontare le dimensioni dell'area di disegno specificata nel membro **rcPaint** di [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) con le dimensioni specificate nel messaggio [**WM \_ SIZECLIPBOARD**](wm-sizeclipboard.md) più recente.</span><span class="sxs-lookup"><span data-stu-id="5b416-115">To determine whether the entire client area or just a portion of it needs repainting, the clipboard owner must compare the dimensions of the drawing area given in the **rcPaint** member of [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) to the dimensions given in the most recent [**WM\_SIZECLIPBOARD**](wm-sizeclipboard.md) message.</span></span>

<span data-ttu-id="5b416-116">Il proprietario degli Appunti deve usare la funzione [**funzione GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock) per bloccare la memoria che contiene la struttura [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) .</span><span class="sxs-lookup"><span data-stu-id="5b416-116">The clipboard owner must use the [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock) function to lock the memory that contains the [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) structure.</span></span> <span data-ttu-id="5b416-117">Prima di restituire, il proprietario degli Appunti deve sbloccare tale memoria utilizzando la funzione [**funzione GlobalUnlock**](/windows/desktop/api/winbase/nf-winbase-globalunlock) .</span><span class="sxs-lookup"><span data-stu-id="5b416-117">Before returning, the clipboard owner must unlock that memory by using the [**GlobalUnlock**](/windows/desktop/api/winbase/nf-winbase-globalunlock) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b416-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5b416-118">Requirements</span></span>



| <span data-ttu-id="5b416-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b416-119">Requirement</span></span> | <span data-ttu-id="5b416-120">Valore</span><span class="sxs-lookup"><span data-stu-id="5b416-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b416-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b416-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5b416-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5b416-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5b416-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b416-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5b416-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5b416-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5b416-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5b416-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b416-126"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5b416-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b416-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5b416-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="5b416-128">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="5b416-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5b416-129">**\_SIZECLIPBOARD WM**</span><span class="sxs-lookup"><span data-stu-id="5b416-129">**WM\_SIZECLIPBOARD**</span></span>](wm-sizeclipboard.md)
</dt> <dt>

<span data-ttu-id="5b416-130">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="5b416-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5b416-131">Appunti</span><span class="sxs-lookup"><span data-stu-id="5b416-131">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 


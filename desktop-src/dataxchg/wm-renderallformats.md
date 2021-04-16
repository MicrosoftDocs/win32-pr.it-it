---
title: Messaggio WM_RENDERALLFORMATS (winuser. h)
description: Inviato al proprietario degli Appunti prima che venga eliminato definitivamente, se il proprietario degli Appunti ha ritardato il rendering di uno o più formati degli Appunti.
ms.assetid: dff9100f-2dba-467d-be74-a9a9c2b2122b
keywords:
- Scambio di dati del messaggio WM_RENDERALLFORMATS
topic_type:
- apiref
api_name:
- WM_RENDERALLFORMATS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cdd3ce1fabdea4cdcae93b5243b89c53def0afa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518555"
---
# <a name="wm_renderallformats-message"></a><span data-ttu-id="aee06-104">\_Messaggio RENDERALLFORMATS WM</span><span class="sxs-lookup"><span data-stu-id="aee06-104">WM\_RENDERALLFORMATS message</span></span>

<span data-ttu-id="aee06-105">Inviato al proprietario degli Appunti prima che venga eliminato definitivamente, se il proprietario degli Appunti ha ritardato il rendering di uno o più formati degli Appunti.</span><span class="sxs-lookup"><span data-stu-id="aee06-105">Sent to the clipboard owner before it is destroyed, if the clipboard owner has delayed rendering one or more clipboard formats.</span></span> <span data-ttu-id="aee06-106">Affinché il contenuto degli Appunti rimanga disponibile per altre applicazioni, il proprietario degli Appunti deve eseguire il rendering dei dati in tutti i formati che è in grado di generare e inserire i dati negli Appunti chiamando la funzione [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) .</span><span class="sxs-lookup"><span data-stu-id="aee06-106">For the content of the clipboard to remain available to other applications, the clipboard owner must render data in all the formats it is capable of generating, and place the data on the clipboard by calling the [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) function.</span></span>

<span data-ttu-id="aee06-107">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="aee06-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_RENDERALLFORMATS             0x0306
```



## <a name="parameters"></a><span data-ttu-id="aee06-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="aee06-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aee06-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aee06-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aee06-110">Questo parametro non viene utilizzato e deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="aee06-110">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="aee06-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aee06-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aee06-112">Questo parametro non viene utilizzato e deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="aee06-112">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aee06-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aee06-113">Return value</span></span>

<span data-ttu-id="aee06-114">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="aee06-114">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="aee06-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="aee06-115">Remarks</span></span>

<span data-ttu-id="aee06-116">Quando si risponde a un messaggio **WM \_ RENDERALLFORMATS** , l'applicazione deve chiamare la funzione [**OpenClipboard**](/windows/win32/api/winuser/nf-winuser-openclipboard) e quindi verificare che sia ancora il proprietario degli Appunti chiamando la funzione [**GetClipboardOwner**](/windows/win32/api/winuser/nf-winuser-getclipboardowner) prima di chiamare [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata).</span><span class="sxs-lookup"><span data-stu-id="aee06-116">When responding to a **WM\_RENDERALLFORMATS** message, the application must call the [**OpenClipboard**](/windows/win32/api/winuser/nf-winuser-openclipboard) function and then check that it is still the clipboard owner by calling the [**GetClipboardOwner**](/windows/win32/api/winuser/nf-winuser-getclipboardowner) function before calling [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata).</span></span>

<span data-ttu-id="aee06-117">L'applicazione deve verificare che sia il proprietario degli Appunti dopo aver aperto gli appunti, perché dopo aver ricevuto il messaggio **WM \_ RENDERALLFORMATS** , ma prima di aprire gli appunti, è possibile che un'altra applicazione abbia aperto e assunto la proprietà degli Appunti e che i dati dell'applicazione non vengano sovrascritti.</span><span class="sxs-lookup"><span data-stu-id="aee06-117">The application needs to check that it is still the clipboard owner after opening the clipboard because after it receives the **WM\_RENDERALLFORMATS** message, but before it opens the clipboard, another application may have opened and taken ownership of the clipboard, and that application's data should not be overwritten.</span></span>

<span data-ttu-id="aee06-118">Nella maggior parte dei casi, l'applicazione non deve chiamare la funzione [**EmptyClipboard**](/windows/win32/api/winuser/nf-winuser-emptyclipboard) prima di chiamare [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata), poiché in questo modo verranno cancellati i formati degli appunti che l'applicazione ha già eseguito il rendering.</span><span class="sxs-lookup"><span data-stu-id="aee06-118">In most cases, the application should not call the [**EmptyClipboard**](/windows/win32/api/winuser/nf-winuser-emptyclipboard) function before calling [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata), since doing so will erase the clipboard formats that the application has already rendered.</span></span>

<span data-ttu-id="aee06-119">Quando l'applicazione viene restituita, il sistema rimuove tutti i formati non sottoposto a rendering dall'elenco dei formati degli appunti disponibili.</span><span class="sxs-lookup"><span data-stu-id="aee06-119">When the application returns, the system removes any unrendered formats from the list of available clipboard formats.</span></span> <span data-ttu-id="aee06-120">Per informazioni sul rendering ritardato, vedere [rendering ritardato](clipboard-operations.md#delayed-rendering).</span><span class="sxs-lookup"><span data-stu-id="aee06-120">For information about delayed rendering, see [Delayed Rendering](clipboard-operations.md#delayed-rendering).</span></span>

## <a name="requirements"></a><span data-ttu-id="aee06-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aee06-121">Requirements</span></span>



| <span data-ttu-id="aee06-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="aee06-122">Requirement</span></span> | <span data-ttu-id="aee06-123">Valore</span><span class="sxs-lookup"><span data-stu-id="aee06-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aee06-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aee06-124">Minimum supported client</span></span><br/> | <span data-ttu-id="aee06-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="aee06-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="aee06-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aee06-126">Minimum supported server</span></span><br/> | <span data-ttu-id="aee06-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="aee06-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="aee06-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aee06-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="aee06-129"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aee06-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aee06-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aee06-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="aee06-131">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="aee06-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="aee06-132">**EmptyClipboard**</span><span class="sxs-lookup"><span data-stu-id="aee06-132">**EmptyClipboard**</span></span>](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard)
</dt> <dt>

[<span data-ttu-id="aee06-133">**OpenClipboard**</span><span class="sxs-lookup"><span data-stu-id="aee06-133">**OpenClipboard**</span></span>](/windows/desktop/api/Winuser/nf-winuser-openclipboard)
</dt> <dt>

[<span data-ttu-id="aee06-134">**SetClipboardData**</span><span class="sxs-lookup"><span data-stu-id="aee06-134">**SetClipboardData**</span></span>](/windows/win32/api/winuser/nf-winuser-setclipboarddata)
</dt> <dt>

[<span data-ttu-id="aee06-135">**\_RENDERFORMAT WM**</span><span class="sxs-lookup"><span data-stu-id="aee06-135">**WM\_RENDERFORMAT**</span></span>](wm-renderformat.md)
</dt> <dt>

<span data-ttu-id="aee06-136">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="aee06-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="aee06-137">Appunti</span><span class="sxs-lookup"><span data-stu-id="aee06-137">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 


---
description: Inviato quando l'utente rilascia un file nella finestra di un'applicazione che si è registrato come destinatario di file eliminati.
ms.assetid: 07dc2df7-4699-4e9c-b1a5-4ce877116268
title: Messaggio WM_DROPFILES (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb8362bfa746eaab519cdfc34d2cdf7757105fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979466"
---
# <a name="wm_dropfiles-message"></a><span data-ttu-id="3a252-103">\_Messaggio DropFiles WM</span><span class="sxs-lookup"><span data-stu-id="3a252-103">WM\_DROPFILES message</span></span>

<span data-ttu-id="3a252-104">Inviato quando l'utente rilascia un file nella finestra di un'applicazione che si è registrato come destinatario di file eliminati.</span><span class="sxs-lookup"><span data-stu-id="3a252-104">Sent when the user drops a file on the window of an application that has registered itself as a recipient of dropped files.</span></span>


```C++
PostMessage(
    (HWND) hWndControl,   // handle to destination control
    (UINT) WM_DROPFILES,  // message ID
    (WPARAM) wParam,      // = (WPARAM) (HDROP) hDrop;
    (LPARAM) lParam       // = 0; not used, must be zero 
);          
```



## <a name="parameters"></a><span data-ttu-id="3a252-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="3a252-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a252-106">*hDrop*</span><span class="sxs-lookup"><span data-stu-id="3a252-106">*hDrop*</span></span> 
</dt> <dd>

<span data-ttu-id="3a252-107">Handle per una struttura interna che descrive i file eliminati.</span><span class="sxs-lookup"><span data-stu-id="3a252-107">A handle to an internal structure describing the dropped files.</span></span> <span data-ttu-id="3a252-108">Passare questo handle [**DragFinish**](/windows/desktop/api/Shellapi/nf-shellapi-dragfinish), [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea)o [**DragQueryPoint**](/windows/desktop/api/Shellapi/nf-shellapi-dragquerypoint) per recuperare le informazioni sui file eliminati.</span><span class="sxs-lookup"><span data-stu-id="3a252-108">Pass this handle [**DragFinish**](/windows/desktop/api/Shellapi/nf-shellapi-dragfinish), [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea), or [**DragQueryPoint**](/windows/desktop/api/Shellapi/nf-shellapi-dragquerypoint) to retrieve information about the dropped files.</span></span>

</dd> <dt>

<span data-ttu-id="3a252-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3a252-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3a252-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="3a252-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a252-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3a252-111">Return value</span></span>

<span data-ttu-id="3a252-112">Un'applicazione deve restituire zero se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="3a252-112">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a252-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="3a252-113">Remarks</span></span>

<span data-ttu-id="3a252-114">L'handle HDROP è dichiarato in Shellapi. h.</span><span class="sxs-lookup"><span data-stu-id="3a252-114">The HDROP handle is declared in Shellapi.h.</span></span> <span data-ttu-id="3a252-115">Per usare **WM \_ DropFiles**, è necessario includere questa intestazione nella compilazione.</span><span class="sxs-lookup"><span data-stu-id="3a252-115">You must include this header in your build to use **WM\_DROPFILES**.</span></span> <span data-ttu-id="3a252-116">Per altre informazioni su come usare il trascinamento della selezione per trasferire i dati della shell, vedere [trasferimento di dati della shell tramite il trascinamento della selezione o gli appunti](dragdrop.md).</span><span class="sxs-lookup"><span data-stu-id="3a252-116">For further discussion of how to use drag-and-drop to transfer Shell data, see [Transferring Shell Data Using Drag-and-Drop or the Clipboard](dragdrop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3a252-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a252-117">Requirements</span></span>



| <span data-ttu-id="3a252-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a252-118">Requirement</span></span> | <span data-ttu-id="3a252-119">Valore</span><span class="sxs-lookup"><span data-stu-id="3a252-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3a252-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a252-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3a252-121">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3a252-121">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3a252-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a252-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3a252-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3a252-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3a252-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3a252-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a252-125"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a252-125"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a252-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3a252-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a252-127">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="3a252-127">**PostMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="3a252-128">**DragAcceptFiles**</span><span class="sxs-lookup"><span data-stu-id="3a252-128">**DragAcceptFiles**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-dragacceptfiles)
</dt> </dl>

 

 

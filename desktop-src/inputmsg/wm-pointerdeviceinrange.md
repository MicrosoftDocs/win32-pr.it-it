---
title: Messaggio WM_POINTERDEVICEINRANGE
description: Inviato a una finestra quando viene rilevato un dispositivo puntatore nell'intervallo di un digitalizzatore di input. Questo messaggio contiene informazioni relative al dispositivo e alla relativa prossimità.
ms.assetid: 04244758-E662-4FB2-850E-20B4B3D1294A
keywords:
- Messaggi e notifiche di input del messaggio WM_POINTERDEVICEINRANGE
topic_type:
- apiref
api_name:
- WM_POINTERDEVICEINRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 76ab6ac4f96d1df4e4e29afbcefe86d34b8b602d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518766"
---
# <a name="wm_pointerdeviceinrange-message"></a><span data-ttu-id="7c810-105">Messaggio WM_POINTERDEVICEINRANGE</span><span class="sxs-lookup"><span data-stu-id="7c810-105">WM_POINTERDEVICEINRANGE message</span></span>

<span data-ttu-id="7c810-106">Inviato a una finestra quando viene rilevato un dispositivo puntatore nell'intervallo di un digitalizzatore di input.</span><span class="sxs-lookup"><span data-stu-id="7c810-106">Sent to a window when a pointer device is detected within range of an input digitizer.</span></span> <span data-ttu-id="7c810-107">Questo messaggio contiene informazioni relative al dispositivo e alla relativa prossimità.</span><span class="sxs-lookup"><span data-stu-id="7c810-107">This message contains information regarding the device and its proximity.</span></span>

> <span data-ttu-id="7c810-108">\[! Importante\]</span><span class="sxs-lookup"><span data-stu-id="7c810-108">\[!Important\]</span></span>  
> <span data-ttu-id="7c810-109">Le applicazioni desktop devono essere compatibili con DPI.</span><span class="sxs-lookup"><span data-stu-id="7c810-109">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="7c810-110">Se l'app non è compatibile con DPI, le coordinate dello schermo contenute nei messaggi puntatore e le strutture correlate potrebbero sembrare non accurate a causa della virtualizzazione DPI.</span><span class="sxs-lookup"><span data-stu-id="7c810-110">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="7c810-111">La virtualizzazione DPI fornisce il supporto per il ridimensionamento automatico per le applicazioni che non sono compatibili con DPI ed è attivo per impostazione predefinita (gli utenti possono disabilitarlo).</span><span class="sxs-lookup"><span data-stu-id="7c810-111">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="7c810-112">Per altre informazioni, vedere [scrittura di applicazioni Win32 ad alta risoluzione](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7c810-112">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_POINTERDEVICEINRANGE       0X239
```



## <a name="parameters"></a><span data-ttu-id="7c810-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="7c810-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c810-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7c810-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c810-115">Ulteriori informazioni specifiche del messaggio.</span><span class="sxs-lookup"><span data-stu-id="7c810-115">Additional message-specific information.</span></span>

</dd> <dt>

<span data-ttu-id="7c810-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7c810-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c810-117">Ulteriori informazioni specifiche del messaggio.</span><span class="sxs-lookup"><span data-stu-id="7c810-117">Additional message-specific information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c810-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7c810-118">Return value</span></span>

<span data-ttu-id="7c810-119">Se l'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="7c810-119">If the application processes this message, it should return zero.</span></span>

<span data-ttu-id="7c810-120">Se l'applicazione non elabora questo messaggio, deve chiamare [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="7c810-120">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="requirements"></a><span data-ttu-id="7c810-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c810-121">Requirements</span></span>



| <span data-ttu-id="7c810-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c810-122">Requirement</span></span> | <span data-ttu-id="7c810-123">Valore</span><span class="sxs-lookup"><span data-stu-id="7c810-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c810-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c810-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7c810-125">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7c810-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="7c810-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c810-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7c810-127">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7c810-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7c810-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7c810-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c810-129"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7c810-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c810-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7c810-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c810-131">Messaggi</span><span class="sxs-lookup"><span data-stu-id="7c810-131">Messages</span></span>](messages.md)
</dt> </dl>

 


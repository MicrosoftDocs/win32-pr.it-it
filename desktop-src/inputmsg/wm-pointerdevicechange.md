---
title: Messaggio WM_POINTERDEVICECHANGE
description: Inviato a una finestra quando viene apportata una modifica alle impostazioni di un monitoraggio a cui è collegato un digitalizzatore. Questo messaggio contiene informazioni sul ridimensionamento della modalità di visualizzazione.
ms.assetid: 9ED01D4C-58B4-4A21-B510-784281F9A909
keywords:
- Messaggi e notifiche di input del messaggio WM_POINTERDEVICECHANGE
topic_type:
- apiref
api_name:
- WM_POINTERDEVICECHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 38f570059f374f64e393e960a8458e605983d6c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302073"
---
# <a name="wm_pointerdevicechange-message"></a><span data-ttu-id="89a99-105">Messaggio WM_POINTERDEVICECHANGE</span><span class="sxs-lookup"><span data-stu-id="89a99-105">WM_POINTERDEVICECHANGE message</span></span>

<span data-ttu-id="89a99-106">Inviato a una finestra quando viene apportata una modifica alle impostazioni di un monitoraggio a cui è collegato un digitalizzatore.</span><span class="sxs-lookup"><span data-stu-id="89a99-106">Sent to a window when there is a change in the settings of a monitor that has a digitizer attached to it.</span></span> <span data-ttu-id="89a99-107">Questo messaggio contiene informazioni sul ridimensionamento della modalità di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="89a99-107">This message contains information regarding the scaling of the display mode.</span></span>

> <span data-ttu-id="89a99-108">\[! Importante\]</span><span class="sxs-lookup"><span data-stu-id="89a99-108">\[!Important\]</span></span>  
> <span data-ttu-id="89a99-109">Le applicazioni desktop devono essere compatibili con DPI.</span><span class="sxs-lookup"><span data-stu-id="89a99-109">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="89a99-110">Se l'app non è compatibile con DPI, le coordinate dello schermo contenute nei messaggi puntatore e le strutture correlate potrebbero sembrare non accurate a causa della virtualizzazione DPI.</span><span class="sxs-lookup"><span data-stu-id="89a99-110">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="89a99-111">La virtualizzazione DPI fornisce il supporto per il ridimensionamento automatico per le applicazioni che non sono compatibili con DPI ed è attivo per impostazione predefinita (gli utenti possono disabilitarlo).</span><span class="sxs-lookup"><span data-stu-id="89a99-111">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="89a99-112">Per altre informazioni, vedere [scrittura di applicazioni Win32 ad alta risoluzione](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="89a99-112">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_POINTERDEVICECHANGE       0X238
```



## <a name="parameters"></a><span data-ttu-id="89a99-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="89a99-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89a99-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="89a99-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="89a99-115">Contiene un valore delle [**costanti di modifica del dispositivo puntatore**](pointer-device-change-constants.md).</span><span class="sxs-lookup"><span data-stu-id="89a99-115">Contains a value from [**Pointer Device Change Constants**](pointer-device-change-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="89a99-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="89a99-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="89a99-117">Ulteriori informazioni specifiche del messaggio.</span><span class="sxs-lookup"><span data-stu-id="89a99-117">Additional message-specific information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89a99-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="89a99-118">Return value</span></span>

<span data-ttu-id="89a99-119">Se l'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="89a99-119">If the application processes this message, it should return zero.</span></span>

<span data-ttu-id="89a99-120">Se l'applicazione non elabora questo messaggio, deve chiamare [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="89a99-120">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="requirements"></a><span data-ttu-id="89a99-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="89a99-121">Requirements</span></span>



| <span data-ttu-id="89a99-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="89a99-122">Requirement</span></span> | <span data-ttu-id="89a99-123">Valore</span><span class="sxs-lookup"><span data-stu-id="89a99-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89a99-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89a99-124">Minimum supported client</span></span><br/> | <span data-ttu-id="89a99-125">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="89a99-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="89a99-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89a99-126">Minimum supported server</span></span><br/> | <span data-ttu-id="89a99-127">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="89a99-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="89a99-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="89a99-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="89a99-129"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="89a99-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89a99-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="89a99-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89a99-131">Messaggi</span><span class="sxs-lookup"><span data-stu-id="89a99-131">Messages</span></span>](messages.md)
</dt> </dl>

 


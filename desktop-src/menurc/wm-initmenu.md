---
title: Messaggio WM_INITMENU (winuser. h)
description: Inviato quando un menu sta per diventare attivo.
ms.assetid: d0fcc6d8-f57c-4d04-b9e7-4cfab6add173
keywords:
- Menu del messaggio WM_INITMENU e altre risorse
topic_type:
- apiref
api_name:
- WM_INITMENU
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94626b99a5016efaa9427d1ae8b3b3122e599965
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302526"
---
# <a name="wm_initmenu-message"></a><span data-ttu-id="9c7ec-104">\_Messaggio INITMENU WM</span><span class="sxs-lookup"><span data-stu-id="9c7ec-104">WM\_INITMENU message</span></span>

<span data-ttu-id="9c7ec-105">Inviato quando un menu sta per diventare attivo.</span><span class="sxs-lookup"><span data-stu-id="9c7ec-105">Sent when a menu is about to become active.</span></span> <span data-ttu-id="9c7ec-106">Si verifica quando l'utente fa clic su un elemento nella barra dei menu o preme un tasto di menu.</span><span class="sxs-lookup"><span data-stu-id="9c7ec-106">It occurs when the user clicks an item on the menu bar or presses a menu key.</span></span> <span data-ttu-id="9c7ec-107">Questo consente all'applicazione di modificare il menu prima che venga visualizzato.</span><span class="sxs-lookup"><span data-stu-id="9c7ec-107">This allows the application to modify the menu before it is displayed.</span></span>

<span data-ttu-id="9c7ec-108">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9c7ec-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_INITMENU                     0x0116
```



## <a name="parameters"></a><span data-ttu-id="9c7ec-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="9c7ec-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c7ec-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9c7ec-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c7ec-111">Handle per il menu da inizializzare.</span><span class="sxs-lookup"><span data-stu-id="9c7ec-111">A handle to the menu to be initialized.</span></span>

</dd> <dt>

<span data-ttu-id="9c7ec-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9c7ec-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c7ec-113">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="9c7ec-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c7ec-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9c7ec-114">Return value</span></span>

<span data-ttu-id="9c7ec-115">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="9c7ec-115">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c7ec-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="9c7ec-116">Remarks</span></span>

<span data-ttu-id="9c7ec-117">Un messaggio **WM \_ INITMENU** viene inviato solo quando si accede per la prima volta a un menu. viene generato un solo messaggio **WM \_ INITMENU** per ogni accesso.</span><span class="sxs-lookup"><span data-stu-id="9c7ec-117">A **WM\_INITMENU** message is sent only when a menu is first accessed; only one **WM\_INITMENU** message is generated for each access.</span></span> <span data-ttu-id="9c7ec-118">Ad esempio, lo spostamento del mouse tra diverse voci di menu tenendo premuto il pulsante non genera nuovi messaggi.</span><span class="sxs-lookup"><span data-stu-id="9c7ec-118">For example, moving the mouse across several menu items while holding down the button does not generate new messages.</span></span> <span data-ttu-id="9c7ec-119">**WM \_ INITMENU** non fornisce informazioni sulle voci di menu.</span><span class="sxs-lookup"><span data-stu-id="9c7ec-119">**WM\_INITMENU** does not provide information about menu items.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c7ec-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9c7ec-120">Requirements</span></span>



| <span data-ttu-id="9c7ec-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c7ec-121">Requirement</span></span> | <span data-ttu-id="9c7ec-122">Valore</span><span class="sxs-lookup"><span data-stu-id="9c7ec-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c7ec-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c7ec-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9c7ec-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9c7ec-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9c7ec-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c7ec-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9c7ec-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9c7ec-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9c7ec-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9c7ec-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c7ec-128"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9c7ec-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c7ec-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9c7ec-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="9c7ec-130">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="9c7ec-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9c7ec-131">**\_INITMENUPOPUP WM**</span><span class="sxs-lookup"><span data-stu-id="9c7ec-131">**WM\_INITMENUPOPUP**</span></span>](wm-initmenupopup.md)
</dt> <dt>

<span data-ttu-id="9c7ec-132">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="9c7ec-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9c7ec-133">Tasti di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="9c7ec-133">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 


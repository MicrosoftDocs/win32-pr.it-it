---
description: Un'applicazione invia il \_ messaggio WM MDIREFRESHMENU a una finestra del client di interfaccia a documenti multipli (MDI) per aggiornare il menu finestra della finestra cornice MDI.
ms.assetid: 6450d84a-a0b9-45d0-9e0c-757d26502059
title: Messaggio WM_MDIREFRESHMENU (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4eafa7b84dc9389e57d379a30019505e85fb602
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312374"
---
# <a name="wm_mdirefreshmenu-message"></a><span data-ttu-id="ad21e-103">\_Messaggio MDIREFRESHMENU WM</span><span class="sxs-lookup"><span data-stu-id="ad21e-103">WM\_MDIREFRESHMENU message</span></span>

<span data-ttu-id="ad21e-104">Un'applicazione invia il messaggio **WM \_ MDIREFRESHMENU** a una finestra del client di interfaccia a documenti multipli (MDI) per aggiornare il menu finestra della finestra cornice MDI.</span><span class="sxs-lookup"><span data-stu-id="ad21e-104">An application sends the **WM\_MDIREFRESHMENU** message to a multiple-document interface (MDI) client window to refresh the window menu of the MDI frame window.</span></span>


```C++
#define WM_MDIREFRESHMENU               0x0234
```



## <a name="parameters"></a><span data-ttu-id="ad21e-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="ad21e-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad21e-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ad21e-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ad21e-107">Questo parametro non viene utilizzato e deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="ad21e-107">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ad21e-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ad21e-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ad21e-109">Questo parametro non viene utilizzato e deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="ad21e-109">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad21e-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ad21e-110">Return value</span></span>

<span data-ttu-id="ad21e-111">Tipo: **HMENU**</span><span class="sxs-lookup"><span data-stu-id="ad21e-111">Type: **HMENU**</span></span>

<span data-ttu-id="ad21e-112">Se il messaggio ha esito positivo, il valore restituito è l'handle per il menu della finestra cornice.</span><span class="sxs-lookup"><span data-stu-id="ad21e-112">If the message succeeds, the return value is the handle to the frame window menu.</span></span>

<span data-ttu-id="ad21e-113">Se il messaggio ha esito negativo, il valore restituito è **null**.</span><span class="sxs-lookup"><span data-stu-id="ad21e-113">If the message fails, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad21e-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="ad21e-114">Remarks</span></span>

<span data-ttu-id="ad21e-115">Dopo l'invio di questo messaggio, un'applicazione deve chiamare la funzione [**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar) per aggiornare la barra dei menu.</span><span class="sxs-lookup"><span data-stu-id="ad21e-115">After sending this message, an application must call the [**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar) function to update the menu bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad21e-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ad21e-116">Requirements</span></span>



| <span data-ttu-id="ad21e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad21e-117">Requirement</span></span> | <span data-ttu-id="ad21e-118">Valore</span><span class="sxs-lookup"><span data-stu-id="ad21e-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad21e-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad21e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ad21e-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ad21e-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ad21e-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad21e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ad21e-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ad21e-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ad21e-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ad21e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad21e-124"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ad21e-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad21e-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ad21e-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="ad21e-126">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="ad21e-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ad21e-127">**DrawMenuBar**</span><span class="sxs-lookup"><span data-stu-id="ad21e-127">**DrawMenuBar**</span></span>](/windows/win32/api/winuser/nf-winuser-drawmenubar)
</dt> <dt>

[<span data-ttu-id="ad21e-128">**\_MDISETMENU WM**</span><span class="sxs-lookup"><span data-stu-id="ad21e-128">**WM\_MDISETMENU**</span></span>](wm-mdisetmenu.md)
</dt> <dt>

<span data-ttu-id="ad21e-129">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="ad21e-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ad21e-130">Interfaccia a documenti multipli</span><span class="sxs-lookup"><span data-stu-id="ad21e-130">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 

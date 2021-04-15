---
description: Un'applicazione invia il \_ messaggio WM MDIICONARRANGE a una finestra del client di interfaccia a documenti multipli (MDI) per disporre tutte le finestre figlio MDI ridotte a icona. Non influisce sulle finestre figlio non ridotte a icona.
ms.assetid: 935b9e29-224d-449e-b89f-b6062bed7702
title: Messaggio WM_MDIICONARRANGE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc2d50d4bccebe3e9758752cc7d0d259e973875c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484756"
---
# <a name="wm_mdiiconarrange-message"></a><span data-ttu-id="6c873-104">\_Messaggio MDIICONARRANGE WM</span><span class="sxs-lookup"><span data-stu-id="6c873-104">WM\_MDIICONARRANGE message</span></span>

<span data-ttu-id="6c873-105">Un'applicazione invia il messaggio **WM \_ MDIICONARRANGE** a una finestra del client di interfaccia a documenti multipli (MDI) per disporre tutte le finestre figlio MDI ridotte a icona.</span><span class="sxs-lookup"><span data-stu-id="6c873-105">An application sends the **WM\_MDIICONARRANGE** message to a multiple-document interface (MDI) client window to arrange all minimized MDI child windows.</span></span> <span data-ttu-id="6c873-106">Non influisce sulle finestre figlio non ridotte a icona.</span><span class="sxs-lookup"><span data-stu-id="6c873-106">It does not affect child windows that are not minimized.</span></span>


```C++
#define WM_MDIICONARRANGE               0x0228
```



## <a name="parameters"></a><span data-ttu-id="6c873-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="6c873-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c873-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6c873-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c873-109">Questo parametro non viene utilizzato. deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="6c873-109">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="6c873-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6c873-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c873-111">Questo parametro non viene utilizzato. deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="6c873-111">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6c873-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6c873-112">Requirements</span></span>



| <span data-ttu-id="6c873-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c873-113">Requirement</span></span> | <span data-ttu-id="6c873-114">Valore</span><span class="sxs-lookup"><span data-stu-id="6c873-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c873-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c873-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6c873-116">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6c873-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6c873-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c873-117">Minimum supported server</span></span><br/> | <span data-ttu-id="6c873-118">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6c873-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6c873-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6c873-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c873-120"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6c873-120"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c873-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6c873-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="6c873-122">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="6c873-122">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6c873-123">**\_MDICASCADE WM**</span><span class="sxs-lookup"><span data-stu-id="6c873-123">**WM\_MDICASCADE**</span></span>](wm-mdicascade.md)
</dt> <dt>

[<span data-ttu-id="6c873-124">**\_MDITILE WM**</span><span class="sxs-lookup"><span data-stu-id="6c873-124">**WM\_MDITILE**</span></span>](wm-mditile.md)
</dt> <dt>

<span data-ttu-id="6c873-125">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="6c873-125">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6c873-126">Interfaccia a documenti multipli</span><span class="sxs-lookup"><span data-stu-id="6c873-126">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 





---
title: Codice di notifica TBN_GETDISPINFO (COMmctrl. h)
description: Recupera le informazioni di visualizzazione per un elemento della barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: ed6e4141-2bf8-4a92-8349-f3833c87fcf3
keywords:
- Controlli di Windows per il codice di notifica TBN_GETDISPINFO
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5f3a0a47adfe7f172f7a4d0e4c9139b67aef01d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120670"
---
# <a name="tbn_getdispinfo-notification-code"></a><span data-ttu-id="30d24-105">\_Codice di notifica GETDISPINFO di TBN</span><span class="sxs-lookup"><span data-stu-id="30d24-105">TBN\_GETDISPINFO notification code</span></span>

<span data-ttu-id="30d24-106">Recupera le informazioni di visualizzazione per un elemento della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="30d24-106">Retrieves display information for a toolbar item.</span></span> <span data-ttu-id="30d24-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="30d24-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_GETDISPINFO 

    lptbdi = (LPNMTBDISPINFO) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="30d24-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="30d24-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30d24-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="30d24-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30d24-110">Puntatore a una struttura [**NMTBDISPINFO**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="30d24-110">Pointer to an [**NMTBDISPINFO**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbdispinfoa) structure.</span></span> <span data-ttu-id="30d24-111">Il membro **idCommand** specifica l'identificatore di comando dell'elemento, il membro **lParam** contiene i dati definiti dall'applicazione dell'elemento e il membro **dwMask** specifica quali informazioni vengono richieste.</span><span class="sxs-lookup"><span data-stu-id="30d24-111">The **idCommand** member specifies the item's command identifier, the **lParam** member contains the item's application-defined data, and the **dwMask** member specifies what information is being requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30d24-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="30d24-112">Return value</span></span>

<span data-ttu-id="30d24-113">Il valore restituito viene ignorato dal controllo.</span><span class="sxs-lookup"><span data-stu-id="30d24-113">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="30d24-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="30d24-114">Requirements</span></span>



| <span data-ttu-id="30d24-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="30d24-115">Requirement</span></span> | <span data-ttu-id="30d24-116">Valore</span><span class="sxs-lookup"><span data-stu-id="30d24-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="30d24-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30d24-117">Minimum supported client</span></span><br/> | <span data-ttu-id="30d24-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="30d24-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="30d24-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30d24-119">Minimum supported server</span></span><br/> | <span data-ttu-id="30d24-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="30d24-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="30d24-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="30d24-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="30d24-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="30d24-122"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="30d24-123">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="30d24-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="30d24-124">**TBN \_ GETDISPINFOW** (Unicode) e **TBN \_ GETDISPINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="30d24-124">**TBN\_GETDISPINFOW** (Unicode) and **TBN\_GETDISPINFOA** (ANSI)</span></span><br/>           |



 

 






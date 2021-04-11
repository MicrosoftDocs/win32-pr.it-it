---
title: Codice di notifica del NM_DBLCLK (scheda) (COMmctrl. h)
description: Notifica a una finestra padre di un controllo struttura a schede che l'utente ha fatto doppio clic con il pulsante sinistro del mouse all'interno del controllo. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: fd99f195-ceac-47e8-b584-d814b055fa21
keywords:
- Codice di notifica di NM_DBLCLK (tabulazione) controlli di Windows
topic_type:
- apiref
api_name:
- NM_DBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74c8171696e57684be55e6e42792666ae206d890
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120954"
---
# <a name="nm_dblclk-tab-notification-code"></a><span data-ttu-id="3b60c-105">\_Codice di notifica DBLCLK (TAB) Nm</span><span class="sxs-lookup"><span data-stu-id="3b60c-105">NM\_DBLCLK (tab) notification code</span></span>

<span data-ttu-id="3b60c-106">Notifica a una finestra padre di un controllo struttura a schede che l'utente ha fatto doppio clic con il pulsante sinistro del mouse all'interno del controllo.</span><span class="sxs-lookup"><span data-stu-id="3b60c-106">Notifies a parent window of a tab control that the user has double-clicked the left mouse button within the control.</span></span> <span data-ttu-id="3b60c-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="3b60c-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_DBLCLK
        
    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="3b60c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3b60c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b60c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3b60c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3b60c-110">Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.</span><span class="sxs-lookup"><span data-stu-id="3b60c-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b60c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3b60c-111">Return value</span></span>

<span data-ttu-id="3b60c-112">Restituisce un valore diverso da zero per non consentire l'elaborazione predefinita oppure zero per consentire l'elaborazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="3b60c-112">Return nonzero to not allow the default processing, or zero to allow the default processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b60c-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3b60c-113">Requirements</span></span>



| <span data-ttu-id="3b60c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b60c-114">Requirement</span></span> | <span data-ttu-id="3b60c-115">Valore</span><span class="sxs-lookup"><span data-stu-id="3b60c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3b60c-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b60c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3b60c-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3b60c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3b60c-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b60c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3b60c-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3b60c-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3b60c-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3b60c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b60c-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b60c-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






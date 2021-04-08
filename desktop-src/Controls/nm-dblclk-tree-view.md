---
title: Codice di notifica di NM_DBLCLK (visualizzazione albero) (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione albero che l'utente ha fatto doppio clic con il pulsante sinistro del mouse all'interno del controllo. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 2ed3b3ad-a252-496a-bfcf-0cec5678f192
keywords:
- NM_DBLCLK (visualizzazione albero) controlli di Windows per il codice di notifica
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
ms.openlocfilehash: 78f89671e1a26962eacf255d4c98ea0baa1578de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047852"
---
# <a name="nm_dblclk-tree-view-notification-code"></a><span data-ttu-id="39798-105">\_Codice di notifica di DBLCLK Nm (visualizzazione albero)</span><span class="sxs-lookup"><span data-stu-id="39798-105">NM\_DBLCLK (tree view) notification code</span></span>

<span data-ttu-id="39798-106">Notifica alla finestra padre di un controllo di visualizzazione albero che l'utente ha fatto doppio clic con il pulsante sinistro del mouse all'interno del controllo.</span><span class="sxs-lookup"><span data-stu-id="39798-106">Notifies the parent window of a tree-view control that the user has double-clicked the left mouse button within the control.</span></span> <span data-ttu-id="39798-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="39798-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_DBLCLK
        
    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="39798-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="39798-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39798-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="39798-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39798-110">Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.</span><span class="sxs-lookup"><span data-stu-id="39798-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39798-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="39798-111">Return value</span></span>

<span data-ttu-id="39798-112">Restituisce un valore diverso da zero per impedire l'elaborazione predefinita oppure zero per consentire l'elaborazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="39798-112">Return nonzero to prevent the default processing, or zero to allow the default processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="39798-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39798-113">Requirements</span></span>



| <span data-ttu-id="39798-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="39798-114">Requirement</span></span> | <span data-ttu-id="39798-115">Valore</span><span class="sxs-lookup"><span data-stu-id="39798-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39798-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="39798-116">Minimum supported client</span></span><br/> | <span data-ttu-id="39798-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="39798-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="39798-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="39798-118">Minimum supported server</span></span><br/> | <span data-ttu-id="39798-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="39798-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="39798-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="39798-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="39798-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="39798-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






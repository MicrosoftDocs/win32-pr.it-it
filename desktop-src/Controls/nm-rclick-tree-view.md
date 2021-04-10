---
title: Codice di notifica di NM_RCLICK (visualizzazione albero) (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione albero che l'utente ha fatto clic con il pulsante destro del mouse all'interno del controllo. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 5816d8b8-7f3d-477d-9116-1b3670d99240
keywords:
- NM_RCLICK (visualizzazione albero) controlli di Windows per il codice di notifica
topic_type:
- apiref
api_name:
- NM_RCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58d72ee220bf33189e8954a2e1ef454b22886553
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121730"
---
# <a name="nm_rclick-tree-view-notification-code"></a><span data-ttu-id="b63e9-105">\_Codice di notifica di RCLICK Nm (visualizzazione albero)</span><span class="sxs-lookup"><span data-stu-id="b63e9-105">NM\_RCLICK (tree view) notification code</span></span>

<span data-ttu-id="b63e9-106">Notifica alla finestra padre di un controllo di visualizzazione albero che l'utente ha fatto clic con il pulsante destro del mouse all'interno del controllo.</span><span class="sxs-lookup"><span data-stu-id="b63e9-106">Notifies the parent window of a tree-view control that the user has clicked the right mouse button within the control.</span></span> <span data-ttu-id="b63e9-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="b63e9-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RCLICK 

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="b63e9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b63e9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b63e9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b63e9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b63e9-110">Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.</span><span class="sxs-lookup"><span data-stu-id="b63e9-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b63e9-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b63e9-111">Return value</span></span>

<span data-ttu-id="b63e9-112">Restituisce un valore diverso da zero per impedire l'elaborazione predefinita oppure zero per consentire l'elaborazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="b63e9-112">Return nonzero to prevent the default processing, or zero to allow the default processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="b63e9-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b63e9-113">Requirements</span></span>



| <span data-ttu-id="b63e9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b63e9-114">Requirement</span></span> | <span data-ttu-id="b63e9-115">Valore</span><span class="sxs-lookup"><span data-stu-id="b63e9-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b63e9-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b63e9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b63e9-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b63e9-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b63e9-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b63e9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b63e9-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b63e9-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b63e9-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b63e9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b63e9-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b63e9-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






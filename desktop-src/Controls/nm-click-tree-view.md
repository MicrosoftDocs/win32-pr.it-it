---
title: Codice di notifica di NM_CLICK (visualizzazione albero) (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione albero che l'utente ha fatto clic con il pulsante sinistro del mouse all'interno del controllo. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 39b5716d-cae7-4dc4-b257-0118f4f432c6
keywords:
- NM_CLICK (visualizzazione albero) controlli di Windows per il codice di notifica
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45809a683d06871398e79419ec08729b1edcd2c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743986"
---
# <a name="nm_click-tree-view-notification-code"></a><span data-ttu-id="d5a17-105">NM \_ clic (visualizzazione albero) codice di notifica</span><span class="sxs-lookup"><span data-stu-id="d5a17-105">NM\_CLICK (tree view) notification code</span></span>

<span data-ttu-id="d5a17-106">Notifica alla finestra padre di un controllo di visualizzazione albero che l'utente ha fatto clic con il pulsante sinistro del mouse all'interno del controllo.</span><span class="sxs-lookup"><span data-stu-id="d5a17-106">Notifies the parent window of a tree-view control that the user has clicked the left mouse button within the control.</span></span> <span data-ttu-id="d5a17-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d5a17-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CLICK
        
    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="d5a17-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d5a17-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5a17-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d5a17-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d5a17-110">Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.</span><span class="sxs-lookup"><span data-stu-id="d5a17-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5a17-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d5a17-111">Return value</span></span>

<span data-ttu-id="d5a17-112">Restituisce un valore diverso da zero per impedire l'elaborazione predefinita oppure zero per consentire l'elaborazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="d5a17-112">Return nonzero to prevent the default processing, or zero to allow the default processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5a17-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d5a17-113">Requirements</span></span>



| <span data-ttu-id="d5a17-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5a17-114">Requirement</span></span> | <span data-ttu-id="d5a17-115">Valore</span><span class="sxs-lookup"><span data-stu-id="d5a17-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d5a17-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5a17-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d5a17-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d5a17-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d5a17-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5a17-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d5a17-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d5a17-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d5a17-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d5a17-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5a17-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5a17-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






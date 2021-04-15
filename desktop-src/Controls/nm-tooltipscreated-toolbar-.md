---
title: Codice di notifica NM_TOOLTIPSCREATED (barra degli strumenti) (COMmctrl. h)
description: Notifica alla finestra padre di una barra degli strumenti che la barra degli strumenti ha creato un controllo ToolTip. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 0e9517c1-aa3f-4b14-82b4-195a4ce99757
keywords:
- Codice di notifica di NM_TOOLTIPSCREATED (barra degli strumenti) controlli Windows
topic_type:
- apiref
api_name:
- NM_TOOLTIPSCREATED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c13366348da075fab48e7a2f12381f51f7d87bf4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476061"
---
# <a name="nm_tooltipscreated-toolbar-notification-code"></a><span data-ttu-id="e7b6b-105">\_Codice di notifica TOOLTIPSCREATED di Nm (barra degli strumenti)</span><span class="sxs-lookup"><span data-stu-id="e7b6b-105">NM\_TOOLTIPSCREATED (toolbar) notification code</span></span>

<span data-ttu-id="e7b6b-106">Notifica alla finestra padre di una barra degli strumenti che la barra degli strumenti ha creato un controllo ToolTip.</span><span class="sxs-lookup"><span data-stu-id="e7b6b-106">Notifies a toolbar's parent window that the toolbar has created a tooltip control.</span></span> <span data-ttu-id="e7b6b-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e7b6b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_TOOLTIPSCREATED

    lpnmttc = (LPNMTOOLTIPSCREATED) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="e7b6b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e7b6b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7b6b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e7b6b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7b6b-110">Puntatore a una struttura [**NMTOOLTIPSCREATED**](/windows/win32/api/commctrl/ns-commctrl-nmtooltipscreated) che contiene informazioni aggiuntive su questa notifica.</span><span class="sxs-lookup"><span data-stu-id="e7b6b-110">Pointer to an [**NMTOOLTIPSCREATED**](/windows/win32/api/commctrl/ns-commctrl-nmtooltipscreated) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7b6b-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e7b6b-111">Return value</span></span>

<span data-ttu-id="e7b6b-112">Il controllo Toolbar ignora il valore restituito da questo codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="e7b6b-112">The toolbar control ignores the return value from this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7b6b-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7b6b-113">Requirements</span></span>



| <span data-ttu-id="e7b6b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7b6b-114">Requirement</span></span> | <span data-ttu-id="e7b6b-115">Valore</span><span class="sxs-lookup"><span data-stu-id="e7b6b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e7b6b-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7b6b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e7b6b-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e7b6b-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e7b6b-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7b6b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e7b6b-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e7b6b-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e7b6b-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e7b6b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7b6b-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7b6b-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






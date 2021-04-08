---
title: Codice di notifica TVN_GETINFOTIP (COMmctrl. h)
description: Inviato da un controllo di visualizzazione albero con lo \_ stile INFOTIP TV. Questo codice di notifica viene inviato quando il controllo richiede la visualizzazione di informazioni aggiuntive sul testo in una descrizione comando. Il codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 20576710-e279-4e61-be6b-bf1d8ea79555
keywords:
- Controlli di Windows per il codice di notifica TVN_GETINFOTIP
topic_type:
- apiref
api_name:
- TVN_GETINFOTIP
- TVN_GETINFOTIPA
- TVN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1336571fa2c06e8b22078b1d761d9841217104e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742255"
---
# <a name="tvn_getinfotip-notification-code"></a><span data-ttu-id="d73c3-106">\_Codice di notifica GETINFOTIP di TVN</span><span class="sxs-lookup"><span data-stu-id="d73c3-106">TVN\_GETINFOTIP notification code</span></span>

<span data-ttu-id="d73c3-107">Inviato da un controllo di visualizzazione albero con lo stile [**\_ INFOTIP TV**](tree-view-control-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="d73c3-107">Sent by a tree-view control that has the [**TVS\_INFOTIP**](tree-view-control-window-styles.md) style.</span></span> <span data-ttu-id="d73c3-108">Questo codice di notifica viene inviato quando il controllo richiede la visualizzazione di informazioni aggiuntive sul testo in una descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="d73c3-108">This notification code is sent when the control is requesting additional text information to be displayed in a tooltip.</span></span> <span data-ttu-id="d73c3-109">Il codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d73c3-109">The notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_GETINFOTIP

    lpGetInfoTip = (LPNMTVGETINFOTIP)lParam;
```



## <a name="parameters"></a><span data-ttu-id="d73c3-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="d73c3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d73c3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d73c3-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d73c3-112">Puntatore a una struttura [**NMTVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmtvgetinfotipa) che contiene informazioni su questo codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="d73c3-112">Pointer to an [**NMTVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmtvgetinfotipa) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d73c3-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d73c3-113">Return value</span></span>

<span data-ttu-id="d73c3-114">Il controllo Ignora il valore restituito per questo codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="d73c3-114">The control ignores the return value for this notification code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d73c3-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="d73c3-115">Remarks</span></span>

<span data-ttu-id="d73c3-116">Questo codice di notifica viene inviato solo da controlli di visualizzazione albero con lo [**stile \_ INFOTIP TV**](tree-view-control-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="d73c3-116">This notification code is only sent by tree-view controls that have the [**TVS\_INFOTIP**](tree-view-control-window-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="d73c3-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d73c3-117">Requirements</span></span>



| <span data-ttu-id="d73c3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d73c3-118">Requirement</span></span> | <span data-ttu-id="d73c3-119">Valore</span><span class="sxs-lookup"><span data-stu-id="d73c3-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d73c3-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d73c3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d73c3-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d73c3-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d73c3-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d73c3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d73c3-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d73c3-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d73c3-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d73c3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d73c3-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d73c3-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="d73c3-126">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="d73c3-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d73c3-127">**TVN \_ GETINFOTIPW** (Unicode) e **TVN \_ GETINFOTIPA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d73c3-127">**TVN\_GETINFOTIPW** (Unicode) and **TVN\_GETINFOTIPA** (ANSI)</span></span><br/>             |



 

 






---
title: Codice di notifica HDN_DROPDOWN (COMmctrl. h)
description: Inviato da un controllo intestazione al relativo elemento padre quando si fa clic sulla freccia a discesa del controllo intestazione. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: cacf5cb9-0593-42ff-868d-b098481f565f
keywords:
- Controlli di Windows per il codice di notifica HDN_DROPDOWN
topic_type:
- apiref
api_name:
- HDN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c0ae7f2e2ee31feab1d8a2293913ac875a03718
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874717"
---
# <a name="hdn_dropdown-notification-code"></a><span data-ttu-id="b16bb-105">\_Codice di notifica a discesa HDN</span><span class="sxs-lookup"><span data-stu-id="b16bb-105">HDN\_DROPDOWN notification code</span></span>

<span data-ttu-id="b16bb-106">Inviato da un controllo intestazione al relativo elemento padre quando si fa clic sulla freccia a discesa del controllo intestazione.</span><span class="sxs-lookup"><span data-stu-id="b16bb-106">Sent by a header control to its parent when the drop-down arrow on the header control is clicked.</span></span> <span data-ttu-id="b16bb-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="b16bb-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_DROPDOWN
        
    pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="b16bb-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b16bb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b16bb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b16bb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b16bb-110">Puntatore a una struttura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) che contiene informazioni sul controllo intestazione.</span><span class="sxs-lookup"><span data-stu-id="b16bb-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information on the header control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b16bb-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b16bb-111">Return value</span></span>

<span data-ttu-id="b16bb-112">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="b16bb-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b16bb-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="b16bb-113">Remarks</span></span>

<span data-ttu-id="b16bb-114">Nell'esempio nella sezione Syntax viene illustrato come il ricevitore di notifiche esegue il cast di **lParam** per recuperare la struttura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) .</span><span class="sxs-lookup"><span data-stu-id="b16bb-114">The example in the Syntax section shows how the notification receiver casts **LPARAM** to retrieve the [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure.</span></span> <span data-ttu-id="b16bb-115">**WParam** contiene l'ID del controllo che invia questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="b16bb-115">**WPARAM** contains the ID of the control that sends this message.</span></span>

<span data-ttu-id="b16bb-116">Questo messaggio viene inviato solo se lo stile HDF \_ SPLITBUTTON è impostato sull'elemento dell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="b16bb-116">This message is sent only if style HDF\_SPLITBUTTON is set on the header item.</span></span>

## <a name="requirements"></a><span data-ttu-id="b16bb-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b16bb-117">Requirements</span></span>



| <span data-ttu-id="b16bb-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b16bb-118">Requirement</span></span> | <span data-ttu-id="b16bb-119">Valore</span><span class="sxs-lookup"><span data-stu-id="b16bb-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b16bb-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b16bb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b16bb-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b16bb-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b16bb-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b16bb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b16bb-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b16bb-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b16bb-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b16bb-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b16bb-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b16bb-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






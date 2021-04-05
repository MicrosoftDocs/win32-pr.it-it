---
title: Codice di notifica HDN_OVERFLOWCLICK (COMmctrl. h)
description: Inviato da un controllo intestazione al relativo padre quando si fa clic sul pulsante di overflow dell'intestazione. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 770ae00a-b87f-4de2-b869-2a233f2c493e
keywords:
- Controlli di Windows per il codice di notifica HDN_OVERFLOWCLICK
topic_type:
- apiref
api_name:
- HDN_OVERFLOWCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 911953fcbea785cb7024bc9d0670c8ed33239524
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873898"
---
# <a name="hdn_overflowclick-notification-code"></a><span data-ttu-id="7737b-105">\_Codice di notifica OVERFLOWCLICK di HDN</span><span class="sxs-lookup"><span data-stu-id="7737b-105">HDN\_OVERFLOWCLICK notification code</span></span>

<span data-ttu-id="7737b-106">Inviato da un controllo intestazione al relativo padre quando si fa clic sul pulsante di overflow dell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="7737b-106">Sent by a header control to its parent when the header's overflow button is clicked.</span></span> <span data-ttu-id="7737b-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7737b-107">This notification code is sent in the form of an [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_OVERFLOWCLICK

    pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="7737b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7737b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7737b-109">*lParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7737b-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7737b-110">Puntatore a una struttura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) che descrive il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="7737b-110">A pointer to a [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that describes the notification code.</span></span> <span data-ttu-id="7737b-111">Il processo chiamante è responsabile dell'allocazione di questa struttura, inclusa la struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contenuta.</span><span class="sxs-lookup"><span data-stu-id="7737b-111">The calling process is responsible for allocating this structure, including the contained [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span> <span data-ttu-id="7737b-112">Impostare i membri della struttura **NMHDR** , incluso il membro di *codice* che deve essere impostato su HDN \_ OVERFLOWCLICK.</span><span class="sxs-lookup"><span data-stu-id="7737b-112">Set the members of the **NMHDR** structure, including the *code* member that must be set to HDN\_OVERFLOWCLICK.</span></span>

<span data-ttu-id="7737b-113">Impostare il membro **iItem** della struttura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) sull'indice della prima voce di intestazione che non è visibile e pertanto deve essere visualizzato in un overflow.</span><span class="sxs-lookup"><span data-stu-id="7737b-113">Set the **iItem** member of the [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure to the index of the first header item that is not visible and thus should be displayed on an overflow.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7737b-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7737b-114">Return value</span></span>

<span data-ttu-id="7737b-115">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="7737b-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7737b-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="7737b-116">Remarks</span></span>

<span data-ttu-id="7737b-117">Il ricevitore di notifiche esegue il cast di **lParam** per recuperare la struttura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) .</span><span class="sxs-lookup"><span data-stu-id="7737b-117">The notification receiver casts **LPARAM** to retrieve the [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure.</span></span> <span data-ttu-id="7737b-118">**WParam** contiene l'ID del controllo che invia la notifica.</span><span class="sxs-lookup"><span data-stu-id="7737b-118">**WPARAM** contains the ID of the control that sends the notification.</span></span>

<span data-ttu-id="7737b-119">Questo messaggio viene inviato solo quando lo stile di [**\_ overflow HDS**](header-control-styles.md) è impostato sul controllo intestazione.</span><span class="sxs-lookup"><span data-stu-id="7737b-119">This message is sent only when style [**HDS\_OVERFLOW**](header-control-styles.md) is set on the header control.</span></span>

## <a name="requirements"></a><span data-ttu-id="7737b-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7737b-120">Requirements</span></span>



| <span data-ttu-id="7737b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7737b-121">Requirement</span></span> | <span data-ttu-id="7737b-122">Valore</span><span class="sxs-lookup"><span data-stu-id="7737b-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7737b-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7737b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7737b-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7737b-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7737b-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7737b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7737b-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7737b-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7737b-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7737b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="7737b-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7737b-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






---
title: Codice di notifica CBEN_ENDEDIT (COMmctrl. h)
description: Inviato quando l'utente ha concluso un'operazione all'interno della casella di modifica o ha selezionato un elemento dall'elenco a discesa del controllo. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: b6b50951-7304-4499-b57b-a5b592de2190
keywords:
- Controlli di Windows per il codice di notifica CBEN_ENDEDIT
topic_type:
- apiref
api_name:
- CBEN_ENDEDIT
- CBEN_ENDEDITA
- CBEN_ENDEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 679b9f878dbd8f7f374b461ee548f9ce2c62e281
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400262"
---
# <a name="cben_endedit-notification-code"></a><span data-ttu-id="da68a-105">Codice di notifica di CBEN \_ ENDEDIT</span><span class="sxs-lookup"><span data-stu-id="da68a-105">CBEN\_ENDEDIT notification code</span></span>

<span data-ttu-id="da68a-106">Inviato quando l'utente ha concluso un'operazione all'interno della casella di modifica o ha selezionato un elemento dall'elenco a discesa del controllo.</span><span class="sxs-lookup"><span data-stu-id="da68a-106">Sent when the user has concluded an operation within the edit box or has selected an item from the control's drop-down list.</span></span> <span data-ttu-id="da68a-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="da68a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
CBEN_ENDEDIT

    pnmEditInfo = (PNMCBEENDEDIT) lParam;
```



## <a name="parameters"></a><span data-ttu-id="da68a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="da68a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da68a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="da68a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da68a-110">Puntatore a una struttura [**NMCBEENDEDIT**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbeendedita) che contiene informazioni sul modo in cui l'utente ha concluso l'operazione di modifica.</span><span class="sxs-lookup"><span data-stu-id="da68a-110">A pointer to an [**NMCBEENDEDIT**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbeendedita) structure that contains information about how the user concluded the edit operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da68a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="da68a-111">Return value</span></span>

<span data-ttu-id="da68a-112">**False** per accettare il codice di notifica e consentire al controllo di visualizzare l'elemento selezionato; in caso contrario, **true**.</span><span class="sxs-lookup"><span data-stu-id="da68a-112">**FALSE** to accept the notification code and allow the control to display the selected item; otherwise, **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="da68a-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da68a-113">Requirements</span></span>



| <span data-ttu-id="da68a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="da68a-114">Requirement</span></span> | <span data-ttu-id="da68a-115">Valore</span><span class="sxs-lookup"><span data-stu-id="da68a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="da68a-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da68a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="da68a-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="da68a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="da68a-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da68a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="da68a-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="da68a-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="da68a-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="da68a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="da68a-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="da68a-121"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="da68a-122">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="da68a-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="da68a-123">**CBEN \_ ENDEDITW** (Unicode) e **CBEN \_ ENDEDITA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="da68a-123">**CBEN\_ENDEDITW** (Unicode) and **CBEN\_ENDEDITA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="da68a-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="da68a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da68a-125">Informazioni sui controlli ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="da68a-125">About ComboBoxEx Controls</span></span>](comboboxex-controls.md)
</dt> </dl>

 

 






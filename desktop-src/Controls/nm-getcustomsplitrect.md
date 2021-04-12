---
title: Codice di notifica NM_GETCUSTOMSPLITRECT (COMmctrl. h)
description: Inviato da un controllo pulsante al relativo elemento padre per ottenere le misurazioni per i due rettangoli del pulsante di suddivisione. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: ce72778d-3cca-46a4-9d05-40954a18681d
keywords:
- Controlli di Windows per il codice di notifica NM_GETCUSTOMSPLITRECT
topic_type:
- apiref
api_name:
- NM_GETCUSTOMSPLITRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97b839540da7e07069fdf56ed656ed8772d029eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104118986"
---
# <a name="nm_getcustomsplitrect-notification-code"></a><span data-ttu-id="7f301-105">\_Codice di notifica GETCUSTOMSPLITRECT Nm</span><span class="sxs-lookup"><span data-stu-id="7f301-105">NM\_GETCUSTOMSPLITRECT notification code</span></span>

<span data-ttu-id="7f301-106">Inviato da un controllo pulsante al relativo elemento padre per ottenere le misurazioni per i due rettangoli del pulsante di suddivisione.</span><span class="sxs-lookup"><span data-stu-id="7f301-106">Sent by a button control to its parent to get measurements for the two rectangles of the split button.</span></span> <span data-ttu-id="7f301-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7f301-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_GETCUSTOMSPLITRECT
        
    nmCustomSplit = (NMCUSTOMSPLITRECTINFO *) lParam;
```



## <a name="parameters"></a><span data-ttu-id="7f301-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7f301-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f301-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7f301-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7f301-110">Puntatore a un [**NMCUSTOMSPLITRECTINFO**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo) per ricevere informazioni sui rettangoli di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="7f301-110">A pointer to an [**NMCUSTOMSPLITRECTINFO**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo) to receive bounding rectangles information.</span></span> <span data-ttu-id="7f301-111">La struttura **NMCUSTOMSPLITRECTINFO** viene inviata con il codice di notifica come richiesta all'elemento padre per fornire misure per i rettangoli del pulsante di suddivisione.</span><span class="sxs-lookup"><span data-stu-id="7f301-111">The **NMCUSTOMSPLITRECTINFO** structure is sent with the notification code as a request for the parent to provide measurements for the rectangles of the split button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f301-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7f301-112">Return value</span></span>

<span data-ttu-id="7f301-113">Restituisce [**CDRF \_ SKIPDEFAULT**](cdrf-constants.md) per indicare al controllo Button di usare i valori restituiti nella struttura [**NMCUSTOMSPLITRECTINFO**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo) ; in caso contrario, restituisce [**CDRF \_ DODEFAULT**](cdrf-constants.md).</span><span class="sxs-lookup"><span data-stu-id="7f301-113">Return [**CDRF\_SKIPDEFAULT**](cdrf-constants.md) to tell the button control to use the values returned in the [**NMCUSTOMSPLITRECTINFO**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo) structure; otherwise, return [**CDRF\_DODEFAULT**](cdrf-constants.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7f301-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="7f301-114">Remarks</span></span>

<span data-ttu-id="7f301-115">Questo codice di notifica viene inviato da un controllo Button prima che venga disegnato.</span><span class="sxs-lookup"><span data-stu-id="7f301-115">This notification code is sent by a button control before it is drawn.</span></span> <span data-ttu-id="7f301-116">Il pulsante deve essere di tipo [**BS \_ SPLITBUTTON**](button-styles.md) o [**BS \_ DEFSPLITBUTTON**](button-styles.md).</span><span class="sxs-lookup"><span data-stu-id="7f301-116">The button must be of style [**BS\_SPLITBUTTON**](button-styles.md) or [**BS\_DEFSPLITBUTTON**](button-styles.md).</span></span> <span data-ttu-id="7f301-117">Se i rettangoli restituiti al controllo in *lParam* non sono validi, verranno ignorati.</span><span class="sxs-lookup"><span data-stu-id="7f301-117">If the rectangles returned to the control in *lParam* are not valid, they are ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f301-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7f301-118">Requirements</span></span>



| <span data-ttu-id="7f301-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f301-119">Requirement</span></span> | <span data-ttu-id="7f301-120">Valore</span><span class="sxs-lookup"><span data-stu-id="7f301-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7f301-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f301-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7f301-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7f301-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7f301-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f301-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7f301-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7f301-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7f301-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7f301-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f301-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f301-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






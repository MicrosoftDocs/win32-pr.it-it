---
title: Codice di notifica UDN_DELTAPOS (COMmctrl. h)
description: Inviato dal sistema operativo alla finestra padre di un controllo di scorrimento quando la posizione del controllo sta per essere modificata.
ms.assetid: 66262566-d35a-4b2a-8157-d1e789a21016
keywords:
- Controlli di Windows per il codice di notifica UDN_DELTAPOS
topic_type:
- apiref
api_name:
- UDN_DELTAPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec8f0ec2200d1f18e48c068b581b42868db197b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741682"
---
# <a name="udn_deltapos-notification-code"></a><span data-ttu-id="bb9bd-104">\_Codice di notifica DELTAPOS di UDN</span><span class="sxs-lookup"><span data-stu-id="bb9bd-104">UDN\_DELTAPOS notification code</span></span>

<span data-ttu-id="bb9bd-105">Inviato dal sistema operativo alla finestra padre di un controllo di scorrimento quando la posizione del controllo sta per essere modificata.</span><span class="sxs-lookup"><span data-stu-id="bb9bd-105">Sent by the operating system to the parent window of an up-down control when the position of the control is about to change.</span></span> <span data-ttu-id="bb9bd-106">Questo errore si verifica quando l'utente richiede una modifica nel valore premendo la freccia su o giù del controllo.</span><span class="sxs-lookup"><span data-stu-id="bb9bd-106">This happens when the user requests a change in the value by pressing the control's up or down arrow.</span></span> <span data-ttu-id="bb9bd-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="bb9bd-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
UDN_DELTAPOS 

    lpnmud = (LPNMUPDOWN) lParam;
```



## <a name="parameters"></a><span data-ttu-id="bb9bd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bb9bd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb9bd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bb9bd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb9bd-110">Puntatore a una struttura [**NMUPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmupdown) contenente informazioni sulla modifica della posizione.</span><span class="sxs-lookup"><span data-stu-id="bb9bd-110">Pointer to an [**NMUPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmupdown) structure that contains information about the position change.</span></span> <span data-ttu-id="bb9bd-111">Il membro **IPO** di questa struttura contiene la posizione corrente del controllo.</span><span class="sxs-lookup"><span data-stu-id="bb9bd-111">The **iPos** member of this structure contains the current position of the control.</span></span> <span data-ttu-id="bb9bd-112">Il membro **oggetto IDelta** della struttura è un intero con segno che contiene la modifica proposta nella posizione.</span><span class="sxs-lookup"><span data-stu-id="bb9bd-112">The **iDelta** member of the structure is a signed integer that contains the proposed change in position.</span></span> <span data-ttu-id="bb9bd-113">Se l'utente ha fatto clic sul pulsante verso l'alto, si tratta di un valore positivo.</span><span class="sxs-lookup"><span data-stu-id="bb9bd-113">If the user has clicked the up button, this is a positive value.</span></span> <span data-ttu-id="bb9bd-114">Se l'utente ha fatto clic sul pulsante giù, si tratta di un valore negativo.</span><span class="sxs-lookup"><span data-stu-id="bb9bd-114">If the user has clicked the down button, this is a negative value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb9bd-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bb9bd-115">Return value</span></span>

<span data-ttu-id="bb9bd-116">Restituisce un valore diverso da zero per impedire la modifica nella posizione del controllo oppure zero per consentire la modifica.</span><span class="sxs-lookup"><span data-stu-id="bb9bd-116">Return nonzero to prevent the change in the control's position, or zero to allow the change.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb9bd-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="bb9bd-117">Remarks</span></span>

<span data-ttu-id="bb9bd-118">Il \_ codice di notifica DELTAPOS di UDN viene inviato prima del messaggio [**WM \_ VSCROLL**](wm-vscroll.md) o [**WM \_ HSCROLL**](wm-hscroll.md) , che modifica effettivamente la posizione del controllo.</span><span class="sxs-lookup"><span data-stu-id="bb9bd-118">The UDN\_DELTAPOS notification code is sent before the [**WM\_VSCROLL**](wm-vscroll.md) or [**WM\_HSCROLL**](wm-hscroll.md) message, which actually changes the control's position.</span></span> <span data-ttu-id="bb9bd-119">In questo modo è possibile esaminare, consentire, modificare o impedire la modifica.</span><span class="sxs-lookup"><span data-stu-id="bb9bd-119">This lets you examine, allow, modify, or disallow the change.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb9bd-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb9bd-120">Requirements</span></span>



| <span data-ttu-id="bb9bd-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb9bd-121">Requirement</span></span> | <span data-ttu-id="bb9bd-122">Valore</span><span class="sxs-lookup"><span data-stu-id="bb9bd-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bb9bd-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb9bd-123">Minimum supported client</span></span><br/> | <span data-ttu-id="bb9bd-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bb9bd-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bb9bd-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb9bd-125">Minimum supported server</span></span><br/> | <span data-ttu-id="bb9bd-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bb9bd-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bb9bd-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bb9bd-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb9bd-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb9bd-128"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb9bd-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb9bd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb9bd-130">**\_comando WM**</span><span class="sxs-lookup"><span data-stu-id="bb9bd-130">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


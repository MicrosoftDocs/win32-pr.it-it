---
title: Codice di notifica di NM_CLICK (Syslink) (COMmctrl. h)
description: Notifica alla finestra padre di un controllo che l'utente ha fatto clic su un collegamento ipertestuale con il pulsante sinistro del mouse all'interno del controllo. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: e92d7c92-f2c6-44aa-bce5-3bb07c184e7d
keywords:
- NM_CLICK (Syslink) (codice di notifica) controlli Windows
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
ms.openlocfilehash: 2ea34682b0cfdfdf1206a133abe4fdb22b8af5cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121746"
---
# <a name="nm_click-syslink-notification-code"></a><span data-ttu-id="ee405-105">\_Codice di notifica di Syslink (clic)</span><span class="sxs-lookup"><span data-stu-id="ee405-105">NM\_CLICK (syslink) notification code</span></span>

<span data-ttu-id="ee405-106">Notifica alla finestra padre di un controllo che l'utente ha fatto clic su un collegamento ipertestuale con il pulsante sinistro del mouse all'interno del controllo.</span><span class="sxs-lookup"><span data-stu-id="ee405-106">Notifies a control's parent window that the user has clicked a hyperlink with the left mouse button within the control.</span></span> <span data-ttu-id="ee405-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ee405-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CLICK

    pnmLink = (PNMLINK) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="ee405-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ee405-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee405-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ee405-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ee405-110">Puntatore a una struttura [**NMLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlink) che contiene informazioni aggiuntive su questa notifica.</span><span class="sxs-lookup"><span data-stu-id="ee405-110">Pointer to an [**NMLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlink) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee405-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ee405-111">Return value</span></span>

<span data-ttu-id="ee405-112">Il valore restituito viene ignorato dal controllo.</span><span class="sxs-lookup"><span data-stu-id="ee405-112">The return value is ignored by the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee405-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="ee405-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ee405-114">Per usare questo codice di notifica, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="ee405-114">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="ee405-115">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ee405-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ee405-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ee405-116">Requirements</span></span>



| <span data-ttu-id="ee405-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee405-117">Requirement</span></span> | <span data-ttu-id="ee405-118">Valore</span><span class="sxs-lookup"><span data-stu-id="ee405-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ee405-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee405-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ee405-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ee405-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ee405-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee405-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ee405-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ee405-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ee405-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ee405-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee405-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee405-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee405-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ee405-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="ee405-126">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="ee405-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ee405-127">**NMLINK**</span><span class="sxs-lookup"><span data-stu-id="ee405-127">**NMLINK**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlink)
</dt> <dt>

[<span data-ttu-id="ee405-128">**\_notifica WM**</span><span class="sxs-lookup"><span data-stu-id="ee405-128">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 






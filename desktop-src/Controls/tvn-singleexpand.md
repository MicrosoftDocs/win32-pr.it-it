---
title: Codice di notifica TVN_SINGLEEXPAND (COMmctrl. h)
description: Inviato da un controllo di visualizzazione albero con lo \_ stile SINGLEEXPAND TVS quando l'utente apre o chiude un elemento della struttura ad albero usando un solo clic del mouse. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: ae738237-172a-400b-b9fe-33832224e299
keywords:
- Controlli di Windows per il codice di notifica TVN_SINGLEEXPAND
topic_type:
- apiref
api_name:
- TVN_SINGLEEXPAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 976c0e8acfee1f024e4ee7f88d9f745e4029ec82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475743"
---
# <a name="tvn_singleexpand-notification-code"></a><span data-ttu-id="350f4-105">\_Codice di notifica SINGLEEXPAND di TVN</span><span class="sxs-lookup"><span data-stu-id="350f4-105">TVN\_SINGLEEXPAND notification code</span></span>

<span data-ttu-id="350f4-106">Inviato da un controllo di visualizzazione albero con lo [**stile \_ SINGLEEXPAND TVS**](tree-view-control-window-styles.md) quando l'utente apre o chiude un elemento della struttura ad albero usando un solo clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="350f4-106">Sent by a tree-view control with the [**TVS\_SINGLEEXPAND**](tree-view-control-window-styles.md) style when the user opens or closes a tree item using a single click of the mouse.</span></span> <span data-ttu-id="350f4-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="350f4-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_SINGLEEXPAND

    lpnmtv = (LPNMTREEVIEW)lParam;
```



## <a name="parameters"></a><span data-ttu-id="350f4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="350f4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="350f4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="350f4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="350f4-110">Puntatore a una struttura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) che contiene informazioni su questo codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="350f4-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="350f4-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="350f4-111">Return value</span></span>

<span data-ttu-id="350f4-112">Restituisce TVNRET \_ default per consentire il comportamento predefinito.</span><span class="sxs-lookup"><span data-stu-id="350f4-112">Return TVNRET\_DEFAULT to allow the default behavior to occur.</span></span> <span data-ttu-id="350f4-113">Per modificare il comportamento predefinito, restituire:</span><span class="sxs-lookup"><span data-stu-id="350f4-113">To modify the default behavior, return:</span></span>



| <span data-ttu-id="350f4-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="350f4-114">Return code</span></span>                                                                                    | <span data-ttu-id="350f4-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="350f4-115">Description</span></span>                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="350f4-116"><dt>**\_SKIPOLD TVNRET**</dt></span><span class="sxs-lookup"><span data-stu-id="350f4-116"><dt>**TVNRET\_SKIPOLD**</dt></span></span> </dl> | <span data-ttu-id="350f4-117">Ignora l'elaborazione predefinita dell'elemento da deselezionare.</span><span class="sxs-lookup"><span data-stu-id="350f4-117">Skip default processing of the item being unselected.</span></span><br/> |
| <dl> <span data-ttu-id="350f4-118"><dt>**\_SKIPNEW TVNRET**</dt></span><span class="sxs-lookup"><span data-stu-id="350f4-118"><dt>**TVNRET\_SKIPNEW**</dt></span></span> </dl> | <span data-ttu-id="350f4-119">Ignora l'elaborazione predefinita dell'elemento selezionato.</span><span class="sxs-lookup"><span data-stu-id="350f4-119">Skip default processing of the item being selected.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="350f4-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="350f4-120">Remarks</span></span>

<span data-ttu-id="350f4-121">Per ignorare l'elaborazione predefinita di elementi selezionati e deselezionati, restituire sia TVNRET \_ SKIPOLD che TVNRET \_ SKIPNEW combinando questi elementi con un OR logico.</span><span class="sxs-lookup"><span data-stu-id="350f4-121">To skip default processing of selected and unselected items, return both TVNRET\_SKIPOLD and TVNRET\_SKIPNEW by combining them with a logical OR.</span></span>

<span data-ttu-id="350f4-122">Questo codice di notifica viene inviato solo da controlli di visualizzazione albero con lo [**stile \_ SINGLEEXPAND TV**](tree-view-control-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="350f4-122">This notification code is only sent by tree-view controls that have the [**TVS\_SINGLEEXPAND**](tree-view-control-window-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="350f4-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="350f4-123">Requirements</span></span>



| <span data-ttu-id="350f4-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="350f4-124">Requirement</span></span> | <span data-ttu-id="350f4-125">Valore</span><span class="sxs-lookup"><span data-stu-id="350f4-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="350f4-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="350f4-126">Minimum supported client</span></span><br/> | <span data-ttu-id="350f4-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="350f4-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="350f4-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="350f4-128">Minimum supported server</span></span><br/> | <span data-ttu-id="350f4-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="350f4-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="350f4-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="350f4-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="350f4-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="350f4-131"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






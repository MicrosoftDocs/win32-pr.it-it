---
title: Codice di notifica TVN_DELETEITEM (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione albero che è in corso l'eliminazione di un elemento. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 0d8801e0-02ae-40c9-8625-83d98b434d0a
keywords:
- Controlli di Windows per il codice di notifica TVN_DELETEITEM
topic_type:
- apiref
api_name:
- TVN_DELETEITEM
- TVN_DELETEITEMA
- TVN_DELETEITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2953ca0cf272b102a08fba0516d4891dccde9daf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476948"
---
# <a name="tvn_deleteitem-notification-code"></a><span data-ttu-id="66c4d-105">\_Codice di notifica DeleteItem di TVN</span><span class="sxs-lookup"><span data-stu-id="66c4d-105">TVN\_DELETEITEM notification code</span></span>

<span data-ttu-id="66c4d-106">Notifica alla finestra padre di un controllo di visualizzazione albero che è in corso l'eliminazione di un elemento.</span><span class="sxs-lookup"><span data-stu-id="66c4d-106">Notifies a tree-view control's parent window that an item is being deleted.</span></span> <span data-ttu-id="66c4d-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="66c4d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_DELETEITEM 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="66c4d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="66c4d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66c4d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="66c4d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="66c4d-110">Puntatore a una struttura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) .</span><span class="sxs-lookup"><span data-stu-id="66c4d-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="66c4d-111">Il membro **itemOld** è una struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) i cui membri **Hite** e **lParam** contengono informazioni valide sull'elemento da eliminare.</span><span class="sxs-lookup"><span data-stu-id="66c4d-111">The **itemOld** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure whose **hItem** and **lParam** members contain valid information about the item being deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66c4d-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="66c4d-112">Return value</span></span>

<span data-ttu-id="66c4d-113">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="66c4d-113">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="66c4d-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="66c4d-114">Remarks</span></span>

<span data-ttu-id="66c4d-115">Se il membro **lParam** della struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) punta alla memoria allocata dall'applicazione, è possibile liberarla quando si riceve il codice di \_ notifica di TVN DeleteItem.</span><span class="sxs-lookup"><span data-stu-id="66c4d-115">If the **lParam** member of the [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure points to memory allocated by your application, you can free it when you receive the TVN\_DELETEITEM notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="66c4d-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="66c4d-116">Requirements</span></span>



| <span data-ttu-id="66c4d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="66c4d-117">Requirement</span></span> | <span data-ttu-id="66c4d-118">Valore</span><span class="sxs-lookup"><span data-stu-id="66c4d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="66c4d-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66c4d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="66c4d-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="66c4d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="66c4d-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66c4d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="66c4d-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="66c4d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="66c4d-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="66c4d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="66c4d-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="66c4d-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="66c4d-125">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="66c4d-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="66c4d-126">**TVN \_ DELETEITEMW** (Unicode) e **TVN \_ DELETEITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="66c4d-126">**TVN\_DELETEITEMW** (Unicode) and **TVN\_DELETEITEMA** (ANSI)</span></span><br/>             |



 

 






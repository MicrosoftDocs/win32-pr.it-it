---
title: Messaggio LVM_ENSUREVISIBLE (COMmctrl. h)
description: Garantisce che un elemento della visualizzazione elenco sia interamente o parzialmente visibile, scorrendo il controllo elenco-visualizzazione, se necessario. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro EnsureVisible di ListView.
ms.assetid: 3564b6e6-b8b6-401b-85bc-8bd6261fc054
keywords:
- Controlli di Windows Message LVM_ENSUREVISIBLE
topic_type:
- apiref
api_name:
- LVM_ENSUREVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0ff4009399988f20f3e162114f91e4cff02820
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963769"
---
# <a name="lvm_ensurevisible-message"></a><span data-ttu-id="cda4f-105">\_Messaggio ENSUREVISIBLE LVM</span><span class="sxs-lookup"><span data-stu-id="cda4f-105">LVM\_ENSUREVISIBLE message</span></span>

<span data-ttu-id="cda4f-106">Garantisce che un elemento della visualizzazione elenco sia interamente o parzialmente visibile, scorrendo il controllo elenco-visualizzazione, se necessario.</span><span class="sxs-lookup"><span data-stu-id="cda4f-106">Ensures that a list-view item is either entirely or partially visible, scrolling the list-view control if necessary.</span></span> <span data-ttu-id="cda4f-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ EnsureVisible di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_ensurevisible) .</span><span class="sxs-lookup"><span data-stu-id="cda4f-107">You can send this message explicitly or by using the [**ListView\_EnsureVisible**](/windows/desktop/api/Commctrl/nf-commctrl-listview_ensurevisible) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="cda4f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="cda4f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cda4f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cda4f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cda4f-110">Indice dell'elemento della visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="cda4f-110">The index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="cda4f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cda4f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cda4f-112">Valore che specifica se l'elemento deve essere interamente visibile.</span><span class="sxs-lookup"><span data-stu-id="cda4f-112">A value specifying whether the item must be entirely visible.</span></span> <span data-ttu-id="cda4f-113">Se questo parametro è **true**, non viene eseguito alcuno scorrimento se l'elemento è almeno parzialmente visibile.</span><span class="sxs-lookup"><span data-stu-id="cda4f-113">If this parameter is **TRUE**, no scrolling occurs if the item is at least partially visible.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cda4f-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cda4f-114">Return value</span></span>

<span data-ttu-id="cda4f-115">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="cda4f-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cda4f-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="cda4f-116">Remarks</span></span>

<span data-ttu-id="cda4f-117">Il messaggio ha esito negativo se lo stile della finestra include [**LVS \_ NoScroll**](list-view-window-styles.md).</span><span class="sxs-lookup"><span data-stu-id="cda4f-117">The message fails if the window style includes [**LVS\_NOSCROLL**](list-view-window-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cda4f-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cda4f-118">Requirements</span></span>



| <span data-ttu-id="cda4f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="cda4f-119">Requirement</span></span> | <span data-ttu-id="cda4f-120">Valore</span><span class="sxs-lookup"><span data-stu-id="cda4f-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cda4f-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cda4f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cda4f-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cda4f-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cda4f-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cda4f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cda4f-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cda4f-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cda4f-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cda4f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="cda4f-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cda4f-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






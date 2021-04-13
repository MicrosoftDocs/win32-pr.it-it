---
title: Messaggio LVM_DELETEALLITEMS (COMmctrl. h)
description: Rimuove tutti gli elementi da un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro DeleteAllItems di ListView.
ms.assetid: 816bf565-79e9-4f5d-b5b4-5cdecce8a61c
keywords:
- Controlli di Windows Message LVM_DELETEALLITEMS
topic_type:
- apiref
api_name:
- LVM_DELETEALLITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e92344e3cccf7578b8953206a9550022f6c6095
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475202"
---
# <a name="lvm_deleteallitems-message"></a><span data-ttu-id="e6294-105">\_Messaggio DELETEALLITEMS LVM</span><span class="sxs-lookup"><span data-stu-id="e6294-105">LVM\_DELETEALLITEMS message</span></span>

<span data-ttu-id="e6294-106">Rimuove tutti gli elementi da un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="e6294-106">Removes all items from a list-view control.</span></span> <span data-ttu-id="e6294-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ DeleteAllItems di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteallitems) .</span><span class="sxs-lookup"><span data-stu-id="e6294-107">You can send this message explicitly or by using the [**ListView\_DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteallitems) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e6294-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e6294-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6294-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e6294-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e6294-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="e6294-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e6294-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e6294-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e6294-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="e6294-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6294-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e6294-113">Return value</span></span>

<span data-ttu-id="e6294-114">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e6294-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6294-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="e6294-115">Remarks</span></span>

<span data-ttu-id="e6294-116">Quando un controllo visualizzazione elenco riceve il messaggio **LVM \_ DELETEALLITEMS** , invia il codice di [**notifica \_ DELETEALLITEMS LVN**](lvn-deleteallitems.md) alla relativa finestra padre.</span><span class="sxs-lookup"><span data-stu-id="e6294-116">When a list-view control receives the **LVM\_DELETEALLITEMS** message, it sends the [**LVN\_DELETEALLITEMS**](lvn-deleteallitems.md) notification code to its parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6294-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e6294-117">Requirements</span></span>



| <span data-ttu-id="e6294-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6294-118">Requirement</span></span> | <span data-ttu-id="e6294-119">Valore</span><span class="sxs-lookup"><span data-stu-id="e6294-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e6294-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6294-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e6294-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e6294-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e6294-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6294-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e6294-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e6294-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e6294-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e6294-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6294-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6294-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






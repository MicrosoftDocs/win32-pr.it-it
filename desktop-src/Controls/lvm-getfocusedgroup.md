---
title: Messaggio LVM_GETFOCUSEDGROUP (COMmctrl. h)
description: Ottiene il gruppo con lo stato attivo. Inviare questo messaggio in modo esplicito o utilizzando la \_ macro GetFocusedGroup di ListView.
ms.assetid: c1902f35-84b7-4f46-89a6-e48148f06172
keywords:
- Controlli di Windows Message LVM_GETFOCUSEDGROUP
topic_type:
- apiref
api_name:
- LVM_GETFOCUSEDGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e0d12eb637ec1a421a5eaff58636df7bef8f449
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475166"
---
# <a name="lvm_getfocusedgroup-message"></a><span data-ttu-id="43fa3-105">\_Messaggio GETFOCUSEDGROUP LVM</span><span class="sxs-lookup"><span data-stu-id="43fa3-105">LVM\_GETFOCUSEDGROUP message</span></span>

<span data-ttu-id="43fa3-106">Ottiene il gruppo con lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="43fa3-106">Gets the group that has the focus.</span></span> <span data-ttu-id="43fa3-107">Inviare questo messaggio in modo esplicito o utilizzando la macro [**\_ GetFocusedGroup di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfocusedgroup) .</span><span class="sxs-lookup"><span data-stu-id="43fa3-107">Send this message explicitly or by using the [**ListView\_GetFocusedGroup**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfocusedgroup) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="43fa3-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="43fa3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43fa3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="43fa3-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="43fa3-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="43fa3-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="43fa3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="43fa3-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="43fa3-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="43fa3-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43fa3-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="43fa3-113">Return value</span></span>

<span data-ttu-id="43fa3-114">Restituisce l'indice del gruppo con stato LVGS \_ attivo oppure-1 se non è presente alcun gruppo con lo stato LVGS \_ .</span><span class="sxs-lookup"><span data-stu-id="43fa3-114">Returns the index of the group with state of LVGS\_FOCUSED, or -1 if there is no group with state of LVGS\_FOCUSED.</span></span>

## <a name="requirements"></a><span data-ttu-id="43fa3-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43fa3-115">Requirements</span></span>



| <span data-ttu-id="43fa3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="43fa3-116">Requirement</span></span> | <span data-ttu-id="43fa3-117">Valore</span><span class="sxs-lookup"><span data-stu-id="43fa3-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="43fa3-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43fa3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="43fa3-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="43fa3-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="43fa3-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43fa3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="43fa3-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="43fa3-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="43fa3-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="43fa3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="43fa3-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="43fa3-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






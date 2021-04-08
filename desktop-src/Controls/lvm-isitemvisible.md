---
title: Messaggio LVM_ISITEMVISIBLE (COMmctrl. h)
description: Indica se un elemento del controllo visualizzazione elenco è visibile. Inviare questo messaggio in modo esplicito o utilizzando la \_ macro IsItemVisible di ListView.
ms.assetid: 355be527-e2b9-46be-96a0-951d72216d92
keywords:
- Controlli di Windows Message LVM_ISITEMVISIBLE
topic_type:
- apiref
api_name:
- LVM_ISITEMVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a95116d2d6da6e3554e63a8149c9b91d6c97f76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874309"
---
# <a name="lvm_isitemvisible-message"></a><span data-ttu-id="52090-105">\_Messaggio ISITEMVISIBLE LVM</span><span class="sxs-lookup"><span data-stu-id="52090-105">LVM\_ISITEMVISIBLE message</span></span>

<span data-ttu-id="52090-106">Indica se un elemento del controllo visualizzazione elenco è visibile.</span><span class="sxs-lookup"><span data-stu-id="52090-106">Indicates if an item in the list-view control is visible.</span></span> <span data-ttu-id="52090-107">Inviare questo messaggio in modo esplicito o utilizzando la macro [**\_ IsItemVisible di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_isitemvisible) .</span><span class="sxs-lookup"><span data-stu-id="52090-107">Send this message explicitly or by using the [**ListView\_IsItemVisible**](/windows/desktop/api/Commctrl/nf-commctrl-listview_isitemvisible) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="52090-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="52090-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52090-109">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="52090-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52090-110">Indice dell'elemento nel controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="52090-110">An index of the item in the list-view control.</span></span>

</dd> <dt>

<span data-ttu-id="52090-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="52090-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="52090-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="52090-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52090-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="52090-113">Return value</span></span>

<span data-ttu-id="52090-114">Restituisce **true** se visibile o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="52090-114">Returns **TRUE** if visible, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="52090-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="52090-115">Requirements</span></span>



| <span data-ttu-id="52090-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="52090-116">Requirement</span></span> | <span data-ttu-id="52090-117">Valore</span><span class="sxs-lookup"><span data-stu-id="52090-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="52090-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52090-118">Minimum supported client</span></span><br/> | <span data-ttu-id="52090-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="52090-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="52090-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52090-120">Minimum supported server</span></span><br/> | <span data-ttu-id="52090-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="52090-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="52090-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="52090-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="52090-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="52090-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






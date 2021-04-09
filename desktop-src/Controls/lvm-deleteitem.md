---
title: Messaggio LVM_DELETEITEM (COMmctrl. h)
description: Rimuove un elemento da un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro DeleteItem di ListView.
ms.assetid: 0eddd4c1-7786-4a8c-a16d-9fd83cce98b3
keywords:
- Controlli di Windows Message LVM_DELETEITEM
topic_type:
- apiref
api_name:
- LVM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19fce5afbbaa6702f296df12acf7dad4edac16fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119010"
---
# <a name="lvm_deleteitem-message"></a><span data-ttu-id="8a14f-105">\_Messaggio DeleteItem LVM</span><span class="sxs-lookup"><span data-stu-id="8a14f-105">LVM\_DELETEITEM message</span></span>

<span data-ttu-id="8a14f-106">Rimuove un elemento da un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="8a14f-106">Removes an item from a list-view control.</span></span> <span data-ttu-id="8a14f-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ DeleteItem di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteitem) .</span><span class="sxs-lookup"><span data-stu-id="8a14f-107">You can send this message explicitly or by using the [**ListView\_DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8a14f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8a14f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a14f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8a14f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8a14f-110">Indice dell'elemento della visualizzazione elenco da eliminare.</span><span class="sxs-lookup"><span data-stu-id="8a14f-110">The index of the list-view item to delete.</span></span>

</dd> <dt>

<span data-ttu-id="8a14f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8a14f-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="8a14f-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="8a14f-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a14f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8a14f-113">Return value</span></span>

<span data-ttu-id="8a14f-114">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="8a14f-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a14f-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8a14f-115">Requirements</span></span>



| <span data-ttu-id="8a14f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a14f-116">Requirement</span></span> | <span data-ttu-id="8a14f-117">Valore</span><span class="sxs-lookup"><span data-stu-id="8a14f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8a14f-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8a14f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8a14f-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8a14f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8a14f-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8a14f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8a14f-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8a14f-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8a14f-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8a14f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a14f-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a14f-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






---
title: Messaggio LVM_GETCOLUMN (COMmctrl. h)
description: Ottiene gli attributi della colonna di un controllo di visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro ListView GetColumn.
ms.assetid: 59b4bbfc-6c38-4faa-8f2e-3ea5d24e55a6
keywords:
- Controlli di Windows Message LVM_GETCOLUMN
topic_type:
- apiref
api_name:
- LVM_GETCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eebf57138d27c31c5594f271e5d36a052b81673
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475173"
---
# <a name="lvm_getcolumn-message"></a><span data-ttu-id="66b0c-105">\_Messaggio GETCOLUMN LVM</span><span class="sxs-lookup"><span data-stu-id="66b0c-105">LVM\_GETCOLUMN message</span></span>

<span data-ttu-id="66b0c-106">Ottiene gli attributi della colonna di un controllo di visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="66b0c-106">Gets the attributes of a list-view control's column.</span></span> <span data-ttu-id="66b0c-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ListView \_ GetColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumn) .</span><span class="sxs-lookup"><span data-stu-id="66b0c-107">You can send this message explicitly or by using the [**ListView\_GetColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumn) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="66b0c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="66b0c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66b0c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="66b0c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="66b0c-110">Indice della colonna.</span><span class="sxs-lookup"><span data-stu-id="66b0c-110">The index of the column.</span></span>

</dd> <dt>

<span data-ttu-id="66b0c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="66b0c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="66b0c-112">Puntatore a una struttura [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) che specifica le informazioni per recuperare e ricevere informazioni sulla colonna.</span><span class="sxs-lookup"><span data-stu-id="66b0c-112">A pointer to an [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) structure that specifies the information to retrieve and receives information about the column.</span></span> <span data-ttu-id="66b0c-113">Il membro **mask** specifica gli attributi di colonna da recuperare.</span><span class="sxs-lookup"><span data-stu-id="66b0c-113">The **mask** member specifies which column attributes to retrieve.</span></span> <span data-ttu-id="66b0c-114">Se il membro **mask** specifica il \_ valore di testo LVCF, il membro **pszText** deve contenere l'indirizzo del buffer che riceve il testo dell'elemento e il membro **cchTextMax** deve specificare le dimensioni del buffer.</span><span class="sxs-lookup"><span data-stu-id="66b0c-114">If the **mask** member specifies the LVCF\_TEXT value, the **pszText** member must contain the address of the buffer that receives the item text and the **cchTextMax** member must specify the size of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66b0c-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="66b0c-115">Return value</span></span>

<span data-ttu-id="66b0c-116">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="66b0c-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="66b0c-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="66b0c-117">Requirements</span></span>



| <span data-ttu-id="66b0c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="66b0c-118">Requirement</span></span> | <span data-ttu-id="66b0c-119">Valore</span><span class="sxs-lookup"><span data-stu-id="66b0c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="66b0c-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66b0c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="66b0c-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="66b0c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="66b0c-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66b0c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="66b0c-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="66b0c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="66b0c-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="66b0c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="66b0c-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="66b0c-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






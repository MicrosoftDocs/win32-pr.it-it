---
title: Messaggio LVM_INSERTCOLUMN (COMmctrl. h)
description: Inserisce una nuova colonna in un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro InsertColumn di ListView.
ms.assetid: 1326e38e-bb45-4d0d-b5bc-ec684b3b92ef
keywords:
- Controlli di Windows Message LVM_INSERTCOLUMN
topic_type:
- apiref
api_name:
- LVM_INSERTCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8be89ff0b4ef417a715085582544112cb90cb6b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518646"
---
# <a name="lvm_insertcolumn-message"></a><span data-ttu-id="1d87f-105">\_Messaggio INSERTCOLUMN LVM</span><span class="sxs-lookup"><span data-stu-id="1d87f-105">LVM\_INSERTCOLUMN message</span></span>

<span data-ttu-id="1d87f-106">Inserisce una nuova colonna in un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="1d87f-106">Inserts a new column in a list-view control.</span></span> <span data-ttu-id="1d87f-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ InsertColumn di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) .</span><span class="sxs-lookup"><span data-stu-id="1d87f-107">You can send this message explicitly or by using the [**ListView\_InsertColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1d87f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1d87f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d87f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1d87f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d87f-110">Indice della nuova colonna.</span><span class="sxs-lookup"><span data-stu-id="1d87f-110">Index of the new column.</span></span>

</dd> <dt>

<span data-ttu-id="1d87f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1d87f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d87f-112">Puntatore a una struttura [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) che contiene gli attributi della nuova colonna.</span><span class="sxs-lookup"><span data-stu-id="1d87f-112">Pointer to an [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) structure that contains the attributes of the new column.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d87f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1d87f-113">Return value</span></span>

<span data-ttu-id="1d87f-114">Restituisce l'indice della nuova colonna se ha esito positivo oppure-1 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="1d87f-114">Returns the index of the new column if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d87f-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="1d87f-115">Remarks</span></span>

<span data-ttu-id="1d87f-116">Le colonne sono visibili solo nella visualizzazione report (Dettagli).</span><span class="sxs-lookup"><span data-stu-id="1d87f-116">Columns are visible only in report (details) view.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d87f-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1d87f-117">Requirements</span></span>



| <span data-ttu-id="1d87f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d87f-118">Requirement</span></span> | <span data-ttu-id="1d87f-119">Valore</span><span class="sxs-lookup"><span data-stu-id="1d87f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1d87f-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d87f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1d87f-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1d87f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1d87f-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d87f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1d87f-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1d87f-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1d87f-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1d87f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d87f-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d87f-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






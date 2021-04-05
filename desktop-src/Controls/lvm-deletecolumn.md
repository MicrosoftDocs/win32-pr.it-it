---
title: Messaggio LVM_DELETECOLUMN (COMmctrl. h)
description: Rimuove una colonna da un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro DeleteColumn di ListView.
ms.assetid: 1748a70b-9a13-4753-ac23-55b5652164c2
keywords:
- Controlli di Windows Message LVM_DELETECOLUMN
topic_type:
- apiref
api_name:
- LVM_DELETECOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: daa9005009ceaf42a01ede4f0f26334ae686c2df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739970"
---
# <a name="lvm_deletecolumn-message"></a><span data-ttu-id="cd51a-105">\_Messaggio DELETECOLUMN LVM</span><span class="sxs-lookup"><span data-stu-id="cd51a-105">LVM\_DELETECOLUMN message</span></span>

<span data-ttu-id="cd51a-106">Rimuove una colonna da un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="cd51a-106">Removes a column from a list-view control.</span></span> <span data-ttu-id="cd51a-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ DeleteColumn di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deletecolumn) .</span><span class="sxs-lookup"><span data-stu-id="cd51a-107">You can send this message explicitly or by using the [**ListView\_DeleteColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deletecolumn) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="cd51a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="cd51a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd51a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cd51a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd51a-110">Indice della colonna da eliminare.</span><span class="sxs-lookup"><span data-stu-id="cd51a-110">The index of the column to delete.</span></span>

</dd> <dt>

<span data-ttu-id="cd51a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cd51a-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="cd51a-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="cd51a-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd51a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cd51a-113">Return value</span></span>

<span data-ttu-id="cd51a-114">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="cd51a-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd51a-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="cd51a-115">Remarks</span></span>

<span data-ttu-id="cd51a-116">L'eliminazione della colonna zero di un controllo visualizzazione elenco è supportata solo in ComCtl32.dll versione 6 e successive.</span><span class="sxs-lookup"><span data-stu-id="cd51a-116">Deleting column zero of a list-view control is supported only in ComCtl32.dll version 6 and later.</span></span> <span data-ttu-id="cd51a-117">La versione 5 supporta anche l'eliminazione della colonna zero, ma solo dopo l'uso di [**CCM \_ Subversion**](ccm-setversion.md) per impostare la versione su 5 o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="cd51a-117">Version 5 also supports deleting column zero, but only after you use [**CCM\_SETVERSION**](ccm-setversion.md) to set the version to 5 or later.</span></span> <span data-ttu-id="cd51a-118">Nelle versioni precedenti alla 5, se è necessario eliminare la colonna zero, inserire una colonna fittizia di lunghezza zero di zero ed eliminare la colonna uno e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="cd51a-118">In versions prior to version 5, if you must delete column zero, insert a zero length dummy column zero and delete column one and above.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd51a-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd51a-119">Requirements</span></span>



| <span data-ttu-id="cd51a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd51a-120">Requirement</span></span> | <span data-ttu-id="cd51a-121">Valore</span><span class="sxs-lookup"><span data-stu-id="cd51a-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cd51a-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd51a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cd51a-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cd51a-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cd51a-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd51a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cd51a-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cd51a-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cd51a-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cd51a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd51a-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd51a-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






---
title: Messaggio LVM_GETTOPINDEX (COMmctrl. h)
description: Recupera l'indice dell'elemento visibile in primo piano in visualizzazione elenco o report. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetTopIndex di ListView.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_gettopindex.htm
keywords:
- Controlli di Windows Message LVM_GETTOPINDEX
topic_type:
- apiref
api_name:
- LVM_GETTOPINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb1cb080588d1825fcbd9e6c5e7b1b573fd7ad2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302290"
---
# <a name="lvm_gettopindex-message"></a><span data-ttu-id="23faf-105">\_Messaggio GETTOPINDEX LVM</span><span class="sxs-lookup"><span data-stu-id="23faf-105">LVM\_GETTOPINDEX message</span></span>

<span data-ttu-id="23faf-106">Recupera l'indice dell'elemento visibile in primo piano in visualizzazione elenco o report.</span><span class="sxs-lookup"><span data-stu-id="23faf-106">Retrieves the index of the topmost visible item when in list or report view.</span></span> <span data-ttu-id="23faf-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetTopIndex di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettopindex) .</span><span class="sxs-lookup"><span data-stu-id="23faf-107">You can send this message explicitly or by using the [**ListView\_GetTopIndex**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettopindex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="23faf-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="23faf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23faf-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="23faf-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="23faf-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="23faf-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="23faf-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="23faf-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="23faf-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="23faf-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23faf-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="23faf-113">Return value</span></span>

<span data-ttu-id="23faf-114">Restituisce l'indice dell'elemento in caso di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="23faf-114">Returns the index of the item if successful.</span></span> <span data-ttu-id="23faf-115">Restituisce zero se il controllo di visualizzazione elenco è in visualizzazione icona o icona piccola o se il controllo elenco-visualizzazione è in visualizzazione dettagli con gruppi abilitati.</span><span class="sxs-lookup"><span data-stu-id="23faf-115">Returns zero if the list-view control is in icon or small icon view, or if the list-view control is in details view with groups enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="23faf-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="23faf-116">Requirements</span></span>



| <span data-ttu-id="23faf-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="23faf-117">Requirement</span></span> | <span data-ttu-id="23faf-118">Valore</span><span class="sxs-lookup"><span data-stu-id="23faf-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="23faf-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23faf-119">Minimum supported client</span></span><br/> | <span data-ttu-id="23faf-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="23faf-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="23faf-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23faf-121">Minimum supported server</span></span><br/> | <span data-ttu-id="23faf-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="23faf-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="23faf-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="23faf-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="23faf-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="23faf-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






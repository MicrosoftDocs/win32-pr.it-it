---
title: Messaggio LVM_GETCOUNTPERPAGE (COMmctrl. h)
description: Calcola il numero di elementi che possono essere posizionati verticalmente nell'area visibile di un controllo di visualizzazione elenco in visualizzazione elenco o report. Vengono conteggiati solo gli elementi completamente visibili. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetCountPerPage di ListView.
ms.assetid: 2ffd2bb1-cddf-4a4a-a4a8-087c9dc3fec0
keywords:
- Controlli di Windows Message LVM_GETCOUNTPERPAGE
topic_type:
- apiref
api_name:
- LVM_GETCOUNTPERPAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 734d460754f9ae8a11c3a42d8eacebf31d0b6fc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047862"
---
# <a name="lvm_getcountperpage-message"></a><span data-ttu-id="c83d7-106">\_Messaggio GETCOUNTPERPAGE LVM</span><span class="sxs-lookup"><span data-stu-id="c83d7-106">LVM\_GETCOUNTPERPAGE message</span></span>

<span data-ttu-id="c83d7-107">Calcola il numero di elementi che possono essere posizionati verticalmente nell'area visibile di un controllo di visualizzazione elenco in visualizzazione elenco o report.</span><span class="sxs-lookup"><span data-stu-id="c83d7-107">Calculates the number of items that can fit vertically in the visible area of a list-view control when in list or report view.</span></span> <span data-ttu-id="c83d7-108">Vengono conteggiati solo gli elementi completamente visibili.</span><span class="sxs-lookup"><span data-stu-id="c83d7-108">Only fully visible items are counted.</span></span> <span data-ttu-id="c83d7-109">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetCountPerPage di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcountperpage) .</span><span class="sxs-lookup"><span data-stu-id="c83d7-109">You can send this message explicitly or by using the [**ListView\_GetCountPerPage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcountperpage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c83d7-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="c83d7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c83d7-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c83d7-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c83d7-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="c83d7-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c83d7-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c83d7-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c83d7-114">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="c83d7-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c83d7-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c83d7-115">Return value</span></span>

<span data-ttu-id="c83d7-116">Restituisce il numero di elementi completamente visibili in caso di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="c83d7-116">Returns the number of fully visible items if successful.</span></span> <span data-ttu-id="c83d7-117">Se la visualizzazione corrente è una visualizzazione icona o piccola, il valore restituito è il numero totale di elementi nel controllo elenco-visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="c83d7-117">If the current view is icon or small icon view, the return value is the total number of items in the list-view control.</span></span>

## <a name="requirements"></a><span data-ttu-id="c83d7-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c83d7-118">Requirements</span></span>



| <span data-ttu-id="c83d7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c83d7-119">Requirement</span></span> | <span data-ttu-id="c83d7-120">Valore</span><span class="sxs-lookup"><span data-stu-id="c83d7-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c83d7-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c83d7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c83d7-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c83d7-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c83d7-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c83d7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c83d7-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c83d7-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c83d7-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c83d7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c83d7-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c83d7-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






---
title: Messaggio LVM_CREATEDRAGIMAGE (COMmctrl. h)
description: Crea un elenco di immagini di trascinamento per l'elemento specificato. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro CreateDragImage di ListView.
ms.assetid: face4c8f-01ff-4f5a-a468-e306a50dae35
keywords:
- Controlli di Windows Message LVM_CREATEDRAGIMAGE
topic_type:
- apiref
api_name:
- LVM_CREATEDRAGIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace975b178fee85e2794b518a78b40b375c65ae7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119011"
---
# <a name="lvm_createdragimage-message"></a><span data-ttu-id="1d77b-105">\_Messaggio CREATEDRAGIMAGE LVM</span><span class="sxs-lookup"><span data-stu-id="1d77b-105">LVM\_CREATEDRAGIMAGE message</span></span>

<span data-ttu-id="1d77b-106">Crea un elenco di immagini di trascinamento per l'elemento specificato.</span><span class="sxs-lookup"><span data-stu-id="1d77b-106">Creates a drag image list for the specified item.</span></span> <span data-ttu-id="1d77b-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ CreateDragImage di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_createdragimage) .</span><span class="sxs-lookup"><span data-stu-id="1d77b-107">You can send this message explicitly or by using the [**ListView\_CreateDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_createdragimage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1d77b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1d77b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d77b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1d77b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d77b-110">Indice dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="1d77b-110">The index of the item.</span></span>

</dd> <dt>

<span data-ttu-id="1d77b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1d77b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d77b-112">Puntatore a una struttura di [**punti**](/previous-versions//dd162805(v=vs.85)) che riceve la posizione iniziale dell'angolo superiore sinistro dell'immagine, in coordinate della visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="1d77b-112">A pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that receives the initial location of the upper-left corner of the image, in view coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d77b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1d77b-113">Return value</span></span>

<span data-ttu-id="1d77b-114">Restituisce l'handle per l'elenco di immagini di trascinamento, in caso di esito positivo, oppure **null** .</span><span class="sxs-lookup"><span data-stu-id="1d77b-114">Returns the handle to the drag image list if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d77b-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="1d77b-115">Remarks</span></span>

<span data-ttu-id="1d77b-116">L'applicazione è responsabile dell'eliminazione dell'elenco di immagini quando non è più necessario.</span><span class="sxs-lookup"><span data-stu-id="1d77b-116">Your application is responsible for destroying the image list when it is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d77b-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1d77b-117">Requirements</span></span>



| <span data-ttu-id="1d77b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d77b-118">Requirement</span></span> | <span data-ttu-id="1d77b-119">Valore</span><span class="sxs-lookup"><span data-stu-id="1d77b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1d77b-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d77b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1d77b-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1d77b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1d77b-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d77b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1d77b-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1d77b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1d77b-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1d77b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d77b-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d77b-125"><dt>Commctrl.h</dt></span></span> </dl> |



 


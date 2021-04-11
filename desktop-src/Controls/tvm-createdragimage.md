---
title: Messaggio TVM_CREATEDRAGIMAGE (COMmctrl. h)
description: Crea una bitmap di trascinamento per l'elemento specificato in un controllo di visualizzazione albero.
ms.assetid: fbe97921-c9d3-473c-933c-d6bc0599e24d
keywords:
- Controlli di Windows Message TVM_CREATEDRAGIMAGE
topic_type:
- apiref
api_name:
- TVM_CREATEDRAGIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 189b37affc6a4382541faea13199cacfcb9b7df5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119919"
---
# <a name="tvm_createdragimage-message"></a><span data-ttu-id="17248-104">\_Messaggio CREATEDRAGIMAGE TVM</span><span class="sxs-lookup"><span data-stu-id="17248-104">TVM\_CREATEDRAGIMAGE message</span></span>

<span data-ttu-id="17248-105">Crea una bitmap di trascinamento per l'elemento specificato in un controllo di visualizzazione albero.</span><span class="sxs-lookup"><span data-stu-id="17248-105">Creates a dragging bitmap for the specified item in a tree-view control.</span></span> <span data-ttu-id="17248-106">Il messaggio crea anche un elenco di immagini per la bitmap e aggiunge la bitmap all'elenco di immagini.</span><span class="sxs-lookup"><span data-stu-id="17248-106">The message also creates an image list for the bitmap and adds the bitmap to the image list.</span></span> <span data-ttu-id="17248-107">Un'applicazione può visualizzare l'immagine durante il trascinamento dell'elemento utilizzando le funzioni dell'elenco immagini.</span><span class="sxs-lookup"><span data-stu-id="17248-107">An application can display the image when dragging the item by using the image list functions.</span></span> <span data-ttu-id="17248-108">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ CreateDragImage di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_createdragimage) .</span><span class="sxs-lookup"><span data-stu-id="17248-108">You can send this message explicitly or by using the [**TreeView\_CreateDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_createdragimage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="17248-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="17248-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17248-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="17248-110">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="17248-111">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="17248-111">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="17248-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="17248-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="17248-113">Handle per l'elemento che riceve la nuova bitmap di trascinamento.</span><span class="sxs-lookup"><span data-stu-id="17248-113">Handle to the item that receives the new dragging bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17248-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="17248-114">Return value</span></span>

<span data-ttu-id="17248-115">Restituisce l'handle all'elenco di immagini a cui è stata aggiunta la bitmap di trascinamento in caso di esito positivo; in caso contrario, **null** .</span><span class="sxs-lookup"><span data-stu-id="17248-115">Returns the handle to the image list to which the dragging bitmap was added if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="17248-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="17248-116">Remarks</span></span>

<span data-ttu-id="17248-117">Se si crea un controllo di visualizzazione albero senza un elenco di immagini associato, non è possibile usare il messaggio **TVM \_ CREATEDRAGIMAGE** per creare l'immagine da visualizzare durante un'operazione di trascinamento.</span><span class="sxs-lookup"><span data-stu-id="17248-117">If you create a tree-view control without an associated image list, you cannot use the **TVM\_CREATEDRAGIMAGE** message to create the image to display during a drag operation.</span></span> <span data-ttu-id="17248-118">È necessario implementare un metodo personalizzato per creare un cursore di trascinamento.</span><span class="sxs-lookup"><span data-stu-id="17248-118">You must implement your own method of creating a drag cursor.</span></span>

<span data-ttu-id="17248-119">L'applicazione è responsabile dell'eliminazione dell'elenco di immagini quando non è più necessario.</span><span class="sxs-lookup"><span data-stu-id="17248-119">Your application is responsible for destroying the image list when it is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="17248-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="17248-120">Requirements</span></span>



| <span data-ttu-id="17248-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="17248-121">Requirement</span></span> | <span data-ttu-id="17248-122">Valore</span><span class="sxs-lookup"><span data-stu-id="17248-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="17248-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17248-123">Minimum supported client</span></span><br/> | <span data-ttu-id="17248-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="17248-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="17248-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17248-125">Minimum supported server</span></span><br/> | <span data-ttu-id="17248-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="17248-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="17248-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="17248-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="17248-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="17248-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






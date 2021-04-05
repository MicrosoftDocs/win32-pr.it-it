---
title: Messaggio HDM_CREATEDRAGIMAGE (COMmctrl. h)
description: Crea una versione semi-trasparente dell'immagine di un elemento da utilizzare come immagine di trascinamento. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro CreateDragImage dell'intestazione.
ms.assetid: 1b9dc515-d327-4634-a424-cc15a32f0f7c
keywords:
- Controlli di Windows Message HDM_CREATEDRAGIMAGE
topic_type:
- apiref
api_name:
- HDM_CREATEDRAGIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9e801ad9771205b5f2e6df8e37bb0a0ad7f0bc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048522"
---
# <a name="hdm_createdragimage-message"></a><span data-ttu-id="0df73-105">\_Messaggio HDM CREATEDRAGIMAGE</span><span class="sxs-lookup"><span data-stu-id="0df73-105">HDM\_CREATEDRAGIMAGE message</span></span>

<span data-ttu-id="0df73-106">Crea una versione semi-trasparente dell'immagine di un elemento da utilizzare come immagine di trascinamento.</span><span class="sxs-lookup"><span data-stu-id="0df73-106">Creates a semi-transparent version of an item's image for use as a dragging image.</span></span> <span data-ttu-id="0df73-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ CreateDragImage dell'intestazione**](/windows/desktop/api/Commctrl/nf-commctrl-header_createdragimage) .</span><span class="sxs-lookup"><span data-stu-id="0df73-107">You can send this message explicitly or use the [**Header\_CreateDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-header_createdragimage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0df73-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0df73-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0df73-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0df73-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0df73-110">Indice in base zero dell'elemento all'interno del controllo intestazione.</span><span class="sxs-lookup"><span data-stu-id="0df73-110">The zero-based index of the item within the header control.</span></span> <span data-ttu-id="0df73-111">L'immagine assegnata a questo elemento rappresenta la base per l'immagine trasparente.</span><span class="sxs-lookup"><span data-stu-id="0df73-111">The image assigned to this item is the basis for the transparent image.</span></span>

</dd> <dt>

<span data-ttu-id="0df73-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0df73-112">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0df73-113">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="0df73-113">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0df73-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0df73-114">Return value</span></span>

<span data-ttu-id="0df73-115">Restituisce un handle a un elenco di immagini che contiene la nuova immagine come unico elemento.</span><span class="sxs-lookup"><span data-stu-id="0df73-115">Returns a handle to an image list that contains the new image as its only element.</span></span>

## <a name="requirements"></a><span data-ttu-id="0df73-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0df73-116">Requirements</span></span>



| <span data-ttu-id="0df73-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0df73-117">Requirement</span></span> | <span data-ttu-id="0df73-118">Valore</span><span class="sxs-lookup"><span data-stu-id="0df73-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0df73-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0df73-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0df73-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0df73-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0df73-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0df73-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0df73-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0df73-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0df73-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0df73-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0df73-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0df73-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






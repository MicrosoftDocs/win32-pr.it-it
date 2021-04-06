---
title: Messaggio HDM_GETIMAGELIST (COMmctrl. h)
description: Ottiene l'handle per l'elenco di immagini che è stato impostato per un controllo intestazione esistente. È possibile inviare questo messaggio in modo esplicito o usare l'intestazione \_ GetStateImageList o la macro header GetImages \_ .
ms.assetid: 3e1a979c-60c5-4538-bd4d-16238829062e
keywords:
- Controlli di Windows Message HDM_GETIMAGELIST
topic_type:
- apiref
api_name:
- HDM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e199d603af873f1957d33855ccf5c59a90a4002
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742279"
---
# <a name="hdm_getimagelist-message"></a><span data-ttu-id="fe55d-105">HDM \_ messaggio GETimagine</span><span class="sxs-lookup"><span data-stu-id="fe55d-105">HDM\_GETIMAGELIST message</span></span>

<span data-ttu-id="fe55d-106">Ottiene l'handle per l'elenco di immagini che è stato impostato per un controllo intestazione esistente.</span><span class="sxs-lookup"><span data-stu-id="fe55d-106">Gets the handle to the image list that has been set for an existing header control.</span></span> <span data-ttu-id="fe55d-107">È possibile inviare questo messaggio in modo esplicito o usare l'intestazione [**\_ GetStateImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_getstateimagelist) o la macro header [**\_ GetImages**](/windows/desktop/api/Commctrl/nf-commctrl-header_getimagelist) .</span><span class="sxs-lookup"><span data-stu-id="fe55d-107">You can send this message explicitly or use the [**Header\_GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_getimagelist) or [**Header\_GetStateImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_getstateimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fe55d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fe55d-108">Parameters</span></span>

<dl> <span data-ttu-id="fe55d-109"><dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="fe55d-109"><dt>*wParam* </dt> </span></span><dd><span data-ttu-id="fe55d-110">Uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="fe55d-110">One of the following values:</span></span>

| <span data-ttu-id="fe55d-111">Valore</span><span class="sxs-lookup"><span data-stu-id="fe55d-111">Value</span></span>                                                                                                                                                      | <span data-ttu-id="fe55d-112">Significato</span><span class="sxs-lookup"><span data-stu-id="fe55d-112">Meaning</span></span>                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="HDSIL_NORMAL"></span><span id="hdsil_normal"></span><dl> <span data-ttu-id="fe55d-113"><dt>**HDSIL \_ normale**</dt></span><span class="sxs-lookup"><span data-stu-id="fe55d-113"><dt>**HDSIL\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="fe55d-114">Indica che si tratta di un elenco di immagini normale.</span><span class="sxs-lookup"><span data-stu-id="fe55d-114">Indicates that this is a normal image list.</span></span><br/> |
| <span id="HDSIL_STATE"></span><span id="hdsil_state"></span><dl> <span data-ttu-id="fe55d-115"><dt>**\_stato HDSIL**</dt></span><span class="sxs-lookup"><span data-stu-id="fe55d-115"><dt>**HDSIL\_STATE**</dt></span></span> </dl>    | <span data-ttu-id="fe55d-116">Indica che si tratta di un elenco di immagini di stato.</span><span class="sxs-lookup"><span data-stu-id="fe55d-116">Indicates that this is a state image list.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="fe55d-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fe55d-117">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="fe55d-118">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="fe55d-118">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe55d-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fe55d-119">Return value</span></span>

<span data-ttu-id="fe55d-120">Restituisce un handle per il set di elenchi di immagini per il controllo intestazione.</span><span class="sxs-lookup"><span data-stu-id="fe55d-120">Returns a handle to the image list set for the header control.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe55d-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe55d-121">Requirements</span></span>



| <span data-ttu-id="fe55d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe55d-122">Requirement</span></span> | <span data-ttu-id="fe55d-123">Valore</span><span class="sxs-lookup"><span data-stu-id="fe55d-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fe55d-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe55d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fe55d-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fe55d-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fe55d-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe55d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fe55d-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fe55d-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fe55d-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fe55d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe55d-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe55d-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






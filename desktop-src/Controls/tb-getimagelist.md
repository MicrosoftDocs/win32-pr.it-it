---
title: Messaggio TB_GETIMAGELIST (COMmctrl. h)
description: Recupera l'elenco di immagini utilizzato da un controllo Toolbar per visualizzare i pulsanti nello stato predefinito. Un controllo toolbar utilizza questo elenco immagini per visualizzare i pulsanti quando non sono attivi o disabilitati.
ms.assetid: 21edde99-019b-495c-a38b-4d686e124f8e
keywords:
- Controlli di Windows Message TB_GETIMAGELIST
topic_type:
- apiref
api_name:
- TB_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07a56b8b847bd212e703d3b512b255cf1693abf7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740274"
---
# <a name="tb_getimagelist-message"></a><span data-ttu-id="55c34-105">TB \_ messaggio GETimagine</span><span class="sxs-lookup"><span data-stu-id="55c34-105">TB\_GETIMAGELIST message</span></span>

<span data-ttu-id="55c34-106">Recupera l'elenco di immagini utilizzato da un controllo Toolbar per visualizzare i pulsanti nello stato predefinito.</span><span class="sxs-lookup"><span data-stu-id="55c34-106">Retrieves the image list that a toolbar control uses to display buttons in their default state.</span></span> <span data-ttu-id="55c34-107">Un controllo toolbar utilizza questo elenco immagini per visualizzare i pulsanti quando non sono attivi o disabilitati.</span><span class="sxs-lookup"><span data-stu-id="55c34-107">A toolbar control uses this image list to display buttons when they are not hot or disabled.</span></span>

## <a name="parameters"></a><span data-ttu-id="55c34-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="55c34-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55c34-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="55c34-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="55c34-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="55c34-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="55c34-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="55c34-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="55c34-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="55c34-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55c34-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="55c34-113">Return value</span></span>

<span data-ttu-id="55c34-114">Restituisce l'handle per l'elenco di immagini oppure **null** se non è impostato alcun elenco di immagini.</span><span class="sxs-lookup"><span data-stu-id="55c34-114">Returns the handle to the image list, or **NULL** if no image list is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="55c34-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="55c34-115">Requirements</span></span>



| <span data-ttu-id="55c34-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="55c34-116">Requirement</span></span> | <span data-ttu-id="55c34-117">Valore</span><span class="sxs-lookup"><span data-stu-id="55c34-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="55c34-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55c34-118">Minimum supported client</span></span><br/> | <span data-ttu-id="55c34-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="55c34-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="55c34-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55c34-120">Minimum supported server</span></span><br/> | <span data-ttu-id="55c34-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="55c34-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="55c34-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="55c34-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="55c34-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="55c34-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






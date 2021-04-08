---
title: Messaggio TCM_SETIMAGELIST (COMmctrl. h)
description: Assegna un elenco di immagini a un controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TabCtrl.
ms.assetid: b457c73c-4c38-4bc5-af5d-12bbd24504a6
keywords:
- Controlli di Windows Message TCM_SETIMAGELIST
topic_type:
- apiref
api_name:
- TCM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59172c677998e816b295939c14effe45ff8aa961
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047842"
---
# <a name="tcm_setimagelist-message"></a><span data-ttu-id="e8e29-105">Messaggio dell'immagine di TCM \_</span><span class="sxs-lookup"><span data-stu-id="e8e29-105">TCM\_SETIMAGELIST message</span></span>

<span data-ttu-id="e8e29-106">Assegna un elenco di immagini a un controllo struttura a schede.</span><span class="sxs-lookup"><span data-stu-id="e8e29-106">Assigns an image list to a tab control.</span></span> <span data-ttu-id="e8e29-107">È possibile inviare questo messaggio in modo esplicito o utilizzando [**la \_ macro TabCtrl**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setimagelist) .</span><span class="sxs-lookup"><span data-stu-id="e8e29-107">You can send this message explicitly or by using the [**TabCtrl\_SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e8e29-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e8e29-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8e29-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e8e29-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e8e29-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="e8e29-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e8e29-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e8e29-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e8e29-112">Handle per l'elenco di immagini da assegnare al controllo struttura a schede.</span><span class="sxs-lookup"><span data-stu-id="e8e29-112">Handle to the image list to assign to the tab control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8e29-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e8e29-113">Return value</span></span>

<span data-ttu-id="e8e29-114">Restituisce l'handle per l'elenco di immagini precedente oppure **null** se non è presente un elenco di immagini precedente.</span><span class="sxs-lookup"><span data-stu-id="e8e29-114">Returns the handle to the previous image list, or **NULL** if there is no previous image list.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8e29-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8e29-115">Requirements</span></span>



| <span data-ttu-id="e8e29-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8e29-116">Requirement</span></span> | <span data-ttu-id="e8e29-117">Valore</span><span class="sxs-lookup"><span data-stu-id="e8e29-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e8e29-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8e29-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e8e29-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e8e29-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e8e29-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8e29-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e8e29-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e8e29-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e8e29-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e8e29-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8e29-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8e29-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






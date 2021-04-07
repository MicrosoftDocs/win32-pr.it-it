---
title: Messaggio TCM_GETIMAGELIST (COMmctrl. h)
description: Recupera l'elenco di immagini associato a un controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TabCtrl Getimagine.
ms.assetid: 86a0d8c7-ff3d-4e16-994e-4c72d1e62e9f
keywords:
- Controlli di Windows Message TCM_GETIMAGELIST
topic_type:
- apiref
api_name:
- TCM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c4d471ef4d072e4305507f4f5ebc4a8f2745ed9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874410"
---
# <a name="tcm_getimagelist-message"></a><span data-ttu-id="6e55b-105">\_Messaggio TCM GETimages</span><span class="sxs-lookup"><span data-stu-id="6e55b-105">TCM\_GETIMAGELIST message</span></span>

<span data-ttu-id="6e55b-106">Recupera l'elenco di immagini associato a un controllo struttura a schede.</span><span class="sxs-lookup"><span data-stu-id="6e55b-106">Retrieves the image list associated with a tab control.</span></span> <span data-ttu-id="6e55b-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**TabCtrl \_ getimagine**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getimagelist) .</span><span class="sxs-lookup"><span data-stu-id="6e55b-107">You can send this message explicitly or by using the [**TabCtrl\_GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6e55b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6e55b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e55b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6e55b-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6e55b-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="6e55b-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6e55b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6e55b-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6e55b-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="6e55b-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e55b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6e55b-113">Return value</span></span>

<span data-ttu-id="6e55b-114">Restituisce l'handle per l'elenco di immagini, se ha esito positivo, oppure **null** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="6e55b-114">Returns the handle to the image list if successful, or **NULL** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e55b-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6e55b-115">Requirements</span></span>



| <span data-ttu-id="6e55b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e55b-116">Requirement</span></span> | <span data-ttu-id="6e55b-117">Valore</span><span class="sxs-lookup"><span data-stu-id="6e55b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6e55b-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e55b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6e55b-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6e55b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6e55b-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e55b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6e55b-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6e55b-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6e55b-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6e55b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e55b-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e55b-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






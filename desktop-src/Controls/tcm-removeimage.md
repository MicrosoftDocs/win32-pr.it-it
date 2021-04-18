---
title: Messaggio TCM_REMOVEIMAGE (COMmctrl. h)
description: Rimuove un'immagine dall'elenco di immagini di un controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TabCtrl RemoveImage.
ms.assetid: f2761338-0afa-47d8-9d9c-1d5a4a7f7bcf
keywords:
- Controlli di Windows Message TCM_REMOVEIMAGE
topic_type:
- apiref
api_name:
- TCM_REMOVEIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cbc51aa0efed847e39e735443c0d42e288bbaab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302515"
---
# <a name="tcm_removeimage-message"></a><span data-ttu-id="2da86-105">\_Messaggio TCM REMOVEIMAGE</span><span class="sxs-lookup"><span data-stu-id="2da86-105">TCM\_REMOVEIMAGE message</span></span>

<span data-ttu-id="2da86-106">Rimuove un'immagine dall'elenco di immagini di un controllo struttura a schede.</span><span class="sxs-lookup"><span data-stu-id="2da86-106">Removes an image from a tab control's image list.</span></span> <span data-ttu-id="2da86-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**TabCtrl \_ RemoveImage**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_removeimage) .</span><span class="sxs-lookup"><span data-stu-id="2da86-107">You can send this message explicitly or by using the [**TabCtrl\_RemoveImage**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_removeimage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2da86-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2da86-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2da86-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2da86-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2da86-110">Indice dell'immagine da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="2da86-110">Index of the image to remove.</span></span>

</dd> <dt>

<span data-ttu-id="2da86-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2da86-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2da86-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="2da86-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2da86-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2da86-113">Return value</span></span>

<span data-ttu-id="2da86-114">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="2da86-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2da86-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="2da86-115">Remarks</span></span>

<span data-ttu-id="2da86-116">Il controllo struttura a schede aggiorna l'indice dell'immagine di ogni scheda, in modo che ogni scheda rimanga associata alla stessa immagine precedente.</span><span class="sxs-lookup"><span data-stu-id="2da86-116">The tab control updates each tab's image index, so each tab remains associated with the same image as before.</span></span> <span data-ttu-id="2da86-117">Se una scheda usa l'immagine da rimuovere, la scheda verrà impostata in modo da non avere alcuna immagine.</span><span class="sxs-lookup"><span data-stu-id="2da86-117">If a tab is using the image being removed, the tab will be set to have no image.</span></span>

## <a name="requirements"></a><span data-ttu-id="2da86-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2da86-118">Requirements</span></span>



| <span data-ttu-id="2da86-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2da86-119">Requirement</span></span> | <span data-ttu-id="2da86-120">Valore</span><span class="sxs-lookup"><span data-stu-id="2da86-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2da86-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2da86-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2da86-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2da86-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2da86-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2da86-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2da86-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2da86-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2da86-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2da86-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2da86-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2da86-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






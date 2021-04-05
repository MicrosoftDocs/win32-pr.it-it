---
title: Messaggio BCM_SETIMAGELIST (COMmctrl. h)
description: Assegna un elenco di immagini a un controllo Button. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro Button.
ms.assetid: 805d2d9b-3e8f-4323-abaf-0dd5765cd740
keywords:
- Controlli di Windows Message BCM_SETIMAGELIST
topic_type:
- apiref
api_name:
- BCM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9bdf29735958f3c40af544bca4b946458df8431
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048266"
---
# <a name="bcm_setimagelist-message"></a><span data-ttu-id="2ae46-105">\_Messaggio SUBimage di BCM</span><span class="sxs-lookup"><span data-stu-id="2ae46-105">BCM\_SETIMAGELIST message</span></span>

<span data-ttu-id="2ae46-106">Assegna un elenco di immagini a un controllo Button.</span><span class="sxs-lookup"><span data-stu-id="2ae46-106">Assigns an image list to a button control.</span></span> <span data-ttu-id="2ae46-107">È possibile inviare questo messaggio in modo esplicito o [**usare \_ la macro Button**](/windows/desktop/api/Commctrl/nf-commctrl-button_setimagelist) .</span><span class="sxs-lookup"><span data-stu-id="2ae46-107">You can send this message explicitly or use the [**Button\_SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_setimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2ae46-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2ae46-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ae46-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2ae46-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ae46-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="2ae46-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2ae46-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2ae46-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ae46-112">Puntatore a una struttura del [**pulsante \_ ImageList**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) che contiene informazioni sull'elenco di immagini.</span><span class="sxs-lookup"><span data-stu-id="2ae46-112">A pointer to a [**BUTTON\_IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) structure that contains image list information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ae46-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2ae46-113">Return value</span></span>

<span data-ttu-id="2ae46-114">Se il messaggio ha esito positivo, restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="2ae46-114">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="2ae46-115">In caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="2ae46-115">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ae46-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="2ae46-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2ae46-117">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="2ae46-117">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="2ae46-118">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="2ae46-118">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

<span data-ttu-id="2ae46-119">L'elenco di immagini a cui si fa riferimento nel membro **himl** della struttura [**\_ ImageList del pulsante**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) deve contenere una singola immagine da usare per tutti gli Stati o singole immagini per ogni stato.</span><span class="sxs-lookup"><span data-stu-id="2ae46-119">The image list referred to in the **himl** member of the [**BUTTON\_IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) structure should contain either a single image to be used for all states or individual images for each state.</span></span> <span data-ttu-id="2ae46-120">Gli Stati seguenti sono definiti in vssym32. h.</span><span class="sxs-lookup"><span data-stu-id="2ae46-120">The following states are defined in vssym32.h.</span></span>

``` syntax
enum PUSHBUTTONSTATES {
    PBS_NORMAL = 1,
    PBS_HOT = 2,
    PBS_PRESSED = 3,
    PBS_DISABLED = 4,
    PBS_DEFAULTED = 5,
    PBS_STYLUSHOT = 6,
};
```

<span data-ttu-id="2ae46-121">Si noti che PBS \_ STYLUSHOT viene utilizzato solo nei computer tablet.</span><span class="sxs-lookup"><span data-stu-id="2ae46-121">Note that PBS\_STYLUSHOT is used only on tablet computers.</span></span>

<span data-ttu-id="2ae46-122">Ogni valore è un indice dell'immagine appropriata nell'elenco immagini.</span><span class="sxs-lookup"><span data-stu-id="2ae46-122">Each value is an index to the appropriate image in the image list.</span></span> <span data-ttu-id="2ae46-123">Se è presente una sola immagine, viene usata per tutti gli Stati.</span><span class="sxs-lookup"><span data-stu-id="2ae46-123">If only one image is present, it is used for all states.</span></span> <span data-ttu-id="2ae46-124">Se l'elenco di immagini contiene più di un'immagine, ogni indice corrisponde a uno stato del pulsante.</span><span class="sxs-lookup"><span data-stu-id="2ae46-124">If the image list contains more than one image, each index corresponds to one state of the button.</span></span> <span data-ttu-id="2ae46-125">Se non viene specificata un'immagine per ogni stato, non viene disegnato alcun elemento per tali Stati senza immagini.</span><span class="sxs-lookup"><span data-stu-id="2ae46-125">If an image is not provided for each state, nothing is drawn for those states without images.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ae46-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2ae46-126">Requirements</span></span>



| <span data-ttu-id="2ae46-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ae46-127">Requirement</span></span> | <span data-ttu-id="2ae46-128">Valore</span><span class="sxs-lookup"><span data-stu-id="2ae46-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2ae46-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ae46-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2ae46-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2ae46-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2ae46-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ae46-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2ae46-132">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2ae46-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2ae46-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2ae46-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ae46-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ae46-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






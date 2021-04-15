---
title: Messaggio BCM_GETIMAGELIST (COMmctrl. h)
description: Ottiene la \_ struttura ImageList del pulsante che descrive l'elenco di immagini assegnato a un controllo Button. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro Button Getimagine.
ms.assetid: 79383758-53d4-4955-b472-befd338cbec6
keywords:
- Controlli di Windows Message BCM_GETIMAGELIST
topic_type:
- apiref
api_name:
- BCM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b0c28e997e23d6df63150fe2283d04be1a8c0d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476996"
---
# <a name="bcm_getimagelist-message"></a><span data-ttu-id="ac9ab-105">\_Messaggio GETimagine BCM</span><span class="sxs-lookup"><span data-stu-id="ac9ab-105">BCM\_GETIMAGELIST message</span></span>

<span data-ttu-id="ac9ab-106">Ottiene la [**struttura \_ ImageList del pulsante**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) che descrive l'elenco di immagini assegnato a un controllo Button.</span><span class="sxs-lookup"><span data-stu-id="ac9ab-106">Gets the [**BUTTON\_IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) structure that describes the image list assigned to a button control.</span></span> <span data-ttu-id="ac9ab-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**Button \_ getimagine**](/windows/desktop/api/Commctrl/nf-commctrl-button_getimagelist) .</span><span class="sxs-lookup"><span data-stu-id="ac9ab-107">You can send this message explicitly or use the [**Button\_GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_getimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ac9ab-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ac9ab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac9ab-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ac9ab-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ac9ab-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="ac9ab-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ac9ab-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ac9ab-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ac9ab-112">Puntatore a una struttura del [**pulsante \_ ImageList**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) che contiene informazioni sull'elenco di immagini.</span><span class="sxs-lookup"><span data-stu-id="ac9ab-112">A pointer to a [**BUTTON\_IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) structure that contains image list information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac9ab-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ac9ab-113">Return value</span></span>

<span data-ttu-id="ac9ab-114">Se il messaggio ha esito positivo, restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="ac9ab-114">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="ac9ab-115">In caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="ac9ab-115">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac9ab-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="ac9ab-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ac9ab-117">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="ac9ab-117">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="ac9ab-118">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ac9ab-118">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ac9ab-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ac9ab-119">Requirements</span></span>



| <span data-ttu-id="ac9ab-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac9ab-120">Requirement</span></span> | <span data-ttu-id="ac9ab-121">Valore</span><span class="sxs-lookup"><span data-stu-id="ac9ab-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ac9ab-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac9ab-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ac9ab-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ac9ab-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ac9ab-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac9ab-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ac9ab-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ac9ab-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ac9ab-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ac9ab-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac9ab-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac9ab-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






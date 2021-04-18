---
title: Messaggio BCM_GETIDEALSIZE (COMmctrl. h)
description: Ottiene le dimensioni del pulsante che meglio si adatta al testo e all'immagine, se è presente un elenco di immagini. È possibile inviare questo messaggio in modo esplicito o usare il pulsante \_ GetIdealSize macro.
ms.assetid: c1bc2043-bf1a-4129-a005-f04048c4c1db
keywords:
- Controlli di Windows Message BCM_GETIDEALSIZE
topic_type:
- apiref
api_name:
- BCM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 446f4acba39b8b9722ef1a01a223f671b56ae845
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301588"
---
# <a name="bcm_getidealsize-message"></a><span data-ttu-id="6f78d-105">\_Messaggio GETIDEALSIZE BCM</span><span class="sxs-lookup"><span data-stu-id="6f78d-105">BCM\_GETIDEALSIZE message</span></span>

<span data-ttu-id="6f78d-106">Ottiene le dimensioni del pulsante che meglio si adatta al testo e all'immagine, se è presente un elenco di immagini.</span><span class="sxs-lookup"><span data-stu-id="6f78d-106">Gets the size of the button that best fits its text and image, if an image list is present.</span></span> <span data-ttu-id="6f78d-107">È possibile inviare questo messaggio in modo esplicito o usare il [**pulsante \_ GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-button_getidealsize) macro.</span><span class="sxs-lookup"><span data-stu-id="6f78d-107">You can send this message explicitly or use the [**Button\_GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-button_getidealsize) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6f78d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6f78d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f78d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6f78d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6f78d-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="6f78d-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="6f78d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6f78d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6f78d-112">Puntatore a una struttura di [**dimensioni**](/previous-versions//dd145106(v=vs.85)) che riceve la dimensione desiderata del pulsante, incluso il testo e l'elenco delle immagini, se presente.</span><span class="sxs-lookup"><span data-stu-id="6f78d-112">A pointer to a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure that receives the desired size of the button, including text and image list, if present.</span></span> <span data-ttu-id="6f78d-113">L'applicazione chiamante è responsabile dell'allocazione di questa struttura.</span><span class="sxs-lookup"><span data-stu-id="6f78d-113">The calling application is responsible for allocating this structure.</span></span> <span data-ttu-id="6f78d-114">Impostare i membri **CX** e **CY** su zero per avere l'altezza e la larghezza ideali restituite nella struttura delle **dimensioni** .</span><span class="sxs-lookup"><span data-stu-id="6f78d-114">Set the **cx** and **cy** members to zero to have the ideal height and width returned in the **SIZE** structure.</span></span> <span data-ttu-id="6f78d-115">Per specificare la larghezza di un pulsante, impostare il membro **CX** sulla larghezza desiderata per il pulsante.</span><span class="sxs-lookup"><span data-stu-id="6f78d-115">To specify a button width, set the **cx** member to the desired button width.</span></span> <span data-ttu-id="6f78d-116">Il sistema calcolerà l'altezza ideale per questa larghezza e la restituirà nel membro **CY** .</span><span class="sxs-lookup"><span data-stu-id="6f78d-116">The system will calculate the ideal height for this width and return it in the **cy** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f78d-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6f78d-117">Return value</span></span>

<span data-ttu-id="6f78d-118">Se il messaggio ha esito positivo, restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="6f78d-118">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="6f78d-119">In caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="6f78d-119">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f78d-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="6f78d-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6f78d-121">Se non si desidera la larghezza del pulsante speciale, è necessario impostare entrambi i membri della [**dimensione**](/previous-versions//dd145106(v=vs.85)) su zero per calcolare e restituire l'altezza e la larghezza ideali.</span><span class="sxs-lookup"><span data-stu-id="6f78d-121">If no special button width is desired, then you must set both members of [**SIZE**](/previous-versions//dd145106(v=vs.85)) to zero to calculate and return the ideal height and width.</span></span> <span data-ttu-id="6f78d-122">Se il valore del membro **CX** è maggiore di zero, questo valore viene considerato la larghezza desiderata del pulsante e l'altezza ideale per questa larghezza viene calcolata e restituita nel membro **CY** .</span><span class="sxs-lookup"><span data-stu-id="6f78d-122">If the value of the **cx** member is greater than zero, then this value is considered the desired button width, and the ideal height for this width is calculated and returned in the **cy** member.</span></span>

 

<span data-ttu-id="6f78d-123">Questo messaggio è più applicabile ai pulsanti.</span><span class="sxs-lookup"><span data-stu-id="6f78d-123">This message is most applicable to PushButtons.</span></span> <span data-ttu-id="6f78d-124">Quando viene inviato a un pulsante, il messaggio recupera il rettangolo di delimitazione necessario per visualizzare il testo del pulsante.</span><span class="sxs-lookup"><span data-stu-id="6f78d-124">When sent to a PushButton, the message retrieves the bounding rectangle required to display the button's text.</span></span> <span data-ttu-id="6f78d-125">Inoltre, se il pulsante ha un elenco di immagini, anche il rettangolo di delimitazione viene ridimensionato in modo da includere l'immagine del pulsante.</span><span class="sxs-lookup"><span data-stu-id="6f78d-125">Additionally, if the PushButton has an image list, the bounding rectangle is also sized to include the button's image.</span></span>

<span data-ttu-id="6f78d-126">Quando viene inviato a un pulsante di qualsiasi altro tipo, vengono recuperate le dimensioni del rettangolo della finestra del controllo.</span><span class="sxs-lookup"><span data-stu-id="6f78d-126">When sent to a button of any other type, the size of the control's window rectangle is retrieved.</span></span>

> [!Note]  
> <span data-ttu-id="6f78d-127">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="6f78d-127">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="6f78d-128">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6f78d-128">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6f78d-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6f78d-129">Requirements</span></span>



| <span data-ttu-id="6f78d-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f78d-130">Requirement</span></span> | <span data-ttu-id="6f78d-131">Valore</span><span class="sxs-lookup"><span data-stu-id="6f78d-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6f78d-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f78d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6f78d-133">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6f78d-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6f78d-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f78d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6f78d-135">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6f78d-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6f78d-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6f78d-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f78d-137"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f78d-137"><dt>Commctrl.h</dt></span></span> </dl> |



 


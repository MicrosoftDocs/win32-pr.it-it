---
title: Messaggio BCM_GETTEXTMARGIN (COMmctrl. h)
description: Ottiene i margini utilizzati per creare il testo in un controllo Button. È possibile inviare questo messaggio in modo esplicito o usare il pulsante \_ GetTextMargin macro.
ms.assetid: 6c141752-e636-41c4-9d05-df8b320ff59f
keywords:
- Controlli di Windows Message BCM_GETTEXTMARGIN
topic_type:
- apiref
api_name:
- BCM_GETTEXTMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6a7d809207c21c74a36c796a9035ed0e3772481
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964121"
---
# <a name="bcm_gettextmargin-message"></a><span data-ttu-id="45180-105">\_Messaggio GETTEXTMARGIN BCM</span><span class="sxs-lookup"><span data-stu-id="45180-105">BCM\_GETTEXTMARGIN message</span></span>

<span data-ttu-id="45180-106">Ottiene i margini utilizzati per creare il testo in un controllo Button.</span><span class="sxs-lookup"><span data-stu-id="45180-106">Gets the margins used to draw text in a button control.</span></span> <span data-ttu-id="45180-107">È possibile inviare questo messaggio in modo esplicito o usare il [**pulsante \_ GetTextMargin**](/windows/desktop/api/Commctrl/nf-commctrl-button_gettextmargin) macro.</span><span class="sxs-lookup"><span data-stu-id="45180-107">You can send this message explicitly or use the [**Button\_GetTextMargin**](/windows/desktop/api/Commctrl/nf-commctrl-button_gettextmargin) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="45180-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="45180-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45180-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="45180-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="45180-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="45180-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="45180-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="45180-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="45180-112">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che contiene i margini da utilizzare per il disegno del testo.</span><span class="sxs-lookup"><span data-stu-id="45180-112">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the margins to use for drawing text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45180-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="45180-113">Return value</span></span>

<span data-ttu-id="45180-114">Se il messaggio ha esito positivo, restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="45180-114">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="45180-115">In caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="45180-115">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="45180-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="45180-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="45180-117">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="45180-117">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="45180-118">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="45180-118">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="45180-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="45180-119">Requirements</span></span>



| <span data-ttu-id="45180-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="45180-120">Requirement</span></span> | <span data-ttu-id="45180-121">Valore</span><span class="sxs-lookup"><span data-stu-id="45180-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="45180-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="45180-122">Minimum supported client</span></span><br/> | <span data-ttu-id="45180-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="45180-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="45180-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="45180-124">Minimum supported server</span></span><br/> | <span data-ttu-id="45180-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="45180-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="45180-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="45180-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="45180-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="45180-127"><dt>Commctrl.h</dt></span></span> </dl> |



 


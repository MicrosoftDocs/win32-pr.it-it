---
title: Messaggio CCM_DPISCALE (COMmctrl. h)
description: Consente la scalabilità di punti per pollice (dpi) automatica in Tree-View controlli, controlli List-View, controlli ComboBoxEx, controlli Header, pulsanti, controlli della barra degli strumenti, controlli di animazione ed elenchi di immagini.
ms.assetid: 3c751f10-992c-41f8-8f0b-3dc58f0591e4
keywords:
- Controlli di Windows Message CCM_DPISCALE
topic_type:
- apiref
api_name:
- CCM_DPISCALE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ef978f486f370adf9872d28e1accbacc37a6de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120330"
---
# <a name="ccm_dpiscale-message"></a><span data-ttu-id="d0b04-104">\_Messaggio DPISCALE CCM</span><span class="sxs-lookup"><span data-stu-id="d0b04-104">CCM\_DPISCALE message</span></span>

<span data-ttu-id="d0b04-105">Consente il ridimensionamento DPI (punti per pollice) automatico per i controlli di [visualizzazione albero](tree-view-controls.md), i [controlli visualizzazione elenco](list-view-control-reference.md), i controlli [ComboBoxEx](comboboxex-controls.md), i [controlli intestazione](header-controls.md), i [pulsanti](buttons.md), i controlli della [barra degli strumenti](toolbar-controls-overview.md), i [controlli di animazione](animation-control-overview.md)e gli [elenchi di immagini](image-lists.md).</span><span class="sxs-lookup"><span data-stu-id="d0b04-105">Enables automatic high dots per inch (dpi) scaling in [Tree-View controls](tree-view-controls.md), [List-View controls](list-view-control-reference.md), [ComboBoxEx controls](comboboxex-controls.md), [Header controls](header-controls.md), [Buttons](buttons.md), [Toolbar controls](toolbar-controls-overview.md), [Animation controls](animation-control-overview.md), and [Image Lists](image-lists.md).</span></span>

## <a name="parameters"></a><span data-ttu-id="d0b04-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d0b04-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0b04-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d0b04-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d0b04-108">Impostare su **true**.</span><span class="sxs-lookup"><span data-stu-id="d0b04-108">Set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="d0b04-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d0b04-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d0b04-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d0b04-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0b04-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d0b04-111">Return value</span></span>

<span data-ttu-id="d0b04-112">Il valore restituito non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="d0b04-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0b04-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="d0b04-113">Remarks</span></span>

<span data-ttu-id="d0b04-114">L'avvio veloce e la [barra delle applicazioni](/windows/desktop/shell/taskbar) non devono specificare una scala dpi, perché le immagini sono già ridimensionate.</span><span class="sxs-lookup"><span data-stu-id="d0b04-114">Quick Launch and [Taskbar](/windows/desktop/shell/taskbar) should not specify a dpi scaling, because the images are already scaled.</span></span>

<span data-ttu-id="d0b04-115">Qualsiasi controllo che usa un elenco di immagini creato con la metrica SmallIcon non deve ridimensionare le proprie icone.</span><span class="sxs-lookup"><span data-stu-id="d0b04-115">Any control that uses an image list created with the SmallIcon metric should not scale its icons.</span></span>

> [!Note]  
> <span data-ttu-id="d0b04-116">Per usare questa API, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="d0b04-116">To use this API, you must provide a manifest that specifies Comclt32.dll version 6.0.</span></span> <span data-ttu-id="d0b04-117">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d0b04-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d0b04-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d0b04-118">Requirements</span></span>



| <span data-ttu-id="d0b04-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0b04-119">Requirement</span></span> | <span data-ttu-id="d0b04-120">Valore</span><span class="sxs-lookup"><span data-stu-id="d0b04-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d0b04-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d0b04-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d0b04-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d0b04-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d0b04-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d0b04-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d0b04-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d0b04-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d0b04-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d0b04-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0b04-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0b04-126"><dt>Commctrl.h</dt></span></span> </dl> |



 


---
title: Messaggio PSM_RECALCPAGESIZES (Prsht. h)
description: Ricalcola le dimensioni di pagina di una finestra delle proprietà standard o della procedura guidata dopo l'aggiunta o la rimozione di pagine. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro RecalcPageSizes di PropSheet.
ms.assetid: 42257ea3-0471-4c67-adcd-01cd2669a51e
keywords:
- Controlli di Windows Message PSM_RECALCPAGESIZES
topic_type:
- apiref
api_name:
- PSM_RECALCPAGESIZES
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ae2030f432e8c52ed6208be34d429b4579edb6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302198"
---
# <a name="psm_recalcpagesizes-message"></a><span data-ttu-id="56f94-105">\_Messaggio RECALCPAGESIZES di PSM</span><span class="sxs-lookup"><span data-stu-id="56f94-105">PSM\_RECALCPAGESIZES message</span></span>

<span data-ttu-id="56f94-106">Ricalcola le dimensioni di pagina di una finestra delle proprietà standard o della procedura guidata dopo l'aggiunta o la rimozione di pagine.</span><span class="sxs-lookup"><span data-stu-id="56f94-106">Recalculates the page size of a standard or wizard property sheet after pages have been added or removed.</span></span> <span data-ttu-id="56f94-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ RecalcPageSizes di PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_recalcpagesizes) .</span><span class="sxs-lookup"><span data-stu-id="56f94-107">You can send this message explicitly or use the [**PropSheet\_RecalcPageSizes**](/windows/desktop/api/Prsht/nf-prsht-propsheet_recalcpagesizes) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="56f94-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="56f94-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56f94-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="56f94-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56f94-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="56f94-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="56f94-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="56f94-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56f94-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="56f94-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56f94-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="56f94-113">Return value</span></span>

<span data-ttu-id="56f94-114">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="56f94-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="56f94-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="56f94-115">Remarks</span></span>

<span data-ttu-id="56f94-116">Quando viene creata, una finestra delle proprietà viene ridimensionata per adattarsi alla raccolta iniziale di pagine.</span><span class="sxs-lookup"><span data-stu-id="56f94-116">When a property sheet is created, it is sized to fit its initial collection of pages.</span></span> <span data-ttu-id="56f94-117">Per mantenere la compatibilità con le versioni precedenti dei controlli comuni, le finestre delle proprietà e le procedure guidate non si ridimensionano automaticamente quando le pagine vengono aggiunte o rimosse.</span><span class="sxs-lookup"><span data-stu-id="56f94-117">In order to maintain compatibility with previous versions of the common controls, property sheets and wizards do not automatically resize themselves when pages are subsequently added or removed.</span></span> <span data-ttu-id="56f94-118">Con i controlli comuni [versione 5,80](common-control-versions.md), le applicazioni devono inviare un messaggio **PSM \_ RECALCPAGESIZES** dopo l'aggiunta o la rimozione di pagine con [**PSM \_ ADDPAGE**](psm-addpage.md), [**PSM \_ INSERTPAGE**](psm-insertpage.md), [**PSM \_ REMOVEPAGE**](psm-removepage.md)o le macro equivalenti.</span><span class="sxs-lookup"><span data-stu-id="56f94-118">With common controls [version 5.80](common-control-versions.md), applications should send a **PSM\_RECALCPAGESIZES** message after adding or removing pages with [**PSM\_ADDPAGE**](psm-addpage.md), [**PSM\_INSERTPAGE**](psm-insertpage.md), [**PSM\_REMOVEPAGE**](psm-removepage.md), or their equivalent macros.</span></span> <span data-ttu-id="56f94-119">Garantisce che la finestra delle proprietà sia dimensionata correttamente per la raccolta di pagine corrente.</span><span class="sxs-lookup"><span data-stu-id="56f94-119">It ensures that the property sheet is properly sized for its current collection of pages.</span></span> <span data-ttu-id="56f94-120">Se il messaggio non viene inviato, è possibile che alcune pagine della finestra delle proprietà vengano troncate o troppo grandi.</span><span class="sxs-lookup"><span data-stu-id="56f94-120">If this message is not sent, some property sheet pages may be truncated or too large.</span></span>

> [!Note]  
> <span data-ttu-id="56f94-121">Questo messaggio non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="56f94-121">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="56f94-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56f94-122">Requirements</span></span>



| <span data-ttu-id="56f94-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="56f94-123">Requirement</span></span> | <span data-ttu-id="56f94-124">Valore</span><span class="sxs-lookup"><span data-stu-id="56f94-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="56f94-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56f94-125">Minimum supported client</span></span><br/> | <span data-ttu-id="56f94-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="56f94-126">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="56f94-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56f94-127">Minimum supported server</span></span><br/> | <span data-ttu-id="56f94-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="56f94-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="56f94-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="56f94-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="56f94-130"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="56f94-130"><dt>Prsht.h</dt></span></span> </dl> |



 

 






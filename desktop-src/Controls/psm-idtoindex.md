---
title: Messaggio PSM_IDTOINDEX (Prsht. h)
description: Accetta l'ID di una pagina della finestra delle proprietà e restituisce il relativo indice in base zero. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro IdToIndex di PropSheet.
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_idtoindex.htm
keywords:
- Controlli di Windows Message PSM_IDTOINDEX
topic_type:
- apiref
api_name:
- PSM_IDTOINDEX
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f098c37ba30e33685abedf9dccd3ffc7c303acb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120834"
---
# <a name="psm_idtoindex-message"></a><span data-ttu-id="ecd8f-105">\_Messaggio IDTOINDEX di PSM</span><span class="sxs-lookup"><span data-stu-id="ecd8f-105">PSM\_IDTOINDEX message</span></span>

<span data-ttu-id="ecd8f-106">Accetta l'ID di una pagina della finestra delle proprietà e restituisce il relativo indice in base zero.</span><span class="sxs-lookup"><span data-stu-id="ecd8f-106">Takes the resource ID of a property sheet page and returns its zero-based index.</span></span> <span data-ttu-id="ecd8f-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ IdToIndex di PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_idtoindex) .</span><span class="sxs-lookup"><span data-stu-id="ecd8f-107">You can send this message explicitly or use the [**PropSheet\_IdToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_idtoindex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ecd8f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ecd8f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecd8f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ecd8f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ecd8f-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="ecd8f-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ecd8f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ecd8f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ecd8f-112">ID risorsa della pagina.</span><span class="sxs-lookup"><span data-stu-id="ecd8f-112">Resource ID of the page.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecd8f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ecd8f-113">Return value</span></span>

<span data-ttu-id="ecd8f-114">Restituisce l'indice in base zero della pagina della finestra delle proprietà specificato da *lParam* se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="ecd8f-114">Returns the zero-based index of the property sheet page specified by *lParam* if successful.</span></span> <span data-ttu-id="ecd8f-115">In caso contrario, restituisce -1.</span><span class="sxs-lookup"><span data-stu-id="ecd8f-115">Otherwise, it returns -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecd8f-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ecd8f-116">Requirements</span></span>



| <span data-ttu-id="ecd8f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecd8f-117">Requirement</span></span> | <span data-ttu-id="ecd8f-118">Valore</span><span class="sxs-lookup"><span data-stu-id="ecd8f-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ecd8f-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ecd8f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ecd8f-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ecd8f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ecd8f-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ecd8f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ecd8f-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ecd8f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ecd8f-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ecd8f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecd8f-124"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecd8f-124"><dt>Prsht.h</dt></span></span> </dl> |



 

 






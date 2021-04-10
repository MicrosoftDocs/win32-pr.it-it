---
title: Messaggio PSM_HWNDTOINDEX (Prsht. h)
description: Accetta l'handle della finestra della pagina delle proprietà e restituisce il relativo indice in base zero. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro HwndToIndex di PropSheet.
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_hwndtoindex.htm
keywords:
- Controlli di Windows Message PSM_HWNDTOINDEX
topic_type:
- apiref
api_name:
- PSM_HWNDTOINDEX
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6632d331a6f271e339663a23210d0b399fb669b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120115"
---
# <a name="psm_hwndtoindex-message"></a><span data-ttu-id="45f5b-105">\_Messaggio HWNDTOINDEX di PSM</span><span class="sxs-lookup"><span data-stu-id="45f5b-105">PSM\_HWNDTOINDEX message</span></span>

<span data-ttu-id="45f5b-106">Accetta l'handle della finestra della pagina delle proprietà e restituisce il relativo indice in base zero.</span><span class="sxs-lookup"><span data-stu-id="45f5b-106">Takes the window handle of the property sheet page and returns its zero-based index.</span></span> <span data-ttu-id="45f5b-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ HwndToIndex di PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_hwndtoindex) .</span><span class="sxs-lookup"><span data-stu-id="45f5b-107">You can send this message explicitly or use the [**PropSheet\_HwndToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_hwndtoindex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="45f5b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="45f5b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45f5b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="45f5b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="45f5b-110">Handle per la finestra della pagina.</span><span class="sxs-lookup"><span data-stu-id="45f5b-110">Handle to the page's window.</span></span>

</dd> <dt>

<span data-ttu-id="45f5b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="45f5b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="45f5b-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="45f5b-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45f5b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="45f5b-113">Return value</span></span>

<span data-ttu-id="45f5b-114">Restituisce l'indice in base zero della pagina della finestra delle proprietà specificata da *wParam* se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="45f5b-114">Returns the zero-based index of the property sheet page specified by *wParam* if successful.</span></span> <span data-ttu-id="45f5b-115">In caso contrario, restituisce -1.</span><span class="sxs-lookup"><span data-stu-id="45f5b-115">Otherwise, it returns -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="45f5b-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="45f5b-116">Requirements</span></span>



| <span data-ttu-id="45f5b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="45f5b-117">Requirement</span></span> | <span data-ttu-id="45f5b-118">Valore</span><span class="sxs-lookup"><span data-stu-id="45f5b-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="45f5b-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="45f5b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="45f5b-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="45f5b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="45f5b-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="45f5b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="45f5b-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="45f5b-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="45f5b-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="45f5b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="45f5b-124"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="45f5b-124"><dt>Prsht.h</dt></span></span> </dl> |



 

 






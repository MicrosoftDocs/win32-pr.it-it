---
title: Messaggio PSM_INDEXTOHWND (Prsht. h)
description: Accetta l'indice di una pagina della finestra delle proprietà e restituisce l'handle della finestra. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro IndexToHwnd di PropSheet.
ms.assetid: 93b46b4c-47f9-4ce8-8797-f3d4bd5248e9
keywords:
- Controlli di Windows Message PSM_INDEXTOHWND
topic_type:
- apiref
api_name:
- PSM_INDEXTOHWND
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 788b1dd0e7312f301051d9a57fcdec43f3f2f72a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120826"
---
# <a name="psm_indextohwnd-message"></a><span data-ttu-id="0f01e-105">\_Messaggio INDEXTOHWND di PSM</span><span class="sxs-lookup"><span data-stu-id="0f01e-105">PSM\_INDEXTOHWND message</span></span>

<span data-ttu-id="0f01e-106">Accetta l'indice di una pagina della finestra delle proprietà e restituisce l'handle della finestra.</span><span class="sxs-lookup"><span data-stu-id="0f01e-106">Takes the index of a property sheet page and returns its window handle.</span></span> <span data-ttu-id="0f01e-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ IndexToHwnd di PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextohwnd) .</span><span class="sxs-lookup"><span data-stu-id="0f01e-107">You can send this message explicitly or use the [**PropSheet\_IndexToHwnd**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextohwnd) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0f01e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0f01e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f01e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0f01e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0f01e-110">Indice in base zero della pagina.</span><span class="sxs-lookup"><span data-stu-id="0f01e-110">Zero-based index of the page.</span></span>

</dd> <dt>

<span data-ttu-id="0f01e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0f01e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0f01e-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="0f01e-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f01e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0f01e-113">Return value</span></span>

<span data-ttu-id="0f01e-114">Restituisce l'handle per la finestra della pagina della finestra delle proprietà specificata da *wParam* in caso di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="0f01e-114">Returns the handle to the window of the property sheet page specified by *wParam* if successful.</span></span> <span data-ttu-id="0f01e-115">In caso contrario, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="0f01e-115">Otherwise, it returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f01e-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f01e-116">Requirements</span></span>



| <span data-ttu-id="0f01e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f01e-117">Requirement</span></span> | <span data-ttu-id="0f01e-118">Valore</span><span class="sxs-lookup"><span data-stu-id="0f01e-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0f01e-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f01e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0f01e-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0f01e-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0f01e-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f01e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0f01e-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0f01e-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0f01e-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0f01e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f01e-124"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f01e-124"><dt>Prsht.h</dt></span></span> </dl> |



 

 






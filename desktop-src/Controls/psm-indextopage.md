---
title: Messaggio PSM_INDEXTOPAGE (Prsht. h)
description: Accetta l'indice di una pagina della finestra delle proprietà e restituisce il relativo handle HPROPSHEETPAGE. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro IndexToPage di PropSheet.
ms.assetid: b14b35ad-bae0-4461-a90f-e2bc5e2ccfc2
keywords:
- Controlli di Windows Message PSM_INDEXTOPAGE
topic_type:
- apiref
api_name:
- PSM_INDEXTOPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38f7a5658dbd92f4208e084f1df47a4dc3582156
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478239"
---
# <a name="psm_indextopage-message"></a><span data-ttu-id="906b0-105">\_Messaggio INDEXTOPAGE di PSM</span><span class="sxs-lookup"><span data-stu-id="906b0-105">PSM\_INDEXTOPAGE message</span></span>

<span data-ttu-id="906b0-106">Accetta l'indice di una pagina della finestra delle proprietà e restituisce il relativo handle HPROPSHEETPAGE.</span><span class="sxs-lookup"><span data-stu-id="906b0-106">Takes the index of a property sheet page and returns its HPROPSHEETPAGE handle.</span></span> <span data-ttu-id="906b0-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ IndexToPage di PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextopage) .</span><span class="sxs-lookup"><span data-stu-id="906b0-107">You can send this message explicitly or use the [**PropSheet\_IndexToPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextopage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="906b0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="906b0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="906b0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="906b0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="906b0-110">Indice in base zero della pagina.</span><span class="sxs-lookup"><span data-stu-id="906b0-110">Zero-based index of the page.</span></span>

</dd> <dt>

<span data-ttu-id="906b0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="906b0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="906b0-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="906b0-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="906b0-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="906b0-113">Return value</span></span>

<span data-ttu-id="906b0-114">Restituisce l'handle HPROPSHEETPAGE della pagina della finestra delle proprietà specificata da *wParam* se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="906b0-114">Returns the HPROPSHEETPAGE handle of the property sheet page specified by *wParam* if successful.</span></span> <span data-ttu-id="906b0-115">In caso contrario, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="906b0-115">Otherwise, it returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="906b0-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="906b0-116">Requirements</span></span>



| <span data-ttu-id="906b0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="906b0-117">Requirement</span></span> | <span data-ttu-id="906b0-118">Valore</span><span class="sxs-lookup"><span data-stu-id="906b0-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="906b0-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="906b0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="906b0-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="906b0-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="906b0-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="906b0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="906b0-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="906b0-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="906b0-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="906b0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="906b0-124"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="906b0-124"><dt>Prsht.h</dt></span></span> </dl> |



 

 






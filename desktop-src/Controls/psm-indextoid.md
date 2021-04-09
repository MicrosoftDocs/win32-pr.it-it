---
title: Messaggio PSM_INDEXTOID (Prsht. h)
description: Accetta l'indice di una pagina della finestra delle proprietà e restituisce il relativo ID di risorsa. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro IndexToId di PropSheet.
ms.assetid: c153675a-360f-4916-aa0b-500636dd9022
keywords:
- Controlli di Windows Message PSM_INDEXTOID
topic_type:
- apiref
api_name:
- PSM_INDEXTOID
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 643861ecb6dc11d949483defc282d6d65648bdca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048517"
---
# <a name="psm_indextoid-message"></a><span data-ttu-id="53444-105">\_Messaggio INDEXTOID di PSM</span><span class="sxs-lookup"><span data-stu-id="53444-105">PSM\_INDEXTOID message</span></span>

<span data-ttu-id="53444-106">Accetta l'indice di una pagina della finestra delle proprietà e restituisce il relativo ID di risorsa.</span><span class="sxs-lookup"><span data-stu-id="53444-106">Takes the index of a property sheet page and returns its resource ID.</span></span> <span data-ttu-id="53444-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ IndexToId di PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextoid) .</span><span class="sxs-lookup"><span data-stu-id="53444-107">You can send this message explicitly or use the [**PropSheet\_IndexToId**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextoid) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="53444-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="53444-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53444-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="53444-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53444-110">Indice in base zero della pagina.</span><span class="sxs-lookup"><span data-stu-id="53444-110">Zero-based index of the page.</span></span>

</dd> <dt>

<span data-ttu-id="53444-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="53444-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53444-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="53444-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53444-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="53444-113">Return value</span></span>

<span data-ttu-id="53444-114">Restituisce l'ID risorsa della pagina della finestra delle proprietà specificata da *wParam* se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="53444-114">Returns the resource ID of the property sheet page specified by *wParam* if successful.</span></span> <span data-ttu-id="53444-115">In caso contrario, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="53444-115">Otherwise, it returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="53444-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53444-116">Requirements</span></span>



| <span data-ttu-id="53444-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="53444-117">Requirement</span></span> | <span data-ttu-id="53444-118">Valore</span><span class="sxs-lookup"><span data-stu-id="53444-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="53444-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53444-119">Minimum supported client</span></span><br/> | <span data-ttu-id="53444-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="53444-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="53444-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53444-121">Minimum supported server</span></span><br/> | <span data-ttu-id="53444-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="53444-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="53444-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="53444-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="53444-124"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="53444-124"><dt>Prsht.h</dt></span></span> </dl> |



 

 






---
title: Messaggio PSM_PAGETOINDEX (Prsht. h)
description: Accetta l'handle HPROPSHEETPAGE della pagina della finestra delle proprietà e restituisce il relativo indice in base zero. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro PageToIndex di PropSheet.
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_pagetoindex.htm
keywords:
- Controlli di Windows Message PSM_PAGETOINDEX
topic_type:
- apiref
api_name:
- PSM_PAGETOINDEX
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13e3cb6688ab918da0dfae8affed36903e6dcea7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301837"
---
# <a name="psm_pagetoindex-message"></a><span data-ttu-id="81287-105">\_Messaggio PAGETOINDEX di PSM</span><span class="sxs-lookup"><span data-stu-id="81287-105">PSM\_PAGETOINDEX message</span></span>

<span data-ttu-id="81287-106">Accetta l'handle HPROPSHEETPAGE della pagina della finestra delle proprietà e restituisce il relativo indice in base zero.</span><span class="sxs-lookup"><span data-stu-id="81287-106">Takes the HPROPSHEETPAGE handle of the property sheet page and returns its zero-based index.</span></span> <span data-ttu-id="81287-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ PageToIndex di PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pagetoindex) .</span><span class="sxs-lookup"><span data-stu-id="81287-107">You can send this message explicitly or use the [**PropSheet\_PageToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pagetoindex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="81287-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="81287-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81287-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="81287-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="81287-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="81287-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="81287-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="81287-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="81287-112">Handle HPROPSHEETPAGE per la pagina della finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="81287-112">HPROPSHEETPAGE handle to the property sheet page.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81287-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="81287-113">Return value</span></span>

<span data-ttu-id="81287-114">Restituisce l'indice in base zero della pagina della finestra delle proprietà specificato da *lParam* se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="81287-114">Returns the zero-based index of the property sheet page specified by *lParam* if successful.</span></span> <span data-ttu-id="81287-115">In caso contrario, restituisce -1.</span><span class="sxs-lookup"><span data-stu-id="81287-115">Otherwise, it returns -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="81287-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="81287-116">Requirements</span></span>



| <span data-ttu-id="81287-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="81287-117">Requirement</span></span> | <span data-ttu-id="81287-118">Valore</span><span class="sxs-lookup"><span data-stu-id="81287-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="81287-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81287-119">Minimum supported client</span></span><br/> | <span data-ttu-id="81287-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="81287-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="81287-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81287-121">Minimum supported server</span></span><br/> | <span data-ttu-id="81287-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="81287-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="81287-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="81287-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="81287-124"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="81287-124"><dt>Prsht.h</dt></span></span> </dl> |



 

 






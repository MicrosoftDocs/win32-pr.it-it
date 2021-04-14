---
title: Messaggio PSM_QUERYSIBLINGS (Prsht. h)
description: Inviato a una finestra delle proprietà che quindi inoltra il messaggio a ognuna delle relative pagine. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro PropSheet QuerySiblings.
ms.assetid: 96f48847-b7b8-4d6f-8bde-ada915b7c962
keywords:
- Controlli di Windows Message PSM_QUERYSIBLINGS
topic_type:
- apiref
api_name:
- PSM_QUERYSIBLINGS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea5943fefa906475e34d1cc7acc7f8a86cd99252
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517967"
---
# <a name="psm_querysiblings-message"></a><span data-ttu-id="a928c-105">\_Messaggio QUERYSIBLINGS di PSM</span><span class="sxs-lookup"><span data-stu-id="a928c-105">PSM\_QUERYSIBLINGS message</span></span>

<span data-ttu-id="a928c-106">Inviato a una finestra delle proprietà che quindi inoltra il messaggio a ognuna delle relative pagine.</span><span class="sxs-lookup"><span data-stu-id="a928c-106">Sent to a property sheet, which then forwards the message to each of its pages.</span></span> <span data-ttu-id="a928c-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**PropSheet \_ QuerySiblings**](/windows/desktop/api/Prsht/nf-prsht-propsheet_querysiblings) .</span><span class="sxs-lookup"><span data-stu-id="a928c-107">You can send this message explicitly or by using the [**PropSheet\_QuerySiblings**](/windows/desktop/api/Prsht/nf-prsht-propsheet_querysiblings) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a928c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a928c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a928c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a928c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a928c-110">Primo parametro definito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a928c-110">First application-defined parameter.</span></span>

</dd> <dt>

<span data-ttu-id="a928c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a928c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a928c-112">Secondo parametro definito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a928c-112">Second application-defined parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a928c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a928c-113">Return value</span></span>

<span data-ttu-id="a928c-114">Restituisce il valore diverso da zero da una pagina nella finestra delle proprietà oppure zero se nessuna pagina restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="a928c-114">Returns the nonzero value from a page in the property sheet, or zero if no page returns a nonzero value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a928c-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="a928c-115">Remarks</span></span>

<span data-ttu-id="a928c-116">Se una pagina restituisce un valore diverso da zero, la finestra delle proprietà non invia il messaggio alle pagine successive.</span><span class="sxs-lookup"><span data-stu-id="a928c-116">If a page returns a nonzero value, the property sheet does not send the message to subsequent pages.</span></span>

## <a name="requirements"></a><span data-ttu-id="a928c-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a928c-117">Requirements</span></span>



| <span data-ttu-id="a928c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a928c-118">Requirement</span></span> | <span data-ttu-id="a928c-119">Valore</span><span class="sxs-lookup"><span data-stu-id="a928c-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a928c-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a928c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a928c-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a928c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a928c-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a928c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a928c-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a928c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a928c-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a928c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a928c-125"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="a928c-125"><dt>Prsht.h</dt></span></span> </dl> |



 

 






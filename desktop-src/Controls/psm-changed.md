---
title: Messaggio PSM_CHANGED (Prsht. h)
description: Informa una finestra delle proprietà che le informazioni in una pagina sono state modificate. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro PropSheet modificata.
ms.assetid: b092969f-31dc-4e3c-9100-d15f1bdd5aa5
keywords:
- Controlli di Windows Message PSM_CHANGED
topic_type:
- apiref
api_name:
- PSM_CHANGED
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57f931db5e25f816f7ea164ca5871a4e3e7757a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302201"
---
# <a name="psm_changed-message"></a><span data-ttu-id="ce9d5-105">PSM- \_ messaggio modificato</span><span class="sxs-lookup"><span data-stu-id="ce9d5-105">PSM\_CHANGED message</span></span>

<span data-ttu-id="ce9d5-106">Informa una finestra delle proprietà che le informazioni in una pagina sono state modificate.</span><span class="sxs-lookup"><span data-stu-id="ce9d5-106">Informs a property sheet that information in a page has changed.</span></span> <span data-ttu-id="ce9d5-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**PropSheet \_ modificata**](/windows/desktop/api/Prsht/nf-prsht-propsheet_changed) .</span><span class="sxs-lookup"><span data-stu-id="ce9d5-107">You can send this message explicitly or by using the [**PropSheet\_Changed**](/windows/desktop/api/Prsht/nf-prsht-propsheet_changed) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ce9d5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ce9d5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce9d5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ce9d5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ce9d5-110">Handle per la pagina che è stata modificata.</span><span class="sxs-lookup"><span data-stu-id="ce9d5-110">Handle to the page that has changed.</span></span>

</dd> <dt>

<span data-ttu-id="ce9d5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ce9d5-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ce9d5-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="ce9d5-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce9d5-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ce9d5-113">Return value</span></span>

<span data-ttu-id="ce9d5-114">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="ce9d5-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce9d5-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="ce9d5-115">Remarks</span></span>

<span data-ttu-id="ce9d5-116">Nella finestra delle proprietà viene abilitato il pulsante **applica** .</span><span class="sxs-lookup"><span data-stu-id="ce9d5-116">The property sheet will enable the **Apply** button.</span></span>

> [!Note]  
> <span data-ttu-id="ce9d5-117">Questo messaggio non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="ce9d5-117">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ce9d5-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce9d5-118">Requirements</span></span>



| <span data-ttu-id="ce9d5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce9d5-119">Requirement</span></span> | <span data-ttu-id="ce9d5-120">Valore</span><span class="sxs-lookup"><span data-stu-id="ce9d5-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ce9d5-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce9d5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ce9d5-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ce9d5-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ce9d5-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce9d5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ce9d5-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ce9d5-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ce9d5-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ce9d5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce9d5-126"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce9d5-126"><dt>Prsht.h</dt></span></span> </dl> |



 

 






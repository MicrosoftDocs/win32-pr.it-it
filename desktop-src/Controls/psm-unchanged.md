---
title: Messaggio PSM_UNCHANGED (Prsht. h)
description: Informa una finestra delle proprietà che le informazioni in una pagina sono state ripristinate allo stato salvato in precedenza. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro PropSheet non modificata.
ms.assetid: 61c15dec-40d0-4720-a117-4eed765c8819
keywords:
- Controlli di Windows Message PSM_UNCHANGED
topic_type:
- apiref
api_name:
- PSM_UNCHANGED
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb1d6216f94afd610bb49710a3e84b4c21a673f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104225234"
---
# <a name="psm_unchanged-message"></a><span data-ttu-id="b9a8e-105">PSM \_ messaggio non modificato</span><span class="sxs-lookup"><span data-stu-id="b9a8e-105">PSM\_UNCHANGED message</span></span>

<span data-ttu-id="b9a8e-106">Informa una finestra delle proprietà che le informazioni in una pagina sono state ripristinate allo stato salvato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="b9a8e-106">Informs a property sheet that information in a page has reverted to the previously saved state.</span></span> <span data-ttu-id="b9a8e-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**PropSheet non \_ modificata**](/windows/desktop/api/Prsht/nf-prsht-propsheet_unchanged) .</span><span class="sxs-lookup"><span data-stu-id="b9a8e-107">You can send this message explicitly or by using the [**PropSheet\_UnChanged**](/windows/desktop/api/Prsht/nf-prsht-propsheet_unchanged) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b9a8e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b9a8e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9a8e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b9a8e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b9a8e-110">Handle per la pagina che ha ripristinato lo stato salvato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="b9a8e-110">Handle to the page that has reverted to the previously saved state.</span></span>

</dd> <dt>

<span data-ttu-id="b9a8e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b9a8e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b9a8e-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="b9a8e-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9a8e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b9a8e-113">Return value</span></span>

<span data-ttu-id="b9a8e-114">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="b9a8e-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9a8e-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="b9a8e-115">Remarks</span></span>

<span data-ttu-id="b9a8e-116">La finestra delle proprietà Disabilita il pulsante **applica** se nessuna altra pagina ha registrato modifiche con la finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="b9a8e-116">The property sheet disables the **Apply** button if no other pages have registered changes with the property sheet.</span></span>

> [!Note]  
> <span data-ttu-id="b9a8e-117">Questo messaggio non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="b9a8e-117">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b9a8e-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9a8e-118">Requirements</span></span>



| <span data-ttu-id="b9a8e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9a8e-119">Requirement</span></span> | <span data-ttu-id="b9a8e-120">Valore</span><span class="sxs-lookup"><span data-stu-id="b9a8e-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b9a8e-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9a8e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b9a8e-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b9a8e-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b9a8e-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9a8e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b9a8e-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b9a8e-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b9a8e-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b9a8e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9a8e-126"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9a8e-126"><dt>Prsht.h</dt></span></span> </dl> |



 

 






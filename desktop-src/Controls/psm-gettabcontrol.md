---
title: Messaggio PSM_GETTABCONTROL (Prsht. h)
description: Recupera l'handle per il controllo struttura a schede di una finestra delle proprietà. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro PropSheet GetTabControl.
ms.assetid: 5ddea541-c8e0-4357-b08e-3b5e64be377f
keywords:
- Controlli di Windows Message PSM_GETTABCONTROL
topic_type:
- apiref
api_name:
- PSM_GETTABCONTROL
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab296159cac4dbfb4ef894d90d31bcd74d6ca2e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518526"
---
# <a name="psm_gettabcontrol-message"></a><span data-ttu-id="354b5-105">\_Messaggio PSM GETtabcontrol</span><span class="sxs-lookup"><span data-stu-id="354b5-105">PSM\_GETTABCONTROL message</span></span>

<span data-ttu-id="354b5-106">Recupera l'handle per il controllo struttura a schede di una finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="354b5-106">Retrieves the handle to the tab control of a property sheet.</span></span> <span data-ttu-id="354b5-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**PropSheet \_ GetTabControl**](/windows/desktop/api/Prsht/nf-prsht-propsheet_gettabcontrol) .</span><span class="sxs-lookup"><span data-stu-id="354b5-107">You can send this message explicitly or by using the [**PropSheet\_GetTabControl**](/windows/desktop/api/Prsht/nf-prsht-propsheet_gettabcontrol) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="354b5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="354b5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="354b5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="354b5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="354b5-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="354b5-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="354b5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="354b5-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="354b5-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="354b5-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="354b5-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="354b5-113">Return value</span></span>

<span data-ttu-id="354b5-114">Restituisce l'handle per il controllo struttura a schede.</span><span class="sxs-lookup"><span data-stu-id="354b5-114">Returns the handle to the tab control.</span></span>

## <a name="remarks"></a><span data-ttu-id="354b5-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="354b5-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="354b5-116">Questo messaggio non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="354b5-116">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="354b5-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="354b5-117">Requirements</span></span>



| <span data-ttu-id="354b5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="354b5-118">Requirement</span></span> | <span data-ttu-id="354b5-119">Valore</span><span class="sxs-lookup"><span data-stu-id="354b5-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="354b5-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="354b5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="354b5-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="354b5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="354b5-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="354b5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="354b5-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="354b5-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="354b5-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="354b5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="354b5-125"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="354b5-125"><dt>Prsht.h</dt></span></span> </dl> |



 

 






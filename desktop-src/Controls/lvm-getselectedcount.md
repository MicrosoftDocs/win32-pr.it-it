---
title: Messaggio LVM_GETSELECTEDCOUNT (COMmctrl. h)
description: Determina il numero di elementi selezionati in un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetSelectedCount di ListView.
ms.assetid: 38916227-e6ca-4efa-9821-13f0fdb29834
keywords:
- Controlli di Windows Message LVM_GETSELECTEDCOUNT
topic_type:
- apiref
api_name:
- LVM_GETSELECTEDCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b23f0e8d1d87e2cc7dd60d32ac3dd4943611a36f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874321"
---
# <a name="lvm_getselectedcount-message"></a><span data-ttu-id="61aed-105">\_Messaggio GETSELECTEDCOUNT LVM</span><span class="sxs-lookup"><span data-stu-id="61aed-105">LVM\_GETSELECTEDCOUNT message</span></span>

<span data-ttu-id="61aed-106">Determina il numero di elementi selezionati in un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="61aed-106">Determines the number of selected items in a list-view control.</span></span> <span data-ttu-id="61aed-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetSelectedCount di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getselectedcount) .</span><span class="sxs-lookup"><span data-stu-id="61aed-107">You can send this message explicitly or by using the [**ListView\_GetSelectedCount**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getselectedcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="61aed-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="61aed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61aed-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="61aed-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="61aed-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="61aed-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="61aed-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="61aed-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="61aed-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="61aed-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61aed-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="61aed-113">Return value</span></span>

<span data-ttu-id="61aed-114">Restituisce il numero di elementi selezionati.</span><span class="sxs-lookup"><span data-stu-id="61aed-114">Returns the number of selected items.</span></span>

## <a name="requirements"></a><span data-ttu-id="61aed-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="61aed-115">Requirements</span></span>



| <span data-ttu-id="61aed-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="61aed-116">Requirement</span></span> | <span data-ttu-id="61aed-117">Valore</span><span class="sxs-lookup"><span data-stu-id="61aed-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="61aed-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="61aed-118">Minimum supported client</span></span><br/> | <span data-ttu-id="61aed-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="61aed-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="61aed-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="61aed-120">Minimum supported server</span></span><br/> | <span data-ttu-id="61aed-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="61aed-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="61aed-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="61aed-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="61aed-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="61aed-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






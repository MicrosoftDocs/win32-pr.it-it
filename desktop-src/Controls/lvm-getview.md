---
title: Messaggio LVM_GETVIEW (COMmctrl. h)
description: Recupera la visualizzazione corrente di un controllo visualizzazione elenco.
ms.assetid: dd63e726-3a7f-40e7-8d46-4680816c02a3
keywords:
- Controlli di Windows Message LVM_GETVIEW
topic_type:
- apiref
api_name:
- LVM_GETVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2da295fa5a5b335de60169ce06b777d9e355121
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120974"
---
# <a name="lvm_getview-message"></a><span data-ttu-id="edf39-104">\_Messaggio LVM GETview</span><span class="sxs-lookup"><span data-stu-id="edf39-104">LVM\_GETVIEW message</span></span>

<span data-ttu-id="edf39-105">Recupera la visualizzazione corrente di un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="edf39-105">Retrieves the current view of a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="edf39-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="edf39-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edf39-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="edf39-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="edf39-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="edf39-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="edf39-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="edf39-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="edf39-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="edf39-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edf39-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="edf39-111">Return value</span></span>

<span data-ttu-id="edf39-112">Restituisce un **valore DWORD** che specifica la visualizzazione corrente.</span><span class="sxs-lookup"><span data-stu-id="edf39-112">Returns a **DWORD** that specifies the current view.</span></span>

## <a name="remarks"></a><span data-ttu-id="edf39-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="edf39-113">Remarks</span></span>

<span data-ttu-id="edf39-114">Di seguito sono riportati i valori per le visualizzazioni.</span><span class="sxs-lookup"><span data-stu-id="edf39-114">Following are the values for views.</span></span>

-   <span data-ttu-id="edf39-115">\_dettagli vista \_ LV</span><span class="sxs-lookup"><span data-stu-id="edf39-115">LV\_VIEW\_DETAILS</span></span>
-   <span data-ttu-id="edf39-116">\_icona di visualizzazione LV \_</span><span class="sxs-lookup"><span data-stu-id="edf39-116">LV\_VIEW\_ICON</span></span>
-   <span data-ttu-id="edf39-117">\_elenco viste \_ LV</span><span class="sxs-lookup"><span data-stu-id="edf39-117">LV\_VIEW\_LIST</span></span>
-   <span data-ttu-id="edf39-118">\_SMALLICON vista \_ LV</span><span class="sxs-lookup"><span data-stu-id="edf39-118">LV\_VIEW\_SMALLICON</span></span>
-   <span data-ttu-id="edf39-119">\_riquadro Vista \_ LV</span><span class="sxs-lookup"><span data-stu-id="edf39-119">LV\_VIEW\_TILE</span></span>

> [!Note]  
> <span data-ttu-id="edf39-120">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="edf39-120">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="edf39-121">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="edf39-121">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="edf39-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="edf39-122">Requirements</span></span>



| <span data-ttu-id="edf39-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="edf39-123">Requirement</span></span> | <span data-ttu-id="edf39-124">Valore</span><span class="sxs-lookup"><span data-stu-id="edf39-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="edf39-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="edf39-125">Minimum supported client</span></span><br/> | <span data-ttu-id="edf39-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="edf39-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="edf39-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="edf39-127">Minimum supported server</span></span><br/> | <span data-ttu-id="edf39-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="edf39-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="edf39-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="edf39-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="edf39-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="edf39-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






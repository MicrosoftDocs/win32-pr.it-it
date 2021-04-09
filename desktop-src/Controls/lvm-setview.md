---
title: Messaggio LVM_SETVIEW (COMmctrl. h)
description: Imposta la visualizzazione di un controllo visualizzazione elenco.
ms.assetid: e6d3f16d-52ea-4863-a6c9-9a085d5f794a
keywords:
- Controlli di Windows Message LVM_SETVIEW
topic_type:
- apiref
api_name:
- LVM_SETVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a159710b3086bcba5298a5a88f9cab15f76e0d89
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120959"
---
# <a name="lvm_setview-message"></a><span data-ttu-id="c0279-104">Messaggio di visualizzazione a LVM \_</span><span class="sxs-lookup"><span data-stu-id="c0279-104">LVM\_SETVIEW message</span></span>

<span data-ttu-id="c0279-105">Imposta la visualizzazione di un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="c0279-105">Sets the view of a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c0279-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c0279-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0279-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c0279-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c0279-108">**DWORD** che specifica la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="c0279-108">**DWORD** that specifies the view.</span></span></dd> <dt>

<span data-ttu-id="c0279-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c0279-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c0279-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="c0279-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0279-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c0279-111">Return value</span></span>

<span data-ttu-id="c0279-112">Restituisce 1 se ha esito positivo oppure-1 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="c0279-112">Returns 1 if successful, or -1 otherwise.</span></span> <span data-ttu-id="c0279-113">Se, ad esempio, la vista non è valida, viene restituito-1.</span><span class="sxs-lookup"><span data-stu-id="c0279-113">For example, -1 is returned if the view is invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0279-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="c0279-114">Remarks</span></span>

<span data-ttu-id="c0279-115">Di seguito sono riportati i valori per le visualizzazioni.</span><span class="sxs-lookup"><span data-stu-id="c0279-115">Following are the values for views.</span></span>

-   <span data-ttu-id="c0279-116">\_dettagli vista \_ LV</span><span class="sxs-lookup"><span data-stu-id="c0279-116">LV\_VIEW\_DETAILS</span></span>
-   <span data-ttu-id="c0279-117">\_icona di visualizzazione LV \_</span><span class="sxs-lookup"><span data-stu-id="c0279-117">LV\_VIEW\_ICON</span></span>
-   <span data-ttu-id="c0279-118">\_elenco viste \_ LV</span><span class="sxs-lookup"><span data-stu-id="c0279-118">LV\_VIEW\_LIST</span></span>
-   <span data-ttu-id="c0279-119">\_SMALLICON vista \_ LV</span><span class="sxs-lookup"><span data-stu-id="c0279-119">LV\_VIEW\_SMALLICON</span></span>
-   <span data-ttu-id="c0279-120">\_riquadro Vista \_ LV</span><span class="sxs-lookup"><span data-stu-id="c0279-120">LV\_VIEW\_TILE</span></span>

> [!Note]  
> <span data-ttu-id="c0279-121">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comctl32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="c0279-121">To use this message, you must provide a manifest specifying Comctl32.dll version 6.0.</span></span> <span data-ttu-id="c0279-122">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c0279-122">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c0279-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c0279-123">Requirements</span></span>



| <span data-ttu-id="c0279-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0279-124">Requirement</span></span> | <span data-ttu-id="c0279-125">Valore</span><span class="sxs-lookup"><span data-stu-id="c0279-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c0279-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0279-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c0279-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c0279-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c0279-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0279-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c0279-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c0279-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c0279-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c0279-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0279-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0279-131"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






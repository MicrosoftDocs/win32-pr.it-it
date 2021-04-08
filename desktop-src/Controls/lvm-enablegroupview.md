---
title: Messaggio LVM_ENABLEGROUPVIEW (COMmctrl. h)
description: Abilita o Disabilita se gli elementi in un controllo visualizzazione elenco vengono visualizzati come gruppo.
ms.assetid: 783a5e23-d1cb-4523-a6d2-b2cf93fa7f62
keywords:
- Controlli di Windows Message LVM_ENABLEGROUPVIEW
topic_type:
- apiref
api_name:
- LVM_ENABLEGROUPVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1d546e1236fa4f0800c0353810beb5b427ba4fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047868"
---
# <a name="lvm_enablegroupview-message"></a><span data-ttu-id="b024b-104">\_Messaggio ENABLEGROUPVIEW LVM</span><span class="sxs-lookup"><span data-stu-id="b024b-104">LVM\_ENABLEGROUPVIEW message</span></span>

<span data-ttu-id="b024b-105">Abilita o Disabilita se gli elementi in un controllo visualizzazione elenco vengono visualizzati come gruppo.</span><span class="sxs-lookup"><span data-stu-id="b024b-105">Enables or disables whether the items in a list-view control display as a group.</span></span>

## <a name="parameters"></a><span data-ttu-id="b024b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b024b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b024b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b024b-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b024b-108">**Bool** che indica se abilitare un controllo visualizzazione elenco per raggruppare gli elementi visualizzati.</span><span class="sxs-lookup"><span data-stu-id="b024b-108">A **BOOL** that indicates whether to enable a list-view control to group displayed items.</span></span> <span data-ttu-id="b024b-109">Utilizzare **true** per abilitare il raggruppamento, **false** per disabilitarlo.</span><span class="sxs-lookup"><span data-stu-id="b024b-109">Use **TRUE** to enable grouping, **FALSE** to disable it.</span></span> </dd> <dt>

<span data-ttu-id="b024b-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b024b-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b024b-111">Deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="b024b-111">Must be **NULL**.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b024b-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b024b-112">Return value</span></span>

<span data-ttu-id="b024b-113">Restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="b024b-113">Returns one of the following values.</span></span>



| <span data-ttu-id="b024b-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="b024b-114">Return code</span></span>                                                                       | <span data-ttu-id="b024b-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b024b-115">Description</span></span>                                                                                  |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b024b-116"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="b024b-116"><dt>**0**</dt></span></span> </dl>  | <span data-ttu-id="b024b-117">La possibilità di visualizzare elementi della visualizzazione elenco come gruppo è già abilitata o disabilitata.</span><span class="sxs-lookup"><span data-stu-id="b024b-117">The ability to display list-view items as a group is already enabled or disabled.</span></span><br/> |
| <dl> <span data-ttu-id="b024b-118"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="b024b-118"><dt>**1**</dt></span></span> </dl>  | <span data-ttu-id="b024b-119">Lo stato del controllo è stato modificato correttamente.</span><span class="sxs-lookup"><span data-stu-id="b024b-119">The state of the control was successfully changed.</span></span><br/>                                |
| <dl> <span data-ttu-id="b024b-120"><dt>**-1**</dt></span><span class="sxs-lookup"><span data-stu-id="b024b-120"><dt>**-1**</dt></span></span> </dl> | <span data-ttu-id="b024b-121">Operazione non riuscita.</span><span class="sxs-lookup"><span data-stu-id="b024b-121">The operation failed.</span></span><br/>                                                             |



 

## <a name="remarks"></a><span data-ttu-id="b024b-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="b024b-122">Remarks</span></span>

<span data-ttu-id="b024b-123">**LVM \_ ENABLEGROUPVIEW** non è supportato nello stile [**\_ OWNERDATA di LVS**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="b024b-123">**LVM\_ENABLEGROUPVIEW** is not supported under the [**LVS\_OWNERDATA**](list-view-window-styles.md) style.</span></span>

> [!Note]  
> <span data-ttu-id="b024b-124">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="b024b-124">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="b024b-125">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b024b-125">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b024b-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b024b-126">Requirements</span></span>



| <span data-ttu-id="b024b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b024b-127">Requirement</span></span> | <span data-ttu-id="b024b-128">Valore</span><span class="sxs-lookup"><span data-stu-id="b024b-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b024b-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b024b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b024b-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b024b-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b024b-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b024b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b024b-132">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b024b-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b024b-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b024b-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="b024b-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b024b-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






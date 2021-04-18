---
title: Messaggio LVM_INSERTGROUP (COMmctrl. h)
description: Inserisce un gruppo in un controllo visualizzazione elenco.
ms.assetid: d43e21bc-e212-42dd-af88-48813d40cd50
keywords:
- Controlli di Windows Message LVM_INSERTGROUP
topic_type:
- apiref
api_name:
- LVM_INSERTGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94dbae780f7de26a5c791477e1a7321794054056
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302287"
---
# <a name="lvm_insertgroup-message"></a><span data-ttu-id="f2dce-104">\_Messaggio INSERTGROUP LVM</span><span class="sxs-lookup"><span data-stu-id="f2dce-104">LVM\_INSERTGROUP message</span></span>

<span data-ttu-id="f2dce-105">Inserisce un gruppo in un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="f2dce-105">Inserts a group into a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f2dce-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f2dce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2dce-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f2dce-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f2dce-108">Indice in cui deve essere aggiunto il gruppo.</span><span class="sxs-lookup"><span data-stu-id="f2dce-108">Index where the group is to be added.</span></span> <span data-ttu-id="f2dce-109">Se è-1, il gruppo viene aggiunto alla fine dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="f2dce-109">If this is -1, the group is added at the end of the list.</span></span></dd> <dt>

<span data-ttu-id="f2dce-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f2dce-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f2dce-111">Puntatore a una struttura <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**LVGROUP**</a> contenente il gruppo da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="f2dce-111">Pointer to a <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**LVGROUP**</a> structure that contains the group to add.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2dce-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f2dce-112">Return value</span></span>

<span data-ttu-id="f2dce-113">Restituisce l'indice dell'elemento a cui è stato aggiunto il gruppo oppure-1 se l'operazione non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="f2dce-113">Returns the index of the item that the group was added to, or -1 if the operation failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2dce-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="f2dce-114">Remarks</span></span>

<span data-ttu-id="f2dce-115">Per attivare la modalità gruppo, chiamare [**LVM \_ ENABLEGROUPVIEW**](lvm-enablegroupview.md) o [**ListView \_ ENABLEGROUPVIEW**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview).</span><span class="sxs-lookup"><span data-stu-id="f2dce-115">To turn on group mode, call [**LVM\_ENABLEGROUPVIEW**](lvm-enablegroupview.md) or [**ListView\_EnableGroupView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview).</span></span>

<span data-ttu-id="f2dce-116">Non è possibile inserire un gruppo in un controllo visualizzazione elenco vuoto.</span><span class="sxs-lookup"><span data-stu-id="f2dce-116">A group cannot be inserted into an empty list-view control.</span></span>

<span data-ttu-id="f2dce-117">Assicurarsi di impostare **iGroupId** negli elementi a cui è stato aggiunto il gruppo.</span><span class="sxs-lookup"><span data-stu-id="f2dce-117">Be sure to set the **iGroupId** in the item(s) the group was added to.</span></span> <span data-ttu-id="f2dce-118">In caso contrario, dopo l'elaborazione del messaggio [**LVM \_ ENABLEGROUPVIEW**](lvm-enablegroupview.md) con **true** , il controllo ListView non visualizzerà alcun elemento.</span><span class="sxs-lookup"><span data-stu-id="f2dce-118">Otherwise after [**LVM\_ENABLEGROUPVIEW**](lvm-enablegroupview.md) message processing with **TRUE** the listview control will not show any items.</span></span>

> [!Note]  
> <span data-ttu-id="f2dce-119">Per usare questo messaggio, è necessario fornire un manifesto che specifichi la versione 6,0 di Comclt32.</span><span class="sxs-lookup"><span data-stu-id="f2dce-119">To use this message, you must provide a manifest specifying Comclt32 version 6.0.</span></span> <span data-ttu-id="f2dce-120">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f2dce-120">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f2dce-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f2dce-121">Requirements</span></span>



| <span data-ttu-id="f2dce-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2dce-122">Requirement</span></span> | <span data-ttu-id="f2dce-123">Valore</span><span class="sxs-lookup"><span data-stu-id="f2dce-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f2dce-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f2dce-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f2dce-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f2dce-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f2dce-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f2dce-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f2dce-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f2dce-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f2dce-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f2dce-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2dce-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2dce-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






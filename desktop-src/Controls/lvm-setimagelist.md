---
title: Messaggio LVM_SETIMAGELIST (COMmctrl. h)
description: Assegna un elenco di immagini a un controllo di visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro ListView.
ms.assetid: 5241065b-85e4-412e-9868-fd5b15ff7c17
keywords:
- Controlli di Windows Message LVM_SETIMAGELIST
topic_type:
- apiref
api_name:
- LVM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 779d31fd781a72dbdfbc4738e091482ca4a08528
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963762"
---
# <a name="lvm_setimagelist-message"></a><span data-ttu-id="8afdd-105">Messaggio dell'immagine di LVM \_</span><span class="sxs-lookup"><span data-stu-id="8afdd-105">LVM\_SETIMAGELIST message</span></span>

<span data-ttu-id="8afdd-106">Assegna un elenco di immagini a un controllo di visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="8afdd-106">Assigns an image list to a list-view control.</span></span> <span data-ttu-id="8afdd-107">È possibile inviare questo messaggio in modo esplicito o utilizzando [**la \_ macro ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setimagelist) .</span><span class="sxs-lookup"><span data-stu-id="8afdd-107">You can send this message explicitly or by using the [**ListView\_SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8afdd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8afdd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8afdd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8afdd-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8afdd-110">Tipo di elenco di immagini.</span><span class="sxs-lookup"><span data-stu-id="8afdd-110">Type of image list.</span></span> <span data-ttu-id="8afdd-111">Questo parametro può essere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="8afdd-111">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="8afdd-112">Valore</span><span class="sxs-lookup"><span data-stu-id="8afdd-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="8afdd-113">Significato</span><span class="sxs-lookup"><span data-stu-id="8afdd-113">Meaning</span></span>                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="LVSIL_NORMAL"></span><span id="lvsil_normal"></span><dl> <span data-ttu-id="8afdd-114"><dt>**LVSIL \_ normale**</dt></span><span class="sxs-lookup"><span data-stu-id="8afdd-114"><dt>**LVSIL\_NORMAL**</dt></span></span> </dl>                | <span data-ttu-id="8afdd-115">Elenco immagini con icone grandi.</span><span class="sxs-lookup"><span data-stu-id="8afdd-115">Image list with large icons.</span></span><br/>  |
| <span id="LVSIL_SMALL"></span><span id="lvsil_small"></span><dl> <span data-ttu-id="8afdd-116"><dt>**LVSIL \_ Small**</dt></span><span class="sxs-lookup"><span data-stu-id="8afdd-116"><dt>**LVSIL\_SMALL**</dt></span></span> </dl>                   | <span data-ttu-id="8afdd-117">Elenco immagini con icone piccole.</span><span class="sxs-lookup"><span data-stu-id="8afdd-117">Image list with small icons.</span></span><br/>  |
| <span id="LVSIL_STATE"></span><span id="lvsil_state"></span><dl> <span data-ttu-id="8afdd-118"><dt>**\_stato LVSIL**</dt></span><span class="sxs-lookup"><span data-stu-id="8afdd-118"><dt>**LVSIL\_STATE**</dt></span></span> </dl>                   | <span data-ttu-id="8afdd-119">Elenco immagini con immagini di stato.</span><span class="sxs-lookup"><span data-stu-id="8afdd-119">Image list with state images.</span></span><br/> |
| <span id="LVSIL_GROUPHEADER"></span><span id="lvsil_groupheader"></span><dl> <span data-ttu-id="8afdd-120"><dt>**\_GROUPHEADER LVSIL**</dt></span><span class="sxs-lookup"><span data-stu-id="8afdd-120"><dt>**LVSIL\_GROUPHEADER**</dt></span></span> </dl> | <span data-ttu-id="8afdd-121">Elenco di immagini per l'intestazione di gruppo.</span><span class="sxs-lookup"><span data-stu-id="8afdd-121">Image list for group header.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="8afdd-122">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8afdd-122">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8afdd-123">Handle per l'elenco di immagini da assegnare.</span><span class="sxs-lookup"><span data-stu-id="8afdd-123">Handle to the image list to assign.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8afdd-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8afdd-124">Return value</span></span>

<span data-ttu-id="8afdd-125">Restituisce l'handle per l'elenco di immagini precedentemente associato al controllo, se ha esito positivo, oppure **null** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="8afdd-125">Returns the handle to the image list previously associated with the control if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8afdd-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="8afdd-126">Remarks</span></span>

<span data-ttu-id="8afdd-127">L'elenco di immagini corrente verrà eliminato definitivamente quando il controllo visualizzazione elenco viene eliminato definitivamente, a meno che non sia impostato lo stile di [**\_ SHAREIMAGELISTS LVS**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="8afdd-127">The current image list will be destroyed when the list-view control is destroyed unless the [**LVS\_SHAREIMAGELISTS**](list-view-window-styles.md) style is set.</span></span> <span data-ttu-id="8afdd-128">Se si usa questo messaggio per sostituire un elenco di immagini con un altro, l'applicazione deve eliminare in modo esplicito tutti gli elenchi di immagini diversi da quello corrente.</span><span class="sxs-lookup"><span data-stu-id="8afdd-128">If you use this message to replace one image list with another, your application must explicitly destroy all image lists other than the current one.</span></span>

## <a name="requirements"></a><span data-ttu-id="8afdd-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8afdd-129">Requirements</span></span>



| <span data-ttu-id="8afdd-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="8afdd-130">Requirement</span></span> | <span data-ttu-id="8afdd-131">Valore</span><span class="sxs-lookup"><span data-stu-id="8afdd-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8afdd-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8afdd-132">Minimum supported client</span></span><br/> | <span data-ttu-id="8afdd-133">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8afdd-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8afdd-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8afdd-134">Minimum supported server</span></span><br/> | <span data-ttu-id="8afdd-135">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8afdd-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8afdd-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8afdd-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="8afdd-137"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8afdd-137"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






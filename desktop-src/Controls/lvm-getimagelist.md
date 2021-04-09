---
title: Messaggio LVM_GETIMAGELIST (COMmctrl. h)
description: Recupera l'handle a un elenco di immagini utilizzato per disegnare elementi della visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro ListView Getimagine.
ms.assetid: dd48d8b5-6dbd-48ab-95c3-0fcf1e8c24f0
keywords:
- Controlli di Windows Message LVM_GETIMAGELIST
topic_type:
- apiref
api_name:
- LVM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0abc68c5e5dd9a18c3ec203ad7fe3db97a542845
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120286"
---
# <a name="lvm_getimagelist-message"></a><span data-ttu-id="63da7-105">\_Messaggio GETimagine LVM</span><span class="sxs-lookup"><span data-stu-id="63da7-105">LVM\_GETIMAGELIST message</span></span>

<span data-ttu-id="63da7-106">Recupera l'handle a un elenco di immagini utilizzato per disegnare elementi della visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="63da7-106">Retrieves the handle to an image list used for drawing list-view items.</span></span> <span data-ttu-id="63da7-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ListView \_ getimagine**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getimagelist) .</span><span class="sxs-lookup"><span data-stu-id="63da7-107">You can send this message explicitly or by using the [**ListView\_GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="63da7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="63da7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63da7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="63da7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="63da7-110">Elenco di immagini da recuperare.</span><span class="sxs-lookup"><span data-stu-id="63da7-110">Image list to retrieve.</span></span> <span data-ttu-id="63da7-111">Questo parametro può essere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="63da7-111">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="63da7-112">Valore</span><span class="sxs-lookup"><span data-stu-id="63da7-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="63da7-113">Significato</span><span class="sxs-lookup"><span data-stu-id="63da7-113">Meaning</span></span>                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="LVSIL_NORMAL"></span><span id="lvsil_normal"></span><dl> <span data-ttu-id="63da7-114"><dt>**LVSIL \_ normale**</dt></span><span class="sxs-lookup"><span data-stu-id="63da7-114"><dt>**LVSIL\_NORMAL**</dt></span></span> </dl>                | <span data-ttu-id="63da7-115">Elenco immagini con icone grandi.</span><span class="sxs-lookup"><span data-stu-id="63da7-115">Image list with large icons.</span></span><br/>  |
| <span id="LVSIL_SMALL"></span><span id="lvsil_small"></span><dl> <span data-ttu-id="63da7-116"><dt>**LVSIL \_ Small**</dt></span><span class="sxs-lookup"><span data-stu-id="63da7-116"><dt>**LVSIL\_SMALL**</dt></span></span> </dl>                   | <span data-ttu-id="63da7-117">Elenco immagini con icone piccole.</span><span class="sxs-lookup"><span data-stu-id="63da7-117">Image list with small icons.</span></span><br/>  |
| <span id="LVSIL_STATE"></span><span id="lvsil_state"></span><dl> <span data-ttu-id="63da7-118"><dt>**\_stato LVSIL**</dt></span><span class="sxs-lookup"><span data-stu-id="63da7-118"><dt>**LVSIL\_STATE**</dt></span></span> </dl>                   | <span data-ttu-id="63da7-119">Elenco immagini con immagini di stato.</span><span class="sxs-lookup"><span data-stu-id="63da7-119">Image list with state images.</span></span><br/> |
| <span id="LVSIL_GROUPHEADER"></span><span id="lvsil_groupheader"></span><dl> <span data-ttu-id="63da7-120"><dt>**\_GROUPHEADER LVSIL**</dt></span><span class="sxs-lookup"><span data-stu-id="63da7-120"><dt>**LVSIL\_GROUPHEADER**</dt></span></span> </dl> | <span data-ttu-id="63da7-121">Elenco di immagini per l'intestazione di gruppo.</span><span class="sxs-lookup"><span data-stu-id="63da7-121">Image list for group header.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="63da7-122">*lParam*</span><span class="sxs-lookup"><span data-stu-id="63da7-122">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="63da7-123">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="63da7-123">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63da7-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="63da7-124">Return value</span></span>

<span data-ttu-id="63da7-125">Restituisce l'handle per l'elenco di immagini specificato, in caso di esito positivo; in caso contrario, **null** .</span><span class="sxs-lookup"><span data-stu-id="63da7-125">Returns the handle to the specified image list if successful, or **NULL** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="63da7-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="63da7-126">Requirements</span></span>



| <span data-ttu-id="63da7-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="63da7-127">Requirement</span></span> | <span data-ttu-id="63da7-128">Valore</span><span class="sxs-lookup"><span data-stu-id="63da7-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="63da7-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63da7-129">Minimum supported client</span></span><br/> | <span data-ttu-id="63da7-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="63da7-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="63da7-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63da7-131">Minimum supported server</span></span><br/> | <span data-ttu-id="63da7-132">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="63da7-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="63da7-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="63da7-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="63da7-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="63da7-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






---
description: Inviato da un'estensione di file Manager per recuperare il numero di file selezionati nella finestra Active File Manager (la finestra Directory o la finestra dei risultati della ricerca). Il conteggio include i file con nomi di file lunghi.
title: Messaggio FM_GETSELCOUNTLFN (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETSELCOUNTLFN
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: d0815afc-5356-48a7-a90d-5f48dae6bee5
ms.openlocfilehash: 0a09ca8315405f06db091b27b9d326090796504c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994757"
---
# <a name="fm_getselcountlfn-message"></a><span data-ttu-id="2f558-104">\_Messaggio GETSELCOUNTLFN FM</span><span class="sxs-lookup"><span data-stu-id="2f558-104">FM\_GETSELCOUNTLFN message</span></span>

<span data-ttu-id="2f558-105">Inviato da un'estensione di file Manager per recuperare il numero di file selezionati nella finestra Active File Manager (la finestra Directory o la finestra dei risultati della ricerca).</span><span class="sxs-lookup"><span data-stu-id="2f558-105">Sent by a File Manager extension to retrieve the number of selected files in the active File Manager window (either the directory window or the Search Results window).</span></span> <span data-ttu-id="2f558-106">Il conteggio include i file con nomi di file lunghi.</span><span class="sxs-lookup"><span data-stu-id="2f558-106">The count includes files that have long file names.</span></span>

## <a name="parameters"></a><span data-ttu-id="2f558-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="2f558-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f558-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2f558-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2f558-109">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="2f558-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2f558-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2f558-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2f558-111">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="2f558-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f558-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2f558-112">Return value</span></span>

<span data-ttu-id="2f558-113">Restituisce il numero di file selezionati.</span><span class="sxs-lookup"><span data-stu-id="2f558-113">Returns the number of selected files.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f558-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="2f558-114">Remarks</span></span>

<span data-ttu-id="2f558-115">Questo messaggio deve essere utilizzato solo dalle estensioni che supportano nomi di file lunghi (ad esempio, le estensioni che supportano la rete).</span><span class="sxs-lookup"><span data-stu-id="2f558-115">Only extensions that support long file names (for example, network-aware extensions) should use this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f558-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f558-116">Requirements</span></span>



| <span data-ttu-id="2f558-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f558-117">Requirement</span></span> | <span data-ttu-id="2f558-118">Valore</span><span class="sxs-lookup"><span data-stu-id="2f558-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2f558-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f558-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2f558-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2f558-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="2f558-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f558-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2f558-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2f558-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2f558-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2f558-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f558-124"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f558-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f558-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2f558-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f558-126">**\_GETFILESEL FM**</span><span class="sxs-lookup"><span data-stu-id="2f558-126">**FM\_GETFILESEL**</span></span>](fm-getfilesel.md)
</dt> <dt>

[<span data-ttu-id="2f558-127">**\_GETFILESELLFN FM**</span><span class="sxs-lookup"><span data-stu-id="2f558-127">**FM\_GETFILESELLFN**</span></span>](fm-getfilesellfn.md)
</dt> <dt>

[<span data-ttu-id="2f558-128">**\_GETSELCOUNT FM**</span><span class="sxs-lookup"><span data-stu-id="2f558-128">**FM\_GETSELCOUNT**</span></span>](fm-getselcount.md)
</dt> </dl>

 

 





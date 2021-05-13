---
description: Inviato da un'estensione di File Manager per recuperare il numero di file selezionati nella finestra di Gestione file attiva (nella finestra della directory o nella finestra Risultati ricerca). Il conteggio include i file con nomi di file lunghi.
title: FM_GETSELCOUNTLFN messaggio (Wfext.h)
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
ms.openlocfilehash: 1ec06c08775836a94b9ada6520ea7c5ea46b62f3
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841342"
---
# <a name="fm_getselcountlfn-message"></a><span data-ttu-id="b9f8a-104">Messaggio \_ FM GETSELCOUNTLFN</span><span class="sxs-lookup"><span data-stu-id="b9f8a-104">FM\_GETSELCOUNTLFN message</span></span>

<span data-ttu-id="b9f8a-105">Inviato da un'estensione di File Manager per recuperare il numero di file selezionati nella finestra di Gestione file attiva (nella finestra della directory o nella finestra Risultati ricerca).</span><span class="sxs-lookup"><span data-stu-id="b9f8a-105">Sent by a File Manager extension to retrieve the number of selected files in the active File Manager window (either the directory window or the Search Results window).</span></span> <span data-ttu-id="b9f8a-106">Il conteggio include i file con nomi di file lunghi.</span><span class="sxs-lookup"><span data-stu-id="b9f8a-106">The count includes files that have long file names.</span></span>

## <a name="parameters"></a><span data-ttu-id="b9f8a-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="b9f8a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9f8a-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b9f8a-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b9f8a-109">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="b9f8a-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b9f8a-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b9f8a-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b9f8a-111">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="b9f8a-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9f8a-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b9f8a-112">Return value</span></span>

<span data-ttu-id="b9f8a-113">Restituisce il numero di file selezionati.</span><span class="sxs-lookup"><span data-stu-id="b9f8a-113">Returns the number of selected files.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9f8a-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="b9f8a-114">Remarks</span></span>

<span data-ttu-id="b9f8a-115">Questo messaggio deve essere utilizzato solo per le estensioni che supportano nomi di file lunghi, ad esempio estensioni che supportano la rete.</span><span class="sxs-lookup"><span data-stu-id="b9f8a-115">Only extensions that support long file names (for example, network-aware extensions) should use this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9f8a-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9f8a-116">Requirements</span></span>



| <span data-ttu-id="b9f8a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9f8a-117">Requirement</span></span> | <span data-ttu-id="b9f8a-118">Valore</span><span class="sxs-lookup"><span data-stu-id="b9f8a-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b9f8a-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9f8a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b9f8a-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b9f8a-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="b9f8a-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9f8a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b9f8a-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b9f8a-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b9f8a-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b9f8a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9f8a-124"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="b9f8a-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9f8a-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b9f8a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9f8a-126">**FM \_ GETFILESEL**</span><span class="sxs-lookup"><span data-stu-id="b9f8a-126">**FM\_GETFILESEL**</span></span>](fm-getfilesel.md)
</dt> <dt>

[<span data-ttu-id="b9f8a-127">**FM \_ GETFILESELLFN**</span><span class="sxs-lookup"><span data-stu-id="b9f8a-127">**FM\_GETFILESELLFN**</span></span>](fm-getfilesellfn.md)
</dt> <dt>

[<span data-ttu-id="b9f8a-128">**FM \_ GETSELCOUNT**</span><span class="sxs-lookup"><span data-stu-id="b9f8a-128">**FM\_GETSELCOUNT**</span></span>](fm-getselcount.md)
</dt> </dl>

 

 





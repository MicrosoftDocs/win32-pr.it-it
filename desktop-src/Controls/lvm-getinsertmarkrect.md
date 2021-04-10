---
title: Messaggio LVM_GETINSERTMARKRECT (COMmctrl. h)
description: Recupera il rettangolo che delimita il punto di inserimento.
ms.assetid: 7b10229c-73ab-426c-8a8a-71258a33e248
keywords:
- Controlli di Windows Message LVM_GETINSERTMARKRECT
topic_type:
- apiref
api_name:
- LVM_GETINSERTMARKRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd85bfb94f6425d2666372fd141b531fcb238643
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964745"
---
# <a name="lvm_getinsertmarkrect-message"></a><span data-ttu-id="bdbb3-104">\_Messaggio GETINSERTMARKRECT LVM</span><span class="sxs-lookup"><span data-stu-id="bdbb3-104">LVM\_GETINSERTMARKRECT message</span></span>

<span data-ttu-id="bdbb3-105">Recupera il rettangolo che delimita il punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="bdbb3-105">Retrieves the rectangle that bounds the insertion point.</span></span>

## <a name="parameters"></a><span data-ttu-id="bdbb3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bdbb3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdbb3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bdbb3-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bdbb3-108">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="bdbb3-108">Not used; must be zero.</span></span></dd> <dt>

<span data-ttu-id="bdbb3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bdbb3-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bdbb3-110">Puntatore a una struttura <a href="/previous-versions//dd162897(v=vs.85)">**Rect**</a> che contiene le coordinate di un rettangolo che delimita il punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="bdbb3-110">Pointer to a <a href="/previous-versions//dd162897(v=vs.85)">**RECT**</a> structure that contains the coordinates of a rectangle that bounds the insertion point.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdbb3-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bdbb3-111">Return value</span></span>

<span data-ttu-id="bdbb3-112">Restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="bdbb3-112">Returns one of the following values.</span></span>



| <span data-ttu-id="bdbb3-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="bdbb3-113">Return code</span></span>                                                                      | <span data-ttu-id="bdbb3-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bdbb3-114">Description</span></span>                          |
|----------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="bdbb3-115"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="bdbb3-115"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="bdbb3-116">Nessun punto di inserimento trovato.</span><span class="sxs-lookup"><span data-stu-id="bdbb3-116">No insertion point found.</span></span><br/> |
| <dl> <span data-ttu-id="bdbb3-117"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="bdbb3-117"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="bdbb3-118">Trovato punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="bdbb3-118">Insertion point found.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="bdbb3-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="bdbb3-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bdbb3-120">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="bdbb3-120">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="bdbb3-121">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="bdbb3-121">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bdbb3-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bdbb3-122">Requirements</span></span>



| <span data-ttu-id="bdbb3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdbb3-123">Requirement</span></span> | <span data-ttu-id="bdbb3-124">Valore</span><span class="sxs-lookup"><span data-stu-id="bdbb3-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bdbb3-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bdbb3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="bdbb3-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bdbb3-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bdbb3-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bdbb3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="bdbb3-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bdbb3-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bdbb3-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bdbb3-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdbb3-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdbb3-130"><dt>Commctrl.h</dt></span></span> </dl> |



 


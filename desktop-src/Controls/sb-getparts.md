---
title: Messaggio SB_GETPARTS (COMmctrl. h)
description: Recupera un conteggio delle parti in una finestra di stato. Il messaggio recupera inoltre la coordinata del bordo destro del numero di parti specificato.
ms.assetid: 2535f490-4d6b-468a-b13c-096941e61bf4
keywords:
- Controlli di Windows Message SB_GETPARTS
topic_type:
- apiref
api_name:
- SB_GETPARTS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cee0f33331c579490cf66a38b9ce6655215ae673
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518447"
---
# <a name="sb_getparts-message"></a><span data-ttu-id="ffcb4-105">\_Messaggio SB GETparts</span><span class="sxs-lookup"><span data-stu-id="ffcb4-105">SB\_GETPARTS message</span></span>

<span data-ttu-id="ffcb4-106">Recupera un conteggio delle parti in una finestra di stato.</span><span class="sxs-lookup"><span data-stu-id="ffcb4-106">Retrieves a count of the parts in a status window.</span></span> <span data-ttu-id="ffcb4-107">Il messaggio recupera inoltre la coordinata del bordo destro del numero di parti specificato.</span><span class="sxs-lookup"><span data-stu-id="ffcb4-107">The message also retrieves the coordinate of the right edge of the specified number of parts.</span></span>

## <a name="parameters"></a><span data-ttu-id="ffcb4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ffcb4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffcb4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ffcb4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ffcb4-110">Numero di parti per le quali recuperare le coordinate.</span><span class="sxs-lookup"><span data-stu-id="ffcb4-110">Number of parts for which to retrieve coordinates.</span></span> <span data-ttu-id="ffcb4-111">Se questo parametro è maggiore del numero di parti nella finestra, il messaggio recupera le coordinate solo per le parti esistenti.</span><span class="sxs-lookup"><span data-stu-id="ffcb4-111">If this parameter is greater than the number of parts in the window, the message retrieves coordinates for existing parts only.</span></span>

</dd> <dt>

<span data-ttu-id="ffcb4-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ffcb4-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ffcb4-113">Puntatore a una matrice di interi che ha lo stesso numero di elementi delle parti specificate da *wParam*.</span><span class="sxs-lookup"><span data-stu-id="ffcb4-113">Pointer to an integer array that has the same number of elements as parts specified by *wParam*.</span></span> <span data-ttu-id="ffcb4-114">Ogni elemento nella matrice riceve la coordinata client del bordo destro della parte corrispondente.</span><span class="sxs-lookup"><span data-stu-id="ffcb4-114">Each element in the array receives the client coordinate of the right edge of the corresponding part.</span></span> <span data-ttu-id="ffcb4-115">Se un elemento è impostato su-1, la posizione del bordo destro della parte viene estesa al bordo destro della finestra.</span><span class="sxs-lookup"><span data-stu-id="ffcb4-115">If an element is set to -1, the position of the right edge for that part extends to the right edge of the window.</span></span> <span data-ttu-id="ffcb4-116">Per recuperare il numero corrente di parti, impostare questo parametro su zero.</span><span class="sxs-lookup"><span data-stu-id="ffcb4-116">To retrieve the current number of parts, set this parameter to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffcb4-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ffcb4-117">Return value</span></span>

<span data-ttu-id="ffcb4-118">Restituisce il numero di parti nella finestra.</span><span class="sxs-lookup"><span data-stu-id="ffcb4-118">Returns the number of parts in the window.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffcb4-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="ffcb4-119">Remarks</span></span>

<span data-ttu-id="ffcb4-120">Questo messaggio restituisce sempre il numero di parti nella barra di stato.</span><span class="sxs-lookup"><span data-stu-id="ffcb4-120">This message always returns the number of parts in the status bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffcb4-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ffcb4-121">Requirements</span></span>



| <span data-ttu-id="ffcb4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffcb4-122">Requirement</span></span> | <span data-ttu-id="ffcb4-123">Valore</span><span class="sxs-lookup"><span data-stu-id="ffcb4-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ffcb4-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ffcb4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ffcb4-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ffcb4-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ffcb4-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ffcb4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ffcb4-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ffcb4-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ffcb4-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ffcb4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffcb4-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffcb4-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






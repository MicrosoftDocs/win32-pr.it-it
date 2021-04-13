---
title: Messaggio SB_SETPARTS (COMmctrl. h)
description: Imposta il numero di parti in una finestra di stato e la coordinata del bordo destro di ogni parte.
ms.assetid: e29e8b09-c018-4ea4-8b47-6f3713113427
keywords:
- Controlli di Windows Message SB_SETPARTS
topic_type:
- apiref
api_name:
- SB_SETPARTS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 062058fa3778cd0394cadd9d76b363a0353ffb2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518436"
---
# <a name="sb_setparts-message"></a><span data-ttu-id="ecb70-104">\_Messaggio di SEparazione SB</span><span class="sxs-lookup"><span data-stu-id="ecb70-104">SB\_SETPARTS message</span></span>

<span data-ttu-id="ecb70-105">Imposta il numero di parti in una finestra di stato e la coordinata del bordo destro di ogni parte.</span><span class="sxs-lookup"><span data-stu-id="ecb70-105">Sets the number of parts in a status window and the coordinate of the right edge of each part.</span></span>

## <a name="parameters"></a><span data-ttu-id="ecb70-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ecb70-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecb70-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ecb70-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ecb70-108">Numero di parti da impostare (non può essere maggiore di 256).</span><span class="sxs-lookup"><span data-stu-id="ecb70-108">Number of parts to set (cannot be greater than 256).</span></span>

</dd> <dt>

<span data-ttu-id="ecb70-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ecb70-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ecb70-110">Puntatore a una matrice di interi.</span><span class="sxs-lookup"><span data-stu-id="ecb70-110">Pointer to an integer array.</span></span> <span data-ttu-id="ecb70-111">Il numero di elementi è specificato in *wParam*.</span><span class="sxs-lookup"><span data-stu-id="ecb70-111">The number of elements is specified in *wParam*.</span></span> <span data-ttu-id="ecb70-112">Ogni elemento specifica la posizione, in coordinate client, del bordo destro della parte corrispondente.</span><span class="sxs-lookup"><span data-stu-id="ecb70-112">Each element specifies the position, in client coordinates, of the right edge of the corresponding part.</span></span> <span data-ttu-id="ecb70-113">Se un elemento è-1, il bordo destro della parte corrispondente si estende al bordo della finestra.</span><span class="sxs-lookup"><span data-stu-id="ecb70-113">If an element is -1, the right edge of the corresponding part extends to the border of the window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecb70-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ecb70-114">Return value</span></span>

<span data-ttu-id="ecb70-115">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="ecb70-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecb70-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ecb70-116">Requirements</span></span>



| <span data-ttu-id="ecb70-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecb70-117">Requirement</span></span> | <span data-ttu-id="ecb70-118">Valore</span><span class="sxs-lookup"><span data-stu-id="ecb70-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ecb70-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ecb70-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ecb70-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ecb70-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ecb70-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ecb70-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ecb70-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ecb70-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ecb70-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ecb70-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecb70-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecb70-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






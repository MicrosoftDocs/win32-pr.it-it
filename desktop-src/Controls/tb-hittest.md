---
title: Messaggio TB_HITTEST (COMmctrl. h)
description: Determina se un punto si trova in un controllo Toolbar.
ms.assetid: d08f3805-2042-470e-8f5a-8a6a681d1189
keywords:
- Controlli di Windows Message TB_HITTEST
topic_type:
- apiref
api_name:
- TB_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6264bc0191f091d3819081ddd67e428b64c84570
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964039"
---
# <a name="tb_hittest-message"></a><span data-ttu-id="bcf78-104">\_Messaggio HITTEST TB</span><span class="sxs-lookup"><span data-stu-id="bcf78-104">TB\_HITTEST message</span></span>

<span data-ttu-id="bcf78-105">Determina se un punto si trova in un controllo Toolbar.</span><span class="sxs-lookup"><span data-stu-id="bcf78-105">Determines where a point lies in a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="bcf78-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bcf78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcf78-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bcf78-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bcf78-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="bcf78-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bcf78-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bcf78-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bcf78-110">Puntatore a una struttura di [**punti**](/previous-versions//dd162805(v=vs.85)) che contiene la coordinata x dell'hit test nel membro **x** e la coordinata y dell'hit test nel membro **y** .</span><span class="sxs-lookup"><span data-stu-id="bcf78-110">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that contains the x-coordinate of the hit test in the **x** member and the y-coordinate of the hit test in the **y** member.</span></span> <span data-ttu-id="bcf78-111">Le coordinate sono relative all'area client della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="bcf78-111">The coordinates are relative to the toolbar's client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcf78-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bcf78-112">Return value</span></span>

<span data-ttu-id="bcf78-113">Restituisce un valore intero.</span><span class="sxs-lookup"><span data-stu-id="bcf78-113">Returns an integer value.</span></span> <span data-ttu-id="bcf78-114">Se il valore restituito è zero o un valore positivo, si tratta dell'indice in base zero dell'elemento non separatore in cui si trova il punto.</span><span class="sxs-lookup"><span data-stu-id="bcf78-114">If the return value is zero or a positive value, it is the zero-based index of the nonseparator item in which the point lies.</span></span> <span data-ttu-id="bcf78-115">Se il valore restituito è negativo, il punto non si trova all'interno di un pulsante.</span><span class="sxs-lookup"><span data-stu-id="bcf78-115">If the return value is negative, the point does not lie within a button.</span></span> <span data-ttu-id="bcf78-116">Il valore assoluto del valore restituito è l'indice di un elemento separatore o l'elemento non separatore più vicino.</span><span class="sxs-lookup"><span data-stu-id="bcf78-116">The absolute value of the return value is the index of a separator item or the nearest nonseparator item.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcf78-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bcf78-117">Requirements</span></span>



| <span data-ttu-id="bcf78-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcf78-118">Requirement</span></span> | <span data-ttu-id="bcf78-119">Valore</span><span class="sxs-lookup"><span data-stu-id="bcf78-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bcf78-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bcf78-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bcf78-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bcf78-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bcf78-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bcf78-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bcf78-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bcf78-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bcf78-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bcf78-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bcf78-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcf78-125"><dt>Commctrl.h</dt></span></span> </dl> |



 


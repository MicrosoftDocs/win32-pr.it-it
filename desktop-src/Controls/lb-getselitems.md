---
title: Messaggio LB_GETSELITEMS (winuser. h)
description: Riempie un buffer con una matrice di Integer che specificano i numeri degli elementi selezionati in una casella di riepilogo a selezione multipla.
ms.assetid: 95dd72ef-76a5-4188-b2c8-d4c5eb2f34e3
keywords:
- Controlli di Windows Message LB_GETSELITEMS
topic_type:
- apiref
api_name:
- LB_GETSELITEMS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 703988749cc5091bc3196f7c6e70364edb40ee04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964294"
---
# <a name="lb_getselitems-message"></a><span data-ttu-id="338cc-104">\_Messaggio GETSELITEMS lb</span><span class="sxs-lookup"><span data-stu-id="338cc-104">LB\_GETSELITEMS message</span></span>

<span data-ttu-id="338cc-105">Riempie un buffer con una matrice di Integer che specificano i numeri degli elementi selezionati in una casella di riepilogo a selezione multipla.</span><span class="sxs-lookup"><span data-stu-id="338cc-105">Fills a buffer with an array of integers that specify the item numbers of selected items in a multiple-selection list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="338cc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="338cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="338cc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="338cc-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="338cc-108">Numero massimo di elementi selezionati i cui numeri di elemento devono essere inseriti nel buffer.</span><span class="sxs-lookup"><span data-stu-id="338cc-108">The maximum number of selected items whose item numbers are to be placed in the buffer.</span></span>

<span data-ttu-id="338cc-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il parametro *wParam* è limitato ai valori a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="338cc-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="338cc-110">Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi.</span><span class="sxs-lookup"><span data-stu-id="338cc-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="338cc-111">Sebbene il numero di elementi sia limitato, le dimensioni totali in byte degli elementi in una casella di riepilogo sono limitate solo dalla memoria disponibile.</span><span class="sxs-lookup"><span data-stu-id="338cc-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="338cc-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="338cc-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="338cc-113">Puntatore a un buffer sufficientemente grande per il numero di numeri interi specificati dal parametro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="338cc-113">A pointer to a buffer large enough for the number of integers specified by the *wParam* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="338cc-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="338cc-114">Return value</span></span>

<span data-ttu-id="338cc-115">Il valore restituito è il numero di elementi inseriti nel buffer.</span><span class="sxs-lookup"><span data-stu-id="338cc-115">The return value is the number of items placed in the buffer.</span></span> <span data-ttu-id="338cc-116">Se la casella di riepilogo è una casella di riepilogo a selezione singola, il valore restituito è LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="338cc-116">If the list box is a single-selection list box, the return value is LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="338cc-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="338cc-117">Requirements</span></span>



| <span data-ttu-id="338cc-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="338cc-118">Requirement</span></span> | <span data-ttu-id="338cc-119">Valore</span><span class="sxs-lookup"><span data-stu-id="338cc-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="338cc-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="338cc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="338cc-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="338cc-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="338cc-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="338cc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="338cc-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="338cc-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="338cc-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="338cc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="338cc-125"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="338cc-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="338cc-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="338cc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="338cc-127">**\_GETSELCOUNT lb**</span><span class="sxs-lookup"><span data-stu-id="338cc-127">**LB\_GETSELCOUNT**</span></span>](lb-getselcount.md)
</dt> </dl>

 

 






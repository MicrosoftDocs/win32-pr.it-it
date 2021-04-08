---
title: Messaggio LVM_GETCOLUMNORDERARRAY (COMmctrl. h)
description: Ottiene l'ordine da sinistra a destra corrente delle colonne in un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro GetColumnOrderArray di ListView.
ms.assetid: d4636aa8-c61e-4467-abc7-eea897bf370e
keywords:
- Controlli di Windows Message LVM_GETCOLUMNORDERARRAY
topic_type:
- apiref
api_name:
- LVM_GETCOLUMNORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aee387f65abd3f30826e361778d5acac02dfab7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047863"
---
# <a name="lvm_getcolumnorderarray-message"></a><span data-ttu-id="48025-105">\_Messaggio GETCOLUMNORDERARRAY LVM</span><span class="sxs-lookup"><span data-stu-id="48025-105">LVM\_GETCOLUMNORDERARRAY message</span></span>

<span data-ttu-id="48025-106">Ottiene l'ordine da sinistra a destra corrente delle colonne in un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="48025-106">Gets the current left-to-right order of columns in a list-view control.</span></span> <span data-ttu-id="48025-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ GetColumnOrderArray di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnorderarray) .</span><span class="sxs-lookup"><span data-stu-id="48025-107">You can send this message explicitly or use the [**ListView\_GetColumnOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnorderarray) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="48025-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="48025-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48025-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="48025-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="48025-110">Numero di colonne nel controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="48025-110">The number of columns in the list-view control.</span></span>

</dd> <dt>

<span data-ttu-id="48025-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="48025-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="48025-112">Puntatore a una matrice di numeri interi che riceve i valori di indice delle colonne nel controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="48025-112">A pointer to an array of integers that receives the index values of the columns in the list-view control.</span></span> <span data-ttu-id="48025-113">La matrice deve essere sufficientemente grande da contenere gli elementi *wParam* .</span><span class="sxs-lookup"><span data-stu-id="48025-113">The array must be large enough to hold *wParam* elements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48025-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="48025-114">Return value</span></span>

<span data-ttu-id="48025-115">In caso di esito positivo, restituisce un valore diverso da zero e il buffer in *lParam* riceve l'indice di colonna di ogni colonna nel controllo nell'ordine in cui appaiono da sinistra a destra.</span><span class="sxs-lookup"><span data-stu-id="48025-115">If successful, returns nonzero, and the buffer at *lParam* receives the column index of each column in the control in the order they appear from left to right.</span></span> <span data-ttu-id="48025-116">In caso contrario, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="48025-116">Otherwise, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="48025-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="48025-117">Requirements</span></span>



| <span data-ttu-id="48025-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="48025-118">Requirement</span></span> | <span data-ttu-id="48025-119">Valore</span><span class="sxs-lookup"><span data-stu-id="48025-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="48025-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="48025-120">Minimum supported client</span></span><br/> | <span data-ttu-id="48025-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="48025-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="48025-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="48025-122">Minimum supported server</span></span><br/> | <span data-ttu-id="48025-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="48025-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="48025-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="48025-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="48025-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="48025-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






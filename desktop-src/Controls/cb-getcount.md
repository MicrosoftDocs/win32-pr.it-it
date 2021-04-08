---
title: Messaggio CB_GETCOUNT (winuser. h)
description: Ottiene il numero di elementi nella casella di riepilogo di una casella combinata.
ms.assetid: 69667724-5452-4fcc-afc3-0d98d3beedc8
keywords:
- Controlli di Windows Message CB_GETCOUNT
topic_type:
- apiref
api_name:
- CB_GETCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7900aadf3ba87cc7603a3fe15f4974911c9f9a37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103744018"
---
# <a name="cb_getcount-message"></a><span data-ttu-id="e1b34-104">\_Messaggio GETCOUNT CB</span><span class="sxs-lookup"><span data-stu-id="e1b34-104">CB\_GETCOUNT message</span></span>

<span data-ttu-id="e1b34-105">Ottiene il numero di elementi nella casella di riepilogo di una casella combinata.</span><span class="sxs-lookup"><span data-stu-id="e1b34-105">Gets the number of items in the list box of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="e1b34-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e1b34-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1b34-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e1b34-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e1b34-108">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="e1b34-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e1b34-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e1b34-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e1b34-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="e1b34-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1b34-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e1b34-111">Return value</span></span>

<span data-ttu-id="e1b34-112">Il valore restituito è il numero di elementi nella casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="e1b34-112">The return value is the number of items in the list box.</span></span> <span data-ttu-id="e1b34-113">Se si verifica un errore, è CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="e1b34-113">If an error occurs, it is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1b34-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="e1b34-114">Remarks</span></span>

<span data-ttu-id="e1b34-115">L'indice è in base zero, quindi il conteggio restituito è maggiore di uno rispetto al valore di indice dell'ultimo elemento.</span><span class="sxs-lookup"><span data-stu-id="e1b34-115">The index is zero-based, so the returned count is one greater than the index value of the last item.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1b34-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e1b34-116">Requirements</span></span>



| <span data-ttu-id="e1b34-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1b34-117">Requirement</span></span> | <span data-ttu-id="e1b34-118">Valore</span><span class="sxs-lookup"><span data-stu-id="e1b34-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1b34-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e1b34-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e1b34-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e1b34-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e1b34-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e1b34-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e1b34-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e1b34-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e1b34-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e1b34-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1b34-124"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e1b34-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 






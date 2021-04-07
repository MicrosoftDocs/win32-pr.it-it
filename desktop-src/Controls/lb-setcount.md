---
title: Messaggio LB_SETCOUNT (winuser. h)
description: Imposta il numero di elementi in una casella di riepilogo creata con lo \_ stile NODATA lbs e non viene creato con lo \_ stile HASSTRINGS lbs.
ms.assetid: 3ebc4237-24d3-443f-86d5-bdcd66a31baf
keywords:
- Controlli di Windows Message LB_SETCOUNT
topic_type:
- apiref
api_name:
- LB_SETCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2042bcf0e0cbe7f5daacfcf7f493a070860ac9a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048649"
---
# <a name="lb_setcount-message"></a><span data-ttu-id="1a76b-104">\_Messaggi di conteggio lb</span><span class="sxs-lookup"><span data-stu-id="1a76b-104">LB\_SETCOUNT message</span></span>

<span data-ttu-id="1a76b-105">Imposta il numero di elementi in una casella di riepilogo creata con lo stile [**\_ NoData lbs**](list-box-styles.md) e non viene creato con lo stile [**\_ HASSTRINGS lbs**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="1a76b-105">Sets the count of items in a list box created with the [**LBS\_NODATA**](list-box-styles.md) style and not created with the [**LBS\_HASSTRINGS**](list-box-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="1a76b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1a76b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a76b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1a76b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1a76b-108">Specifica il nuovo conteggio degli elementi nella casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="1a76b-108">Specifies the new count of items in the list box.</span></span>

<span data-ttu-id="1a76b-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il parametro *wParam* è limitato ai valori a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="1a76b-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="1a76b-110">Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi.</span><span class="sxs-lookup"><span data-stu-id="1a76b-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="1a76b-111">Sebbene il numero di elementi sia limitato, le dimensioni totali in byte degli elementi in una casella di riepilogo sono limitate solo dalla memoria disponibile.</span><span class="sxs-lookup"><span data-stu-id="1a76b-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="1a76b-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1a76b-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1a76b-113">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="1a76b-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a76b-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1a76b-114">Return value</span></span>

<span data-ttu-id="1a76b-115">Se si verifica un errore, il valore restituito è LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="1a76b-115">If an error occurs, the return value is LB\_ERR.</span></span> <span data-ttu-id="1a76b-116">Se la memoria disponibile non è sufficiente per archiviare gli elementi, il valore restituito è LB \_ ERRSPACE.</span><span class="sxs-lookup"><span data-stu-id="1a76b-116">If there is insufficient memory to store the items, the return value is LB\_ERRSPACE.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a76b-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="1a76b-117">Remarks</span></span>

<span data-ttu-id="1a76b-118">Il messaggio **lb \_ secount** è supportato solo dalle caselle di riepilogo create con lo stile [**\_ NoData di lbs**](list-box-styles.md) e non create con lo stile [**\_ HASSTRINGS lbs**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="1a76b-118">The **LB\_SETCOUNT** message is supported only by list boxes created with the [**LBS\_NODATA**](list-box-styles.md) style and not created with the [**LBS\_HASSTRINGS**](list-box-styles.md) style.</span></span> <span data-ttu-id="1a76b-119">Tutte le altre caselle di riepilogo restituiscono LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="1a76b-119">All other list boxes return LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a76b-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1a76b-120">Requirements</span></span>



| <span data-ttu-id="1a76b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a76b-121">Requirement</span></span> | <span data-ttu-id="1a76b-122">Valore</span><span class="sxs-lookup"><span data-stu-id="1a76b-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a76b-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1a76b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1a76b-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1a76b-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1a76b-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1a76b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1a76b-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1a76b-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1a76b-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1a76b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a76b-128"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1a76b-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a76b-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1a76b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a76b-130">**CONTEGGIO di LB \_**</span><span class="sxs-lookup"><span data-stu-id="1a76b-130">**LB\_GETCOUNT**</span></span>](lb-getcount.md)
</dt> </dl>

 

 






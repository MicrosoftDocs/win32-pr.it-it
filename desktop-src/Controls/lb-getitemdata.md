---
title: Messaggio LB_GETITEMDATA (winuser. h)
description: Ottiene il valore definito dall'applicazione associato all'elemento della casella di riepilogo specificato.
ms.assetid: 3a3f7fa5-ce04-4e95-86e1-5c7de796d1b6
keywords:
- Controlli di Windows Message LB_GETITEMDATA
topic_type:
- apiref
api_name:
- LB_GETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80da838828cad7354aaa244f2218e8f9a8346755
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121311"
---
# <a name="lb_getitemdata-message"></a><span data-ttu-id="ee056-104">\_Messaggio GETITEMDATA lb</span><span class="sxs-lookup"><span data-stu-id="ee056-104">LB\_GETITEMDATA message</span></span>

<span data-ttu-id="ee056-105">Ottiene il valore definito dall'applicazione associato all'elemento della casella di riepilogo specificato.</span><span class="sxs-lookup"><span data-stu-id="ee056-105">Gets the application-defined value associated with the specified list box item.</span></span>

## <a name="parameters"></a><span data-ttu-id="ee056-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ee056-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee056-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ee056-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ee056-108">Indice dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="ee056-108">The index of the item.</span></span>

<span data-ttu-id="ee056-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il parametro *wParam* è limitato ai valori a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="ee056-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="ee056-110">Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi.</span><span class="sxs-lookup"><span data-stu-id="ee056-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="ee056-111">Sebbene il numero di elementi sia limitato, le dimensioni totali in byte degli elementi in una casella di riepilogo sono limitate solo dalla memoria disponibile.</span><span class="sxs-lookup"><span data-stu-id="ee056-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="ee056-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ee056-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ee056-113">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="ee056-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee056-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ee056-114">Return value</span></span>

<span data-ttu-id="ee056-115">Il valore restituito è il valore associato all'elemento, oppure LB \_ Err se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="ee056-115">The return value is the value associated with the item, or LB\_ERR if an error occurs.</span></span> <span data-ttu-id="ee056-116">Se l'elemento si trova in una casella di riepilogo creata dal proprietario ed è stato creato senza lo stile [**\_ HASSTRINGS lbs**](list-box-styles.md) , questo valore era nel parametro *lParam* del messaggio [**lb \_ ADDSTRING**](lb-addstring.md) o [**lb \_ INSERTSTRING**](lb-insertstring.md) che ha aggiunto l'elemento alla casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="ee056-116">If the item is in an owner-drawn list box and was created without the [**LBS\_HASSTRINGS**](list-box-styles.md) style, this value was in the *lParam* parameter of the [**LB\_ADDSTRING**](lb-addstring.md) or [**LB\_INSERTSTRING**](lb-insertstring.md) message that added the item to the list box.</span></span> <span data-ttu-id="ee056-117">In caso contrario, è il valore nel valore *lParam* del [**messaggio \_ SETITEMDATA lb**](lb-setitemdata.md) .</span><span class="sxs-lookup"><span data-stu-id="ee056-117">Otherwise, it is the value in the *lParam* of the [**LB\_SETITEMDATA**](lb-setitemdata.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee056-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ee056-118">Requirements</span></span>



| <span data-ttu-id="ee056-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee056-119">Requirement</span></span> | <span data-ttu-id="ee056-120">Valore</span><span class="sxs-lookup"><span data-stu-id="ee056-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee056-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee056-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ee056-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ee056-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ee056-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee056-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ee056-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ee056-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ee056-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ee056-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee056-126"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ee056-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee056-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ee056-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="ee056-128">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="ee056-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ee056-129">**\_ADDSTRING lb**</span><span class="sxs-lookup"><span data-stu-id="ee056-129">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="ee056-130">**\_INSERTSTRING lb**</span><span class="sxs-lookup"><span data-stu-id="ee056-130">**LB\_INSERTSTRING**</span></span>](lb-insertstring.md)
</dt> <dt>

[<span data-ttu-id="ee056-131">**\_SETITEMDATA lb**</span><span class="sxs-lookup"><span data-stu-id="ee056-131">**LB\_SETITEMDATA**</span></span>](lb-setitemdata.md)
</dt> </dl>

 

 






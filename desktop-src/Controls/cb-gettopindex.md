---
title: Messaggio CB_GETTOPINDEX (winuser. h)
description: Un'applicazione invia il \_ messaggio CB GETTOPINDEX per recuperare l'indice in base zero del primo elemento visibile nella parte della casella di riepilogo di una casella combinata.
ms.assetid: vs|controls|~\controls\comboboxes\comboboxreference\comboboxmessages\cb_gettopindex.htm
keywords:
- Controlli di Windows Message CB_GETTOPINDEX
topic_type:
- apiref
api_name:
- CB_GETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59d5d6834dd954261822c8b1cb1a449d16398284
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964204"
---
# <a name="cb_gettopindex-message"></a><span data-ttu-id="25b76-104">\_Messaggio GETTOPINDEX CB</span><span class="sxs-lookup"><span data-stu-id="25b76-104">CB\_GETTOPINDEX message</span></span>

<span data-ttu-id="25b76-105">Un'applicazione invia il messaggio **CB \_ GETTOPINDEX** per recuperare l'indice in base zero del primo elemento visibile nella parte della casella di riepilogo di una casella combinata.</span><span class="sxs-lookup"><span data-stu-id="25b76-105">An application sends the **CB\_GETTOPINDEX** message to retrieve the zero-based index of the first visible item in the list box portion of a combo box.</span></span> <span data-ttu-id="25b76-106">Inizialmente, l'elemento con indice 0 si trova nella parte superiore della casella di riepilogo, ma se il contenuto della casella di riepilogo è stato spostato, un altro elemento potrebbe trovarsi nella parte superiore.</span><span class="sxs-lookup"><span data-stu-id="25b76-106">Initially, the item with index 0 is at the top of the list box, but if the list box contents have been scrolled, another item may be at the top.</span></span>

## <a name="parameters"></a><span data-ttu-id="25b76-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="25b76-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25b76-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="25b76-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="25b76-109">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="25b76-109">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="25b76-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="25b76-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="25b76-111">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="25b76-111">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25b76-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="25b76-112">Return value</span></span>

<span data-ttu-id="25b76-113">Se il messaggio ha esito positivo, il valore restituito è l'indice del primo elemento visibile nella casella di riepilogo della casella combinata.</span><span class="sxs-lookup"><span data-stu-id="25b76-113">If the message is successful, the return value is the index of the first visible item in the list box of the combo box.</span></span>

<span data-ttu-id="25b76-114">Se il messaggio ha esito negativo, il valore restituito è CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="25b76-114">If the message fails, the return value is CB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="25b76-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25b76-115">Requirements</span></span>



| <span data-ttu-id="25b76-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="25b76-116">Requirement</span></span> | <span data-ttu-id="25b76-117">Valore</span><span class="sxs-lookup"><span data-stu-id="25b76-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25b76-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25b76-118">Minimum supported client</span></span><br/> | <span data-ttu-id="25b76-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="25b76-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="25b76-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25b76-120">Minimum supported server</span></span><br/> | <span data-ttu-id="25b76-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="25b76-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="25b76-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="25b76-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="25b76-123"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="25b76-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25b76-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="25b76-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25b76-125">**CB \_ SETTOPINDEX**</span><span class="sxs-lookup"><span data-stu-id="25b76-125">**CB\_SETTOPINDEX**</span></span>](cb-settopindex.md)
</dt> </dl>

 

 






---
title: Messaggio CB_SETTOPINDEX (winuser. h)
description: Un'applicazione invia il \_ messaggio SETTOPINDEX CB per assicurarsi che un particolare elemento sia visibile nella casella di riepilogo di una casella combinata.
ms.assetid: vs|controls|~\controls\comboboxes\comboboxreference\comboboxmessages\cb_settopindex.htm
keywords:
- Controlli di Windows Message CB_SETTOPINDEX
topic_type:
- apiref
api_name:
- CB_SETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f402cbd16cd61a829a2221600bd3c548829f348
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740119"
---
# <a name="cb_settopindex-message"></a><span data-ttu-id="7b9b5-104">\_Messaggio SETTOPINDEX CB</span><span class="sxs-lookup"><span data-stu-id="7b9b5-104">CB\_SETTOPINDEX message</span></span>

<span data-ttu-id="7b9b5-105">Un'applicazione invia il **messaggio \_ SETTOPINDEX CB** per assicurarsi che un particolare elemento sia visibile nella casella di riepilogo di una casella combinata.</span><span class="sxs-lookup"><span data-stu-id="7b9b5-105">An application sends the **CB\_SETTOPINDEX** message to ensure that a particular item is visible in the list box of a combo box.</span></span> <span data-ttu-id="7b9b5-106">Il sistema scorre il contenuto della casella di riepilogo in modo che l'elemento specificato venga visualizzato nella parte superiore della casella di riepilogo oppure che sia stato raggiunto l'intervallo massimo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="7b9b5-106">The system scrolls the list box contents so that either the specified item appears at the top of the list box or the maximum scroll range has been reached.</span></span>

## <a name="parameters"></a><span data-ttu-id="7b9b5-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="7b9b5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b9b5-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7b9b5-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7b9b5-109">Specifica l'indice in base zero dell'elemento dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="7b9b5-109">Specifies the zero-based index of the list item.</span></span>

</dd> <dt>

<span data-ttu-id="7b9b5-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7b9b5-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7b9b5-111">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="7b9b5-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b9b5-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7b9b5-112">Return value</span></span>

<span data-ttu-id="7b9b5-113">Se il messaggio ha esito positivo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="7b9b5-113">If the message is successful, the return value is zero.</span></span>

<span data-ttu-id="7b9b5-114">Se il messaggio ha esito negativo, il valore restituito è CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="7b9b5-114">If the message fails, the return value is CB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b9b5-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7b9b5-115">Requirements</span></span>



| <span data-ttu-id="7b9b5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b9b5-116">Requirement</span></span> | <span data-ttu-id="7b9b5-117">Valore</span><span class="sxs-lookup"><span data-stu-id="7b9b5-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b9b5-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b9b5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7b9b5-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7b9b5-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7b9b5-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b9b5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7b9b5-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7b9b5-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7b9b5-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7b9b5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b9b5-123"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7b9b5-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b9b5-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7b9b5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b9b5-125">**CB \_ GETTOPINDEX**</span><span class="sxs-lookup"><span data-stu-id="7b9b5-125">**CB\_GETTOPINDEX**</span></span>](cb-gettopindex.md)
</dt> </dl>

 

 






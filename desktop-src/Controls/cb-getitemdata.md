---
title: Messaggio CB_GETITEMDATA (winuser. h)
description: Un'applicazione invia un \_ messaggio GETITEMDATA CB a una casella combinata per recuperare il valore fornito dall'applicazione associato all'elemento specificato nella casella combinata.
ms.assetid: 433b7f75-2831-4919-b931-c17ba651d145
keywords:
- Controlli di Windows Message CB_GETITEMDATA
topic_type:
- apiref
api_name:
- CB_GETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 643954cf266c52ccbeae082ffacf317c91bc7b33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741455"
---
# <a name="cb_getitemdata-message"></a><span data-ttu-id="3478c-104">\_Messaggio GETITEMDATA CB</span><span class="sxs-lookup"><span data-stu-id="3478c-104">CB\_GETITEMDATA message</span></span>

<span data-ttu-id="3478c-105">Un'applicazione invia un **messaggio \_ GETITEMDATA CB** a una casella combinata per recuperare il valore fornito dall'applicazione associato all'elemento specificato nella casella combinata.</span><span class="sxs-lookup"><span data-stu-id="3478c-105">An application sends a **CB\_GETITEMDATA** message to a combo box to retrieve the application-supplied value associated with the specified item in the combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="3478c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3478c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3478c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3478c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3478c-108">Indice in base zero di un elemento.</span><span class="sxs-lookup"><span data-stu-id="3478c-108">The zero-based index of the item.</span></span>

</dd> <dt>

<span data-ttu-id="3478c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3478c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3478c-110">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="3478c-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3478c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3478c-111">Return value</span></span>

<span data-ttu-id="3478c-112">Il valore restituito è il valore associato all'elemento.</span><span class="sxs-lookup"><span data-stu-id="3478c-112">The return value is the value associated with the item.</span></span> <span data-ttu-id="3478c-113">Se si verifica un errore, è CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="3478c-113">If an error occurs, it is CB\_ERR.</span></span>

<span data-ttu-id="3478c-114">Se l'elemento si trova in una casella combinata creata dal proprietario creata senza lo stile [**CBS \_ HASSTRINGS**](combo-box-styles.md) , il valore restituito è il valore contenuto nel parametro *lParam* del messaggio [**CB \_ ADDSTRING**](cb-addstring.md) o [**CB \_ INSERTSTRING**](cb-insertstring.md) , che ha aggiunto l'elemento alla casella combinata.</span><span class="sxs-lookup"><span data-stu-id="3478c-114">If the item is in an owner-drawn combo box created without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the return value is the value contained in the *lParam* parameter of the [**CB\_ADDSTRING**](cb-addstring.md) or [**CB\_INSERTSTRING**](cb-insertstring.md) message, that added the item to the combo box.</span></span> <span data-ttu-id="3478c-115">Se non è stato usato lo stile **CBS \_ HASSTRINGS** , il valore restituito è il parametro *lParam* contenuto in un messaggio [**CB \_ SETITEMDATA**](cb-setitemdata.md) .</span><span class="sxs-lookup"><span data-stu-id="3478c-115">If the **CBS\_HASSTRINGS** style was not used, the return value is the *lParam* parameter contained in a [**CB\_SETITEMDATA**](cb-setitemdata.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="3478c-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3478c-116">Requirements</span></span>



| <span data-ttu-id="3478c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3478c-117">Requirement</span></span> | <span data-ttu-id="3478c-118">Valore</span><span class="sxs-lookup"><span data-stu-id="3478c-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3478c-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3478c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3478c-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3478c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3478c-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3478c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3478c-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3478c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3478c-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3478c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3478c-124"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3478c-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3478c-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3478c-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="3478c-126">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="3478c-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3478c-127">**CB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="3478c-127">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="3478c-128">**CB \_ INSERTSTRING**</span><span class="sxs-lookup"><span data-stu-id="3478c-128">**CB\_INSERTSTRING**</span></span>](cb-insertstring.md)
</dt> <dt>

[<span data-ttu-id="3478c-129">**CB \_ SETITEMDATA**</span><span class="sxs-lookup"><span data-stu-id="3478c-129">**CB\_SETITEMDATA**</span></span>](cb-setitemdata.md)
</dt> </dl>

 

 






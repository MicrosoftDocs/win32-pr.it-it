---
title: Messaggio CB_SETITEMDATA (winuser. h)
description: Un'applicazione invia un \_ messaggio SETITEMDATA CB per impostare il valore associato all'elemento specificato in una casella combinata.
ms.assetid: 8be9eb57-a635-4c52-9838-556368813c74
keywords:
- Controlli di Windows Message CB_SETITEMDATA
topic_type:
- apiref
api_name:
- CB_SETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbb1603f9906ebf30a391b57bd812dc2002136c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874129"
---
# <a name="cb_setitemdata-message"></a><span data-ttu-id="33c51-104">\_Messaggio SETITEMDATA CB</span><span class="sxs-lookup"><span data-stu-id="33c51-104">CB\_SETITEMDATA message</span></span>

<span data-ttu-id="33c51-105">Un'applicazione invia un **messaggio \_ SETITEMDATA CB** per impostare il valore associato all'elemento specificato in una casella combinata.</span><span class="sxs-lookup"><span data-stu-id="33c51-105">An application sends a **CB\_SETITEMDATA** message to set the value associated with the specified item in a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="33c51-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="33c51-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33c51-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="33c51-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="33c51-108">Specifica l'indice in base zero dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="33c51-108">Specifies the item's zero-based index.</span></span>

</dd> <dt>

<span data-ttu-id="33c51-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="33c51-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="33c51-110">Specifica il nuovo valore da associare all'elemento.</span><span class="sxs-lookup"><span data-stu-id="33c51-110">Specifies the new value to be associated with the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33c51-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="33c51-111">Return value</span></span>

<span data-ttu-id="33c51-112">Se si verifica un errore, il valore restituito è CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="33c51-112">If an error occurs, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="33c51-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="33c51-113">Remarks</span></span>

<span data-ttu-id="33c51-114">Se l'elemento specificato si trova in una casella combinata creata dal proprietario creata senza lo stile [**\_ HASSTRINGS CBS**](combo-box-styles.md) , questo messaggio sostituisce il valore nel parametro *lParam* del messaggio [**CB \_ ADDSTRING**](cb-addstring.md) o [**CB \_ INSERTSTRING**](cb-insertstring.md) che ha aggiunto l'elemento alla casella combinata.</span><span class="sxs-lookup"><span data-stu-id="33c51-114">If the specified item is in an owner-drawn combo box created without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, this message replaces the value in the *lParam* parameter of the [**CB\_ADDSTRING**](cb-addstring.md) or [**CB\_INSERTSTRING**](cb-insertstring.md) message that added the item to the combo box.</span></span>

## <a name="requirements"></a><span data-ttu-id="33c51-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="33c51-115">Requirements</span></span>



| <span data-ttu-id="33c51-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="33c51-116">Requirement</span></span> | <span data-ttu-id="33c51-117">Valore</span><span class="sxs-lookup"><span data-stu-id="33c51-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33c51-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33c51-118">Minimum supported client</span></span><br/> | <span data-ttu-id="33c51-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="33c51-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="33c51-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33c51-120">Minimum supported server</span></span><br/> | <span data-ttu-id="33c51-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="33c51-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="33c51-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="33c51-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="33c51-123"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="33c51-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33c51-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33c51-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="33c51-125">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="33c51-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="33c51-126">**CB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="33c51-126">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="33c51-127">**CB \_ GETITEMDATA**</span><span class="sxs-lookup"><span data-stu-id="33c51-127">**CB\_GETITEMDATA**</span></span>](cb-getitemdata.md)
</dt> <dt>

[<span data-ttu-id="33c51-128">**CB \_ INSERTSTRING**</span><span class="sxs-lookup"><span data-stu-id="33c51-128">**CB\_INSERTSTRING**</span></span>](cb-insertstring.md)
</dt> </dl>

 

 






---
title: Messaggio CBEM_DELETEITEM (COMmctrl. h)
description: Rimuove un elemento da un controllo ComboBoxEx.
ms.assetid: 688cf388-54ba-4b45-88d7-628da49d8615
keywords:
- Controlli di Windows Message CBEM_DELETEITEM
topic_type:
- apiref
api_name:
- CBEM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa3034f79dffabcd7d7aa780582646e17d30b62f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302648"
---
# <a name="cbem_deleteitem-message"></a><span data-ttu-id="d4844-104">\_Messaggio CBEM DeleteItem</span><span class="sxs-lookup"><span data-stu-id="d4844-104">CBEM\_DELETEITEM message</span></span>

<span data-ttu-id="d4844-105">Rimuove un elemento da un controllo ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="d4844-105">Removes an item from a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d4844-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d4844-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4844-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d4844-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d4844-108">Indice in base zero dell'elemento da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="d4844-108">The zero-based index of the item to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="d4844-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d4844-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d4844-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d4844-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4844-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d4844-111">Return value</span></span>

<span data-ttu-id="d4844-112">Restituisce un valore INT che rappresenta il numero di elementi rimanenti nel controllo.</span><span class="sxs-lookup"><span data-stu-id="d4844-112">Returns an INT value that represents the number of items remaining in the control.</span></span> <span data-ttu-id="d4844-113">Se *iIndex* non è valido, il messaggio restituisce CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="d4844-113">If *iIndex* is invalid, the message returns CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4844-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="d4844-114">Remarks</span></span>

<span data-ttu-id="d4844-115">Questo messaggio viene mappato al messaggio di controllo casella combinata [**CB \_ DELETESTRING**](cb-deletestring.md).</span><span class="sxs-lookup"><span data-stu-id="d4844-115">This message maps to the combo box control message [**CB\_DELETESTRING**](cb-deletestring.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d4844-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d4844-116">Requirements</span></span>



| <span data-ttu-id="d4844-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4844-117">Requirement</span></span> | <span data-ttu-id="d4844-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d4844-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d4844-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d4844-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d4844-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d4844-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d4844-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d4844-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d4844-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d4844-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d4844-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d4844-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4844-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4844-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






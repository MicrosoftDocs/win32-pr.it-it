---
title: Messaggio CB_SETCUEBANNER (winuser. h)
description: Imposta il testo del banner cue visualizzato per il controllo di modifica di una casella combinata.
ms.assetid: 4b2b5042-ba64-4e3f-adeb-9aea66773b0e
keywords:
- Controlli di Windows Message CB_SETCUEBANNER
topic_type:
- apiref
api_name:
- CB_SETCUEBANNER
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5799b1b1be5e938ce1e234948a1f7d878122f30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048350"
---
# <a name="cb_setcuebanner-message"></a><span data-ttu-id="ccba2-104">\_Messaggio SETCUEBANNER CB</span><span class="sxs-lookup"><span data-stu-id="ccba2-104">CB\_SETCUEBANNER message</span></span>

<span data-ttu-id="ccba2-105">Imposta il testo del banner cue visualizzato per il controllo di modifica di una casella combinata.</span><span class="sxs-lookup"><span data-stu-id="ccba2-105">Sets the cue banner text that is displayed for the edit control of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="ccba2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ccba2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccba2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ccba2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ccba2-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="ccba2-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ccba2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ccba2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ccba2-110">Puntatore a un buffer di stringa Unicode con terminazione null che contiene il testo.</span><span class="sxs-lookup"><span data-stu-id="ccba2-110">A pointer to a null-terminated Unicode string buffer that contains the text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccba2-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ccba2-111">Return value</span></span>

<span data-ttu-id="ccba2-112">Restituisce 1 se l'operazione ha esito positivo o un valore di errore in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="ccba2-112">Returns 1 if successful, or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccba2-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="ccba2-113">Remarks</span></span>

<span data-ttu-id="ccba2-114">Il banner cue è il testo visualizzato nel controllo di modifica di una casella combinata in assenza di selezione.</span><span class="sxs-lookup"><span data-stu-id="ccba2-114">The cue banner is text that is displayed in the edit control of a combo box when there is no selection.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccba2-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ccba2-115">Requirements</span></span>



| <span data-ttu-id="ccba2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccba2-116">Requirement</span></span> | <span data-ttu-id="ccba2-117">Valore</span><span class="sxs-lookup"><span data-stu-id="ccba2-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccba2-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ccba2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ccba2-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ccba2-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ccba2-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ccba2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ccba2-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ccba2-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ccba2-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ccba2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccba2-123"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccba2-123"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccba2-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ccba2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccba2-125">Funzionalità della casella combinata</span><span class="sxs-lookup"><span data-stu-id="ccba2-125">Combo Box Features</span></span>](combo-box-features.md)
</dt> </dl>

 

 






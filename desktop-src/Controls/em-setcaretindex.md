---
title: Messaggio EM_SETCARETINDEX (CommCtrl. h)
description: Imposta il valore di indice in base zero della posizione del cursore in un controllo di modifica.
ms.assetid: 5cb7ff1e-18e8-49c8-8072-872cf32b18b0
keywords:
- Controlli di Windows Message EM_SETCARETINDEX
topic_type:
- apiref
api_name:
- EM_SETCARETINDEX
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: ea0c49ebad91532e82dc7e96facb62f38b2abfa1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478580"
---
# <a name="em_setcaretindex-message"></a><span data-ttu-id="63aab-104">\_Messaggio SETCARETINDEX em</span><span class="sxs-lookup"><span data-stu-id="63aab-104">EM\_SETCARETINDEX message</span></span>

<span data-ttu-id="63aab-105">Imposta il valore di indice in base zero della posizione del cursore in un controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="63aab-105">Sets the zero-based index value of the position of the caret in an edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="63aab-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="63aab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63aab-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="63aab-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="63aab-108">Nuovo valore di indice in base zero della posizione del cursore.</span><span class="sxs-lookup"><span data-stu-id="63aab-108">The new zero-based index value of the position of the caret.</span></span>

</dd> <dt>

<span data-ttu-id="63aab-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="63aab-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="63aab-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="63aab-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63aab-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="63aab-111">Return value</span></span>

<span data-ttu-id="63aab-112">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="63aab-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="63aab-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="63aab-113">Remarks</span></span>

<span data-ttu-id="63aab-114">Se l'indice non è compreso nell'intervallo del testo in un controllo di modifica, l'indice verrà regolato in modo da adattarsi all'intervallo del testo.</span><span class="sxs-lookup"><span data-stu-id="63aab-114">If the index is out of the range of the text in an edit control, the index will be adjusted to fit inside the range of the text.</span></span>

## <a name="requirements"></a><span data-ttu-id="63aab-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="63aab-115">Requirements</span></span>



| <span data-ttu-id="63aab-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="63aab-116">Requirement</span></span> | <span data-ttu-id="63aab-117">Valore</span><span class="sxs-lookup"><span data-stu-id="63aab-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63aab-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63aab-118">Minimum supported client</span></span><br/> | <span data-ttu-id="63aab-119">Solo app desktop Windows 10, 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="63aab-119">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="63aab-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63aab-120">Minimum supported server</span></span><br/> | <span data-ttu-id="63aab-121">\[Solo app desktop Windows Server 2019\]</span><span class="sxs-lookup"><span data-stu-id="63aab-121">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="63aab-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="63aab-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="63aab-123"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="63aab-123"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63aab-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="63aab-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="63aab-125">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="63aab-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="63aab-126">**\_GETCARETINDEX em**</span><span class="sxs-lookup"><span data-stu-id="63aab-126">**EM\_GETCARETINDEX**</span></span>](em-getcaretindex.md)
</dt> </dl>

 

 






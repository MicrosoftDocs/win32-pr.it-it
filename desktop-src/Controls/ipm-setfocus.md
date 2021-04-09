---
title: Messaggio IPM_SETFOCUS (COMmctrl. h)
description: Imposta lo stato attivo della tastiera sul campo specificato nel controllo degli indirizzi IP. Tutto il testo in tale campo verrà selezionato.
ms.assetid: 4b975eb2-85e1-4e33-a803-99b48d2ff5e8
keywords:
- Controlli di Windows Message IPM_SETFOCUS
topic_type:
- apiref
api_name:
- IPM_SETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d713e0a8b7eb838a2db5c4738c801d4fb76b782
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120291"
---
# <a name="ipm_setfocus-message"></a><span data-ttu-id="58763-105">\_Messaggio di DISattivazione IPM</span><span class="sxs-lookup"><span data-stu-id="58763-105">IPM\_SETFOCUS message</span></span>

<span data-ttu-id="58763-106">Imposta lo stato attivo della tastiera sul campo specificato nel controllo degli indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="58763-106">Sets the keyboard focus to the specified field in the IP address control.</span></span> <span data-ttu-id="58763-107">Tutto il testo in tale campo verrà selezionato.</span><span class="sxs-lookup"><span data-stu-id="58763-107">All of the text in that field will be selected.</span></span>

## <a name="parameters"></a><span data-ttu-id="58763-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="58763-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58763-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="58763-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="58763-110">Indice di campo in base zero in cui impostare lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="58763-110">A zero-based field index to which the focus should be set.</span></span> <span data-ttu-id="58763-111">Se questo valore è maggiore del numero di campi, lo stato attivo è impostato sul primo campo vuoto.</span><span class="sxs-lookup"><span data-stu-id="58763-111">If this value is greater than the number of fields, focus is set to the first blank field.</span></span> <span data-ttu-id="58763-112">Se tutti i campi non sono vuoti, lo stato attivo è impostato sul primo campo.</span><span class="sxs-lookup"><span data-stu-id="58763-112">If all fields are nonblank, focus is set to the first field.</span></span>

</dd> <dt>

<span data-ttu-id="58763-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="58763-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="58763-114">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="58763-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58763-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="58763-115">Return value</span></span>

<span data-ttu-id="58763-116">Il valore restituito non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="58763-116">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="58763-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="58763-117">Requirements</span></span>



| <span data-ttu-id="58763-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="58763-118">Requirement</span></span> | <span data-ttu-id="58763-119">Valore</span><span class="sxs-lookup"><span data-stu-id="58763-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="58763-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="58763-120">Minimum supported client</span></span><br/> | <span data-ttu-id="58763-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="58763-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="58763-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="58763-122">Minimum supported server</span></span><br/> | <span data-ttu-id="58763-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="58763-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="58763-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="58763-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="58763-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="58763-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






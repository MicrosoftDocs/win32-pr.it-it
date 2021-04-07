---
title: Messaggio di EM_GETIMEMODEBIAS (RichEdit. h)
description: Recupera la distorsione della modalità IME (Input Method Editor) per un controllo Rich Edit di Microsoft.
ms.assetid: e8ca899f-3423-4814-86e9-133dfd11f9a6
keywords:
- Controlli di Windows Message EM_GETIMEMODEBIAS
topic_type:
- apiref
api_name:
- EM_GETIMEMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea13e151ae9d487340ee440e3b123ae70b437a02
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048560"
---
# <a name="em_getimemodebias-message"></a><span data-ttu-id="f906b-104">\_Messaggio GETIMEMODEBIAS em</span><span class="sxs-lookup"><span data-stu-id="f906b-104">EM\_GETIMEMODEBIAS message</span></span>

<span data-ttu-id="f906b-105">Recupera la distorsione della modalità IME (Input Method Editor) per un controllo Rich Edit di Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f906b-105">Retrieves the Input Method Editor (IME) mode bias for a Microsoft Rich Edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f906b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f906b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f906b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f906b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f906b-108">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="f906b-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f906b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f906b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f906b-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="f906b-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f906b-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f906b-111">Return value</span></span>

<span data-ttu-id="f906b-112">Questo messaggio restituisce l'impostazione di distorsione della modalità IME corrente.</span><span class="sxs-lookup"><span data-stu-id="f906b-112">This message returns the current IME mode bias setting.</span></span>

## <a name="remarks"></a><span data-ttu-id="f906b-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="f906b-113">Remarks</span></span>

<span data-ttu-id="f906b-114">Per ottenere la distorsione della modalità del Framework dei servizi di testo, usare [**em \_ GETCTFMODEBIAS**](em-getctfmodebias.md).</span><span class="sxs-lookup"><span data-stu-id="f906b-114">To get the Text Services Framework mode bias, use [**EM\_GETCTFMODEBIAS**](em-getctfmodebias.md).</span></span>

<span data-ttu-id="f906b-115">Prima di chiamare questa funzione, l'applicazione deve chiamare [**em \_ ISIME**](em-isime.md) .</span><span class="sxs-lookup"><span data-stu-id="f906b-115">The application should call [**EM\_ISIME**](em-isime.md) before calling this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f906b-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f906b-116">Requirements</span></span>



| <span data-ttu-id="f906b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f906b-117">Requirement</span></span> | <span data-ttu-id="f906b-118">Valore</span><span class="sxs-lookup"><span data-stu-id="f906b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f906b-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f906b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f906b-120">Solo app desktop Windows XP con SP1 \[\]</span><span class="sxs-lookup"><span data-stu-id="f906b-120">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f906b-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f906b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f906b-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f906b-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f906b-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f906b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f906b-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f906b-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f906b-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f906b-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="f906b-126">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="f906b-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f906b-127">**\_ISIME em**</span><span class="sxs-lookup"><span data-stu-id="f906b-127">**EM\_ISIME**</span></span>](em-isime.md)
</dt> <dt>

[<span data-ttu-id="f906b-128">**\_GETCTFMODEBIAS em**</span><span class="sxs-lookup"><span data-stu-id="f906b-128">**EM\_GETCTFMODEBIAS**</span></span>](em-getctfmodebias.md)
</dt> </dl>

 

 






---
title: Messaggio EM_SEARCHWEB (COMmctrl. h)
description: Apre il browser ed esegue una ricerca Web con il testo selezionato come termine di ricerca.
ms.assetid: 1b1ff5e7-e0b8-40c1-8b7e-7003e9ef959b
keywords:
- Controlli di Windows Message EM_SEARCHWEB
topic_type:
- apiref
api_name:
- EM_SEARCHWEB
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2e83c18db47d18648797ee3d58fe12567af941b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874270"
---
# <a name="em_searchweb-message"></a><span data-ttu-id="d9fad-104">\_Messaggio SEARCHWEB em</span><span class="sxs-lookup"><span data-stu-id="d9fad-104">EM\_SEARCHWEB message</span></span>

<span data-ttu-id="d9fad-105">Apre il browser ed esegue una ricerca Web con il testo selezionato come termine di ricerca.</span><span class="sxs-lookup"><span data-stu-id="d9fad-105">Opens the browser and performs a web search with the selected text as the search term.</span></span>

## <a name="parameters"></a><span data-ttu-id="d9fad-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d9fad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9fad-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d9fad-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d9fad-108">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d9fad-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d9fad-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d9fad-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d9fad-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d9fad-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9fad-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d9fad-111">Return value</span></span>

<span data-ttu-id="d9fad-112">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="d9fad-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9fad-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="d9fad-113">Remarks</span></span>

<span data-ttu-id="d9fad-114">Se la funzionalità "Cerca sul Web" è disabilitata usando il messaggio [**\_ ENABLESEARCHWEB em**](em-enablesearchweb.md) , questo messaggio non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="d9fad-114">If the "Search the web" feature is disabled using the [**EM\_ENABLESEARCHWEB**](em-enablesearchweb.md) message, this message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9fad-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d9fad-115">Requirements</span></span>



| <span data-ttu-id="d9fad-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9fad-116">Requirement</span></span> | <span data-ttu-id="d9fad-117">Valore</span><span class="sxs-lookup"><span data-stu-id="d9fad-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d9fad-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9fad-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d9fad-119">Solo app desktop Windows 10, 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="d9fad-119">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d9fad-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9fad-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d9fad-121">\[Solo app desktop Windows Server 2019\]</span><span class="sxs-lookup"><span data-stu-id="d9fad-121">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d9fad-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d9fad-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9fad-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9fad-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9fad-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d9fad-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9fad-125">**\_ENABLESEARCHWEB em**</span><span class="sxs-lookup"><span data-stu-id="d9fad-125">**EM\_ENABLESEARCHWEB**</span></span>](em-enablesearchweb.md)
</dt> </dl>

 

 






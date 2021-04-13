---
title: Metodo DVD. back
description: Il metodo back restituisce la visualizzazione da un sottomenu al relativo menu padre.
ms.assetid: 4b6c3562-6484-4ef0-8c5c-c24d88e02096
keywords:
- Back metodo Windows Media Player
- Back metodo Windows Media Player, classe DVD
- Classe DVD Media Player Windows, metodo back
topic_type:
- apiref
api_name:
- DVD.back
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e656051d02ec5efc74aa7595d2ca6cb20e648f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400628"
---
# <a name="dvdback-method"></a><span data-ttu-id="4b294-106">Metodo DVD. back</span><span class="sxs-lookup"><span data-stu-id="4b294-106">DVD.back method</span></span>

<span data-ttu-id="4b294-107">Il metodo **back** restituisce la visualizzazione da un sottomenu al relativo menu padre.</span><span class="sxs-lookup"><span data-stu-id="4b294-107">The **back** method returns the display from a submenu to its parent menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b294-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4b294-108">Syntax</span></span>


```JScript
DVD.back()
```



## <a name="parameters"></a><span data-ttu-id="4b294-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="4b294-109">Parameters</span></span>

<span data-ttu-id="4b294-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="4b294-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4b294-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4b294-111">Return value</span></span>

<span data-ttu-id="4b294-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="4b294-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b294-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="4b294-113">Remarks</span></span>

<span data-ttu-id="4b294-114">Ogni DVD viene creato in modo diverso.</span><span class="sxs-lookup"><span data-stu-id="4b294-114">Every DVD is authored differently.</span></span> <span data-ttu-id="4b294-115">Alcuni DVD vengono creati in modo che il metodo **back** sia disponibile dal menu radice, ma quando viene richiamato, non eseguirà alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="4b294-115">Some DVDs are authored so that the **back** method is available from the root menu, but when invoked, it will do nothing.</span></span>

<span data-ttu-id="4b294-116">**Windows Media Player 10 Mobile:** Questo metodo ha sempre esito positivo, ma non esegue l'operazione desiderata.</span><span class="sxs-lookup"><span data-stu-id="4b294-116">**Windows Media Player 10 Mobile:** This method always succeeds, but does not perform the intended operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b294-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4b294-117">Requirements</span></span>



| <span data-ttu-id="4b294-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b294-118">Requirement</span></span> | <span data-ttu-id="4b294-119">Valore</span><span class="sxs-lookup"><span data-stu-id="4b294-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4b294-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b294-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4b294-121">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4b294-121">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4b294-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b294-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4b294-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4b294-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4b294-124">Versione</span><span class="sxs-lookup"><span data-stu-id="4b294-124">Version</span></span><br/>                  | <span data-ttu-id="4b294-125">Windows Media Player per Windows XP o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="4b294-125">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="4b294-126">DLL</span><span class="sxs-lookup"><span data-stu-id="4b294-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b294-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b294-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b294-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4b294-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b294-129">**Oggetto DVD**</span><span class="sxs-lookup"><span data-stu-id="4b294-129">**DVD Object**</span></span>](dvd-object.md)
</dt> </dl>

 

 






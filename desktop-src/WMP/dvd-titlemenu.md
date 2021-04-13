---
title: DVD. titleMenu, metodo
description: Il metodo titleMenu interrompe la riproduzione del titolo e visualizza il menu del titolo.
ms.assetid: 3be3e7cd-5969-4051-ae63-ff070a19fe51
keywords:
- Metodo titleMenu Windows Media Player
- Metodo titleMenu Windows Media Player, classe DVD
- Classe DVD Media Player Windows, metodo titleMenu
topic_type:
- apiref
api_name:
- DVD.titleMenu
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9351603d5307415f57610422a83d3586067bdcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340592"
---
# <a name="dvdtitlemenu-method"></a><span data-ttu-id="14b8c-106">DVD. titleMenu, metodo</span><span class="sxs-lookup"><span data-stu-id="14b8c-106">DVD.titleMenu method</span></span>

<span data-ttu-id="14b8c-107">Il metodo **titleMenu** interrompe la riproduzione del titolo e visualizza il menu del titolo.</span><span class="sxs-lookup"><span data-stu-id="14b8c-107">The **titleMenu** method stops title playback and displays the title menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="14b8c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="14b8c-108">Syntax</span></span>


```JScript
DVD.titleMenu()
```



## <a name="parameters"></a><span data-ttu-id="14b8c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="14b8c-109">Parameters</span></span>

<span data-ttu-id="14b8c-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="14b8c-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="14b8c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="14b8c-111">Return value</span></span>

<span data-ttu-id="14b8c-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="14b8c-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="14b8c-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="14b8c-113">Remarks</span></span>

<span data-ttu-id="14b8c-114">Ogni DVD viene creato in modo diverso.</span><span class="sxs-lookup"><span data-stu-id="14b8c-114">Every DVD is authored differently.</span></span> <span data-ttu-id="14b8c-115">Il DVD deve contenere un menu per il funzionamento di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="14b8c-115">The DVD must contain a menu for this method to work.</span></span> <span data-ttu-id="14b8c-116">Alcuni DVD vengono creati in modo che i metodi **tomenu** e **titleMenu** aprano lo stesso menu.</span><span class="sxs-lookup"><span data-stu-id="14b8c-116">Some DVDs are authored so that the **topMenu** and **titleMenu** methods open the same menu.</span></span> <span data-ttu-id="14b8c-117">Il metodo **titleMenu** richiama in genere il menu del titolo, ma può richiamare invece il menu superiore se non è disponibile alcun menu titolo.</span><span class="sxs-lookup"><span data-stu-id="14b8c-117">The **titleMenu** method usually invokes the title menu but it may invoke the top menu instead, if there is no title menu available.</span></span>

<span data-ttu-id="14b8c-118">**Windows Media Player 10 Mobile:** Questo metodo ha sempre esito positivo, ma non esegue l'operazione desiderata.</span><span class="sxs-lookup"><span data-stu-id="14b8c-118">**Windows Media Player 10 Mobile:** This method always succeeds, but does not perform the intended operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="14b8c-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14b8c-119">Requirements</span></span>



| <span data-ttu-id="14b8c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="14b8c-120">Requirement</span></span> | <span data-ttu-id="14b8c-121">Valore</span><span class="sxs-lookup"><span data-stu-id="14b8c-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="14b8c-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14b8c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="14b8c-123">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="14b8c-123">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="14b8c-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14b8c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="14b8c-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="14b8c-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="14b8c-126">Versione</span><span class="sxs-lookup"><span data-stu-id="14b8c-126">Version</span></span><br/>                  | <span data-ttu-id="14b8c-127">Windows Media Player per Windows XP o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="14b8c-127">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="14b8c-128">DLL</span><span class="sxs-lookup"><span data-stu-id="14b8c-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14b8c-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14b8c-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14b8c-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="14b8c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14b8c-131">**Oggetto DVD**</span><span class="sxs-lookup"><span data-stu-id="14b8c-131">**DVD Object**</span></span>](dvd-object.md)
</dt> <dt>

[<span data-ttu-id="14b8c-132">**DVD. menu di scelta rapida**</span><span class="sxs-lookup"><span data-stu-id="14b8c-132">**DVD.topMenu**</span></span>](dvd-topmenu.md)
</dt> </dl>

 

 






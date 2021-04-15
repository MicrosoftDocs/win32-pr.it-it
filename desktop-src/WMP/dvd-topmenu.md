---
title: DVD. tomenu (metodo)
description: Il metodo di menu di scelta rapida interrompe la riproduzione del titolo e visualizza il menu principale (o radice) per il titolo corrente.
ms.assetid: 9998e8d1-e5e7-4003-bf27-da319a1a3058
keywords:
- Windows Media Player metodo di menu di scelta rapida
- Metodo di menu di scelta rapida Windows Media Player, classe DVD
- Classe DVD Media Player Windows, metodo tomenu
topic_type:
- apiref
api_name:
- DVD.topMenu
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2be2b0fdafb10039b24f1d77e65f4b105889da85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477380"
---
# <a name="dvdtopmenu-method"></a><span data-ttu-id="e44bd-106">DVD. tomenu (metodo)</span><span class="sxs-lookup"><span data-stu-id="e44bd-106">DVD.topMenu method</span></span>

<span data-ttu-id="e44bd-107">Il metodo di **menu di scelta rapida** interrompe la riproduzione del titolo e visualizza il menu principale (o radice) per il titolo corrente.</span><span class="sxs-lookup"><span data-stu-id="e44bd-107">The **topMenu** method stops title playback and displays the top (or root) menu for the current title.</span></span>

## <a name="syntax"></a><span data-ttu-id="e44bd-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e44bd-108">Syntax</span></span>


```JScript
DVD.topMenu()
```



## <a name="parameters"></a><span data-ttu-id="e44bd-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e44bd-109">Parameters</span></span>

<span data-ttu-id="e44bd-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="e44bd-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e44bd-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e44bd-111">Return value</span></span>

<span data-ttu-id="e44bd-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="e44bd-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e44bd-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="e44bd-113">Remarks</span></span>

<span data-ttu-id="e44bd-114">Ogni DVD viene creato in modo diverso.</span><span class="sxs-lookup"><span data-stu-id="e44bd-114">Every DVD is authored differently.</span></span> <span data-ttu-id="e44bd-115">Il DVD deve contenere un menu per il funzionamento di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="e44bd-115">The DVD must contain a menu for this method to work.</span></span> <span data-ttu-id="e44bd-116">Alcuni DVD vengono creati in modo che i metodi **tomenu** e **titleMenu** aprano lo stesso menu.</span><span class="sxs-lookup"><span data-stu-id="e44bd-116">Some DVDs are authored so that the **topMenu** and **titleMenu** methods open the same menu.</span></span> <span data-ttu-id="e44bd-117">Il metodo di **menu di scelta rapida** richiama in genere il menu superiore (o radice), ma può invece richiamare il menu del titolo, se non è disponibile alcun menu radice.</span><span class="sxs-lookup"><span data-stu-id="e44bd-117">The **topMenu** method usually invokes the top (or root) menu but it may invoke the title menu instead, if there is no root menu available.</span></span>

<span data-ttu-id="e44bd-118">**Windows Media Player 10 Mobile:** Questo metodo ha sempre esito positivo, ma non esegue l'operazione desiderata.</span><span class="sxs-lookup"><span data-stu-id="e44bd-118">**Windows Media Player 10 Mobile:** This method always succeeds, but does not perform the intended operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="e44bd-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e44bd-119">Requirements</span></span>



| <span data-ttu-id="e44bd-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e44bd-120">Requirement</span></span> | <span data-ttu-id="e44bd-121">Valore</span><span class="sxs-lookup"><span data-stu-id="e44bd-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e44bd-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e44bd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e44bd-123">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e44bd-123">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e44bd-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e44bd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e44bd-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e44bd-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e44bd-126">Versione</span><span class="sxs-lookup"><span data-stu-id="e44bd-126">Version</span></span><br/>                  | <span data-ttu-id="e44bd-127">Windows Media Player per Windows XP o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="e44bd-127">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="e44bd-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e44bd-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e44bd-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e44bd-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e44bd-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e44bd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e44bd-131">**Oggetto DVD**</span><span class="sxs-lookup"><span data-stu-id="e44bd-131">**DVD Object**</span></span>](dvd-object.md)
</dt> <dt>

[<span data-ttu-id="e44bd-132">**DVD. titleMenu**</span><span class="sxs-lookup"><span data-stu-id="e44bd-132">**DVD.titleMenu**</span></span>](dvd-titlemenu.md)
</dt> </dl>

 

 






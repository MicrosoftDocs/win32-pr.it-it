---
title: External. cancelNavigate, metodo
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. | External. cancelNavigate, metodo
ms.assetid: e65d64fb-292c-4413-9727-b24609e78d68
keywords:
- Metodo cancelNavigate Windows Media Player
- Metodo cancelNavigate Windows Media Player, classe esterna
- Classe esterna Media Player Windows, metodo cancelNavigate
topic_type:
- apiref
api_name:
- External.cancelNavigate
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55a6cbc0f749fd6ca33d78dfaed1d256634eb9c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331237"
---
# <a name="externalcancelnavigate-method"></a><span data-ttu-id="eec26-107">External. cancelNavigate, metodo</span><span class="sxs-lookup"><span data-stu-id="eec26-107">External.cancelNavigate method</span></span>

> [!Note]  
> <span data-ttu-id="eec26-108">Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online.</span><span class="sxs-lookup"><span data-stu-id="eec26-108">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="eec26-109">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="eec26-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="eec26-110">Il metodo **cancelNavigate** informa Windows Media Player che non dovrebbe visualizzare una nuova pagina di individuazione anche se la visualizzazione è cambiata nel lettore.</span><span class="sxs-lookup"><span data-stu-id="eec26-110">The **cancelNavigate** method informs Windows Media Player that it should not display a new discovery page even though the view has changed in the Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="eec26-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eec26-111">Syntax</span></span>


```JScript
External.cancelNavigate()
```



## <a name="parameters"></a><span data-ttu-id="eec26-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="eec26-112">Parameters</span></span>

<span data-ttu-id="eec26-113">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="eec26-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="eec26-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eec26-114">Return value</span></span>

<span data-ttu-id="eec26-115">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="eec26-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eec26-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="eec26-116">Remarks</span></span>

<span data-ttu-id="eec26-117">Quando la visualizzazione cambia in Windows Media Player, il lettore chiama il plug-in Online Store per determinare la pagina di individuazione da visualizzare successivamente.</span><span class="sxs-lookup"><span data-stu-id="eec26-117">When the view changes in Windows Media Player, the Player calls the online store's plug-in to determine which discovery page to display next.</span></span> <span data-ttu-id="eec26-118">In alcuni casi, tuttavia, l'archivio online potrebbe volere che il lettore continui a visualizzare la pagina di individuazione esistente.</span><span class="sxs-lookup"><span data-stu-id="eec26-118">In some cases, however, the online store might want the Player to continue displaying the existing discovery page.</span></span> <span data-ttu-id="eec26-119">Il processo seguente determina se il lettore Visualizza una nuova pagina di individuazione:</span><span class="sxs-lookup"><span data-stu-id="eec26-119">The following process determines whether the Player displays a new discovery page:</span></span>

1.  <span data-ttu-id="eec26-120">Un'azione da parte dell'utente, nell'interfaccia utente del lettore o nella pagina di individuazione, richiede che il lettore modifichi la propria visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="eec26-120">An action by the user, either in the Player's user interface or on the discovery page, requests that the Player change its view.</span></span>
2.  <span data-ttu-id="eec26-121">Il lettore chiama il metodo [GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) del plug-in per determinare la pagina di individuazione da visualizzare successivamente.</span><span class="sxs-lookup"><span data-stu-id="eec26-121">The Player calls the plug-in's [GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) method to determine which discovery page to display next.</span></span> <span data-ttu-id="eec26-122">Il lettore archivia l'URL della nuova pagina di individuazione, ma non Visualizza la nuova pagina di individuazione in questo momento.</span><span class="sxs-lookup"><span data-stu-id="eec26-122">The Player stores the URL of the new discovery page but does not display the new discovery page at this time.</span></span>
3.  <span data-ttu-id="eec26-123">Il lettore genera l'evento [OnViewChange](external-onviewchange-event.md) .</span><span class="sxs-lookup"><span data-stu-id="eec26-123">The Player raises the [OnViewChange](external-onviewchange-event.md) event.</span></span>
4.  <span data-ttu-id="eec26-124">Se il gestore dell'evento **OnViewChange** nella pagina di individuazione chiama **CancelNavigate**, il lettore non Visualizza la nuova pagina di individuazione (determinata nel passaggio 2).</span><span class="sxs-lookup"><span data-stu-id="eec26-124">If the **OnViewChange** event handler on the discovery page calls **cancelNavigate**, the Player does not display the new discovery page (determined in step 2).</span></span> <span data-ttu-id="eec26-125">Ma continua a visualizzare la pagina di individuazione esistente.</span><span class="sxs-lookup"><span data-stu-id="eec26-125">Instead, it continues to display the existing discovery page.</span></span> <span data-ttu-id="eec26-126">Se il gestore dell'evento **OnViewChange** non chiama **CancelNavigate**, il lettore Visualizza la nuova pagina di individuazione.</span><span class="sxs-lookup"><span data-stu-id="eec26-126">If the **OnViewChange** event handler does not call **cancelNavigate**, the Player does display the new discovery page.</span></span>

<span data-ttu-id="eec26-127">Si supponga, ad esempio, che il lettore stia visualizzando la visualizzazione di un album con una certa traccia selezionata.</span><span class="sxs-lookup"><span data-stu-id="eec26-127">For example, suppose the Player is currently displaying the view of an album with a certain track selected.</span></span> <span data-ttu-id="eec26-128">Si supponga inoltre che la pagina di individuazione corrente sia la pagina che rappresenta l'intero album.</span><span class="sxs-lookup"><span data-stu-id="eec26-128">Also assume that the current discovery page is the page that represents the entire album.</span></span> <span data-ttu-id="eec26-129">Se l'utente fa clic su una traccia diversa dallo stesso album, la visualizzazione del giocatore cambia leggermente per indicare che la nuova traccia è selezionata.</span><span class="sxs-lookup"><span data-stu-id="eec26-129">If the user clicks a different track from the same album, the Player's view changes slightly to show that the new track is selected.</span></span> <span data-ttu-id="eec26-130">Non è tuttavia necessario visualizzare una nuova pagina di individuazione.</span><span class="sxs-lookup"><span data-stu-id="eec26-130">But there is no need to display a new discovery page.</span></span> <span data-ttu-id="eec26-131">La pagina di individuazione che rappresenta l'intero album è ancora la pagina appropriata per la visualizzazione del lettore.</span><span class="sxs-lookup"><span data-stu-id="eec26-131">The discovery page that represents the entire album is still the appropriate page for the Player to display.</span></span>

## <a name="requirements"></a><span data-ttu-id="eec26-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eec26-132">Requirements</span></span>



| <span data-ttu-id="eec26-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="eec26-133">Requirement</span></span> | <span data-ttu-id="eec26-134">Valore</span><span class="sxs-lookup"><span data-stu-id="eec26-134">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="eec26-135">Versione</span><span class="sxs-lookup"><span data-stu-id="eec26-135">Version</span></span><br/> | <span data-ttu-id="eec26-136">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="eec26-136">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="eec26-137">DLL</span><span class="sxs-lookup"><span data-stu-id="eec26-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="eec26-138"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eec26-138"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eec26-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eec26-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eec26-140">**Oggetto esterno per i negozi di tipo 1 online**</span><span class="sxs-lookup"><span data-stu-id="eec26-140">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="eec26-141">**External. changeViewOnlineList**</span><span class="sxs-lookup"><span data-stu-id="eec26-141">**External.changeViewOnlineList**</span></span>](external-changeviewonlinelist.md)
</dt> <dt>

[<span data-ttu-id="eec26-142">**External. OnViewChange**</span><span class="sxs-lookup"><span data-stu-id="eec26-142">**External.OnViewChange**</span></span>](external-onviewchange-event.md)
</dt> </dl>

 

 






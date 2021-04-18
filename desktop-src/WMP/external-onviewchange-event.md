---
title: Evento External. OnViewChange
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. L'evento OnViewChange si verifica quando la visualizzazione cambia in Windows Media Player.
ms.assetid: aa1378ad-8b84-4592-85c5-5e284be05ea6
keywords:
- Media Player di Windows dell'evento External. OnViewChange
topic_type:
- apiref
api_name:
- External.OnViewChange Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c7144e03955fb67ed90cad4a4336bf782ca1566
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324555"
---
# <a name="externalonviewchange-event"></a><span data-ttu-id="7b984-106">Evento External. OnViewChange</span><span class="sxs-lookup"><span data-stu-id="7b984-106">External.OnViewChange Event</span></span>

> [!Note]  
> <span data-ttu-id="7b984-107">Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online.</span><span class="sxs-lookup"><span data-stu-id="7b984-107">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="7b984-108">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="7b984-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="7b984-109">L'evento **OnViewChange** si verifica quando la visualizzazione cambia in Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="7b984-109">The **OnViewChange** event occurs when the view changes in Windows Media Player.</span></span>

``` syntax
window.external.OnViewChange = FunctionName
```

## <a name="possible-values"></a><span data-ttu-id="7b984-110">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="7b984-110">Possible Values</span></span>

<span data-ttu-id="7b984-111">Si tratta di una proprietà di sola scrittura che specifica il nome della funzione nello script che Windows Media Player chiama quando si verifica l'evento.</span><span class="sxs-lookup"><span data-stu-id="7b984-111">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="7b984-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="7b984-112">Parameters</span></span>

<span data-ttu-id="7b984-113">La funzione che gestisce questo evento non accetta parametri.</span><span class="sxs-lookup"><span data-stu-id="7b984-113">The function that handles this event takes no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b984-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="7b984-114">Remarks</span></span>

<span data-ttu-id="7b984-115">La visualizzazione in Windows Media Player può variare per uno dei seguenti motivi:</span><span class="sxs-lookup"><span data-stu-id="7b984-115">The view in Windows Media Player can change for any of the following reasons:</span></span>

-   <span data-ttu-id="7b984-116">L'utente interagisce con l'interfaccia utente di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="7b984-116">The user interacts with the Windows Media Player user interface.</span></span>
-   <span data-ttu-id="7b984-117">L'utente interagisce con una pagina di individuazione e lo script nella pagina di individuazione chiama [External. changeView](external-changeview.md).</span><span class="sxs-lookup"><span data-stu-id="7b984-117">The user interacts with a discovery page, and script on the discovery page calls [External.changeView](external-changeview.md).</span></span>
-   <span data-ttu-id="7b984-118">L'utente interagisce con una pagina di individuazione e lo script nella pagina di individuazione chiama [External. changeViewOnlineList](external-changeviewonlinelist.md).</span><span class="sxs-lookup"><span data-stu-id="7b984-118">The user interacts with a discovery page, and script on the discovery page calls [External.changeViewOnlineList](external-changeviewonlinelist.md).</span></span>

<span data-ttu-id="7b984-119">Quando la visualizzazione cambia in Windows Media Player, il lettore chiama [IWMPContentPartner:: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) per ottenere l'URL della pagina di individuazione successiva da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="7b984-119">When the view changes in Windows Media Player, the Player calls [IWMPContentPartner::GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) to get the URL of the next discovery page to display.</span></span> <span data-ttu-id="7b984-120">Tuttavia, prima che il lettore visualizzi la nuova pagina di individuazione, genera l'evento **OnViewChange** .</span><span class="sxs-lookup"><span data-stu-id="7b984-120">However, before the Player displays the new discovery page, it raises the **OnViewChange** event.</span></span> <span data-ttu-id="7b984-121">Se il gestore dell'evento **OnViewChange** chiama [External. cancelNavigate](external-cancelnavigate.md), Windows Media Player non Visualizza la nuova pagina di individuazione.</span><span class="sxs-lookup"><span data-stu-id="7b984-121">If the **OnViewChange** event handler calls [External.cancelNavigate](external-cancelnavigate.md), Windows Media Player does not display the new discovery page.</span></span> <span data-ttu-id="7b984-122">Ma continua a visualizzare la pagina di individuazione corrente.</span><span class="sxs-lookup"><span data-stu-id="7b984-122">Instead, it continues to display the current discovery page.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b984-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7b984-123">Requirements</span></span>



| <span data-ttu-id="7b984-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b984-124">Requirement</span></span> | <span data-ttu-id="7b984-125">Valore</span><span class="sxs-lookup"><span data-stu-id="7b984-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7b984-126">Versione</span><span class="sxs-lookup"><span data-stu-id="7b984-126">Version</span></span><br/> | <span data-ttu-id="7b984-127">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="7b984-127">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="7b984-128">DLL</span><span class="sxs-lookup"><span data-stu-id="7b984-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="7b984-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b984-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b984-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7b984-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b984-131">**Oggetto esterno per i negozi di tipo 1 online**</span><span class="sxs-lookup"><span data-stu-id="7b984-131">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="7b984-132">**External. changeView**</span><span class="sxs-lookup"><span data-stu-id="7b984-132">**External.changeView**</span></span>](external-changeview.md)
</dt> <dt>

[<span data-ttu-id="7b984-133">**External. changeViewOnlineList**</span><span class="sxs-lookup"><span data-stu-id="7b984-133">**External.changeViewOnlineList**</span></span>](external-changeviewonlinelist.md)
</dt> </dl>

 

 






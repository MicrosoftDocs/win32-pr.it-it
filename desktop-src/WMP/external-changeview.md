---
title: External. changeView, metodo
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. Il metodo changeView modifica la visualizzazione in Windows Media Player.
ms.assetid: bd9d7d4b-ee4c-4d7c-92ef-dd0b8ab46d9d
keywords:
- Metodo changeView Windows Media Player
- Metodo changeView Windows Media Player, classe esterna
- Classe esterna Media Player Windows, metodo changeView
topic_type:
- apiref
api_name:
- External.changeView
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35adb253d5dd14d755353c29f9278b1c122133d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324570"
---
# <a name="externalchangeview-method"></a><span data-ttu-id="900e6-108">External. changeView, metodo</span><span class="sxs-lookup"><span data-stu-id="900e6-108">External.changeView method</span></span>

> [!Note]  
> <span data-ttu-id="900e6-109">Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online.</span><span class="sxs-lookup"><span data-stu-id="900e6-109">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="900e6-110">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="900e6-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="900e6-111">Il metodo **changeView** modifica la visualizzazione in Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="900e6-111">The **changeView** method changes the view in Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="900e6-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="900e6-112">Syntax</span></span>


```JScript
External.changeView(
  LibraryLocationType,
  LibraryLocationID,
  Filter,
  ViewParams
)
```



## <a name="parameters"></a><span data-ttu-id="900e6-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="900e6-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="900e6-114">*LibraryLocationType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="900e6-114">*LibraryLocationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="900e6-115">[Costante del percorso della libreria](library-location-constants.md) che specifica il tipo della nuova visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="900e6-115">A [library location constant](library-location-constants.md) that specifies the type of the new view.</span></span> <span data-ttu-id="900e6-116">Ad esempio, la costante CPGenreID specifica che la nuova vista mostrerà un genere particolare.</span><span class="sxs-lookup"><span data-stu-id="900e6-116">For example, the constant CPGenreID specifies that the new view will show a particular genre.</span></span>

</dd> <dt>

<span data-ttu-id="900e6-117">*LibraryLocationID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="900e6-117">*LibraryLocationID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="900e6-118">**Stringa** contenente l'ID dell'elemento specifico da visualizzare nella nuova visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="900e6-118">**String** containing the ID of the specific item to show in the new view.</span></span> <span data-ttu-id="900e6-119">Ad esempio, se *LibraryLocationType* è CPGenreID, questo parametro specifica l'ID del genere da visualizzare nella nuova visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="900e6-119">For example, if *LibraryLocationType* is CPGenreID, then this parameter specifies the ID of the genre to show in the new view.</span></span> <span data-ttu-id="900e6-120">Questa stringa può essere vuota.</span><span class="sxs-lookup"><span data-stu-id="900e6-120">This string can be empty.</span></span> <span data-ttu-id="900e6-121">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="900e6-121">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="900e6-122">*Filtro* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="900e6-122">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="900e6-123">**Stringa** contenente il filtro per la nuova visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="900e6-123">**String** containing the filter for the new view.</span></span> <span data-ttu-id="900e6-124">La vista verrà filtrata come se l'utente avesse immesso il testo nel controllo rotellina della parola del giocatore.</span><span class="sxs-lookup"><span data-stu-id="900e6-124">The view will be filtered as if the user had entered this text in the Player's word wheel control.</span></span> <span data-ttu-id="900e6-125">Questa stringa può essere vuota.</span><span class="sxs-lookup"><span data-stu-id="900e6-125">This string can be empty.</span></span>

</dd> <dt>

<span data-ttu-id="900e6-126">*ViewParams* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="900e6-126">*ViewParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="900e6-127">**Stringa** contenente i parametri resi disponibili da Windows Media Player alla nuova pagina di individuazione visualizzata con la nuova visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="900e6-127">**String** containing parameters that Windows Media Player makes available to the new discovery page that is displayed with the new view.</span></span> <span data-ttu-id="900e6-128">Questi parametri non vengono interpretati da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="900e6-128">These parameters are not interpreted by Windows Media Player.</span></span> <span data-ttu-id="900e6-129">Vengono creati dal negozio online e hanno un significato solo per lo Store online.</span><span class="sxs-lookup"><span data-stu-id="900e6-129">They are created by the online store and have meaning only to the online store.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="900e6-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="900e6-130">Return value</span></span>

<span data-ttu-id="900e6-131">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="900e6-131">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="900e6-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="900e6-132">Remarks</span></span>

<span data-ttu-id="900e6-133">In alcuni casi, è opportuno impostare il parametro *LibraryLocationID* sulla stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="900e6-133">In some cases, it makes sense to set the *LibraryLocationID* parameter to the empty string.</span></span> <span data-ttu-id="900e6-134">Se ad esempio si imposta il parametro *LibraryLocationType* su AllCPAlbumIDs, la nuova vista rappresenterà tutti gli album.</span><span class="sxs-lookup"><span data-stu-id="900e6-134">For example, if you set the *LibraryLocationType* parameter to AllCPAlbumIDs, the new view will represent all albums.</span></span> <span data-ttu-id="900e6-135">Nessun singolo album sarà l'obiettivo della nuova visualizzazione, quindi non è necessario fornire un ID album nel parametro *LibraryLocationID* .</span><span class="sxs-lookup"><span data-stu-id="900e6-135">No individual album will be the focus of the new view, so there is no need to supply an album ID in the *LibraryLocationID* parameter.</span></span>

<span data-ttu-id="900e6-136">Il parametro *ViewParams* consente a una pagina di individuazione di comunicare con un'altra pagina di individuazione.</span><span class="sxs-lookup"><span data-stu-id="900e6-136">The *ViewParams* parameter provides a way for a discovery page to communicate with another discovery page.</span></span> <span data-ttu-id="900e6-137">Quando script in una pagina di individuazione chiama **changeView**, Windows Media Player regola l'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="900e6-137">When script on a discovery page calls **changeView**, Windows Media Player adjusts its user interface.</span></span> <span data-ttu-id="900e6-138">Tale modifica fa in modo che il lettore chiami il metodo [IWMPContentPartner:: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) del plug-in per ottenere l'URL di una nuova pagina di individuazione.</span><span class="sxs-lookup"><span data-stu-id="900e6-138">That adjustment causes the Player to call the plug-in's [IWMPContentPartner::GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) method to get the URL of a new discovery page.</span></span> <span data-ttu-id="900e6-139">La stringa che la pagina di individuazione originale passa nel parametro *ViewParams* non viene passata a **GetTemplate**.</span><span class="sxs-lookup"><span data-stu-id="900e6-139">The string that the original discovery page passes in the *ViewParams* parameter does not get passed to **GetTemplate**.</span></span> <span data-ttu-id="900e6-140">Tuttavia, la nuova pagina di individuazione può recuperare la stringa *ViewParams* chiamando [External. viewParameters](external-viewparameters.md).</span><span class="sxs-lookup"><span data-stu-id="900e6-140">However, the new discovery page can retrieve the *ViewParams* string by calling [External.viewParameters](external-viewparameters.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="900e6-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="900e6-141">Requirements</span></span>



| <span data-ttu-id="900e6-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="900e6-142">Requirement</span></span> | <span data-ttu-id="900e6-143">Valore</span><span class="sxs-lookup"><span data-stu-id="900e6-143">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="900e6-144">Versione</span><span class="sxs-lookup"><span data-stu-id="900e6-144">Version</span></span><br/> | <span data-ttu-id="900e6-145">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="900e6-145">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="900e6-146">DLL</span><span class="sxs-lookup"><span data-stu-id="900e6-146">DLL</span></span><br/>     | <dl> <span data-ttu-id="900e6-147"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="900e6-147"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="900e6-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="900e6-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="900e6-149">**Oggetto esterno per i negozi di tipo 1 online**</span><span class="sxs-lookup"><span data-stu-id="900e6-149">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="900e6-150">**External. changeViewOnlineList**</span><span class="sxs-lookup"><span data-stu-id="900e6-150">**External.changeViewOnlineList**</span></span>](external-changeviewonlinelist.md)
</dt> <dt>

[<span data-ttu-id="900e6-151">**External. libraryLocationID**</span><span class="sxs-lookup"><span data-stu-id="900e6-151">**External.libraryLocationID**</span></span>](external-librarylocationid.md)
</dt> <dt>

[<span data-ttu-id="900e6-152">**External. libraryLocationType**</span><span class="sxs-lookup"><span data-stu-id="900e6-152">**External.libraryLocationType**</span></span>](external-librarylocationtype.md)
</dt> <dt>

[<span data-ttu-id="900e6-153">**External. viewParameters**</span><span class="sxs-lookup"><span data-stu-id="900e6-153">**External.viewParameters**</span></span>](external-viewparameters.md)
</dt> </dl>

 

 






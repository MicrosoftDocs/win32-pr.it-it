---
title: External. changeViewOnlineList, metodo
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. | External. changeViewOnlineList, metodo
ms.assetid: d7a45ced-431f-4d35-8c9c-c6eeba6fcbf3
keywords:
- Metodo changeViewOnlineList Windows Media Player
- Metodo changeViewOnlineList Windows Media Player, classe esterna
- Classe esterna Media Player Windows, metodo changeViewOnlineList
topic_type:
- apiref
api_name:
- External.changeViewOnlineList
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75e36adfa79b62863c3de78acf2adbd65011417b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331233"
---
# <a name="externalchangeviewonlinelist-method"></a><span data-ttu-id="0c904-107">External. changeViewOnlineList, metodo</span><span class="sxs-lookup"><span data-stu-id="0c904-107">External.changeViewOnlineList method</span></span>

> [!Note]  
> <span data-ttu-id="0c904-108">Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online.</span><span class="sxs-lookup"><span data-stu-id="0c904-108">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="0c904-109">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="0c904-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="0c904-110">Il metodo **changeViewOnlineList** modifica la visualizzazione in Windows Media Player per visualizzare un elenco generato dinamicamente dal negozio online.</span><span class="sxs-lookup"><span data-stu-id="0c904-110">The **changeViewOnlineList** method changes the view in Windows Media Player to display a list generated dynamically by the online store.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c904-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0c904-111">Syntax</span></span>


```JScript
External.changeViewOnlineList(
  LibraryLocationType,
  LibraryLocationID,
  Params,
  FriendlyName,
  ListType,
  ViewMode
)
```



## <a name="parameters"></a><span data-ttu-id="0c904-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="0c904-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c904-113">*LibraryLocationType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0c904-113">*LibraryLocationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c904-114">[Costante del percorso della libreria](library-location-constants.md) che specifica il tipo della nuova visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="0c904-114">A [library location constant](library-location-constants.md) that specifies the type of the new view.</span></span> <span data-ttu-id="0c904-115">Ad esempio, la costante CPGenreID specifica che la nuova vista mostrerà un genere particolare.</span><span class="sxs-lookup"><span data-stu-id="0c904-115">For example, the constant CPGenreID specifies that the new view will show a particular genre.</span></span>

</dd> <dt>

<span data-ttu-id="0c904-116">*LibraryLocationID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0c904-116">*LibraryLocationID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c904-117">**Stringa** contenente l'ID dell'elemento specifico da visualizzare nella nuova visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="0c904-117">**String** containing the ID of the specific item to show in the new view.</span></span> <span data-ttu-id="0c904-118">Ad esempio, se *LibraryLocationType* è CPGenreID, questo parametro specifica l'ID del genere da visualizzare nella nuova visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="0c904-118">For example, if *LibraryLocationType* is CPGenreID, then this parameter specifies the ID of the genre to show in the new view.</span></span> <span data-ttu-id="0c904-119">Questa stringa può essere vuota.</span><span class="sxs-lookup"><span data-stu-id="0c904-119">This string can be empty.</span></span>

</dd> <dt>

<span data-ttu-id="0c904-120">*Parametri* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0c904-120">*Params* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c904-121">**Stringa** contenente i parametri che Windows Media Player passa al plug-in del negozio online chiamando [IWMPContentPartner:: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate).</span><span class="sxs-lookup"><span data-stu-id="0c904-121">**String** containing parameters that Windows Media Player passes along to the online store's plug-in by calling [IWMPContentPartner::GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate).</span></span> <span data-ttu-id="0c904-122">Questi parametri non vengono interpretati da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="0c904-122">These parameters are not interpreted by Windows Media Player.</span></span> <span data-ttu-id="0c904-123">Vengono creati dal negozio online e hanno un significato solo per lo Store online.</span><span class="sxs-lookup"><span data-stu-id="0c904-123">They are created by the online store and have meaning only to the online store.</span></span> <span data-ttu-id="0c904-124">Questa stringa può essere vuota</span><span class="sxs-lookup"><span data-stu-id="0c904-124">This string can be empty</span></span>

</dd> <dt>

<span data-ttu-id="0c904-125">*FriendlyName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0c904-125">*FriendlyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c904-126">**Stringa** contenente un nome descrittivo, che deve essere visualizzato da Windows Media Player per l'elenco dinamico.</span><span class="sxs-lookup"><span data-stu-id="0c904-126">**String** containing a friendly name, to be displayed by Windows Media Player, for the dynamic list.</span></span>

</dd> <dt>

<span data-ttu-id="0c904-127">*ListType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0c904-127">*ListType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c904-128">Costante del percorso della libreria che specifica il tipo degli elementi nell'elenco generato dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="0c904-128">A library location constant that specifies the type of the items in the dynamically generated list.</span></span> <span data-ttu-id="0c904-129">Se, ad esempio, il valore di questo parametro è CPTrackID, l'elenco dinamico conterrà le tracce.</span><span class="sxs-lookup"><span data-stu-id="0c904-129">For example, if the value of this parameter is CPTrackID, then the dynamic list will contain tracks.</span></span>

</dd> <dt>

<span data-ttu-id="0c904-130">*ViewMode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0c904-130">*ViewMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c904-131">**Stringa** che specifica la modalità utilizzata da Windows Media Player per visualizzare l'elenco dinamico.</span><span class="sxs-lookup"><span data-stu-id="0c904-131">**String** that specifies the mode that Windows Media Player will use to display the dynamic list.</span></span> <span data-ttu-id="0c904-132">Il chiamante deve impostare questo parametro su uno dei valori seguenti, definiti in contentpartner. h:</span><span class="sxs-lookup"><span data-stu-id="0c904-132">The caller must set this parameter to one of the following values, which are defined in contentpartner.h:</span></span>

<span data-ttu-id="0c904-133">ViewModeReport</span><span class="sxs-lookup"><span data-stu-id="0c904-133">ViewModeReport</span></span>

<span data-ttu-id="0c904-134">ViewModeDetails</span><span class="sxs-lookup"><span data-stu-id="0c904-134">ViewModeDetails</span></span>

<span data-ttu-id="0c904-135">ViewModeIcon</span><span class="sxs-lookup"><span data-stu-id="0c904-135">ViewModeIcon</span></span>

<span data-ttu-id="0c904-136">ViewModeTile</span><span class="sxs-lookup"><span data-stu-id="0c904-136">ViewModeTile</span></span>

<span data-ttu-id="0c904-137">ViewModeOrderedList</span><span class="sxs-lookup"><span data-stu-id="0c904-137">ViewModeOrderedList</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c904-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0c904-138">Return value</span></span>

<span data-ttu-id="0c904-139">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="0c904-139">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c904-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="0c904-140">Remarks</span></span>

<span data-ttu-id="0c904-141">Quando lo script in una pagina di individuazione chiama **changeViewOnlineList**, Windows Media Player passa alcuni dei parametri insieme ai metodi [IWMPContentPartner:: GetListContents](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents) e [IWMPContentPartner:: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) , implementati dal plug-in Online Store.</span><span class="sxs-lookup"><span data-stu-id="0c904-141">When script on a discovery page calls **changeViewOnlineList**, Windows Media Player passes some of the parameters along to the [IWMPContentPartner::GetListContents](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents) and [IWMPContentPartner::GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) methods, which are implemented by the online store's plug-in.</span></span> <span data-ttu-id="0c904-142">Nella tabella seguente viene illustrata la corrispondenza tra i parametri dei tre metodi.</span><span class="sxs-lookup"><span data-stu-id="0c904-142">The following table shows the correspondence between the parameters of the three methods.</span></span>



| <span data-ttu-id="0c904-143">parametro changeViewOnlineList</span><span class="sxs-lookup"><span data-stu-id="0c904-143">changeViewOnlineList parameter</span></span> | <span data-ttu-id="0c904-144">Parametro GetListContents</span><span class="sxs-lookup"><span data-stu-id="0c904-144">GetListContents parameter</span></span> | <span data-ttu-id="0c904-145">Parametro GetTemplate</span><span class="sxs-lookup"><span data-stu-id="0c904-145">GetTemplate parameter</span></span> |
|--------------------------------|---------------------------|-----------------------|
| <span data-ttu-id="0c904-146">*LocationType*</span><span class="sxs-lookup"><span data-stu-id="0c904-146">*LocationType*</span></span>                 | <span data-ttu-id="0c904-147">*location*</span><span class="sxs-lookup"><span data-stu-id="0c904-147">*location*</span></span>                | <span data-ttu-id="0c904-148">*location*</span><span class="sxs-lookup"><span data-stu-id="0c904-148">*location*</span></span>            |
| <span data-ttu-id="0c904-149">*LocationID*</span><span class="sxs-lookup"><span data-stu-id="0c904-149">*LocationID*</span></span>                   | <span data-ttu-id="0c904-150">*pContext*</span><span class="sxs-lookup"><span data-stu-id="0c904-150">*pContext*</span></span>                | <span data-ttu-id="0c904-151">*pContext*</span><span class="sxs-lookup"><span data-stu-id="0c904-151">*pContext*</span></span>            |
| <span data-ttu-id="0c904-152">*Params*</span><span class="sxs-lookup"><span data-stu-id="0c904-152">*Params*</span></span>                       | <span data-ttu-id="0c904-153">*bstrParams*</span><span class="sxs-lookup"><span data-stu-id="0c904-153">*bstrParams*</span></span>              | <span data-ttu-id="0c904-154">*bstrViewParams*</span><span class="sxs-lookup"><span data-stu-id="0c904-154">*bstrViewParams*</span></span>      |
| <span data-ttu-id="0c904-155">*ListType*</span><span class="sxs-lookup"><span data-stu-id="0c904-155">*ListType*</span></span>                     | <span data-ttu-id="0c904-156">*bstrListType*</span><span class="sxs-lookup"><span data-stu-id="0c904-156">*bstrListType*</span></span>            | <span data-ttu-id="0c904-157">non applicabile</span><span class="sxs-lookup"><span data-stu-id="0c904-157">not applicable</span></span>        |



 

<span data-ttu-id="0c904-158">Poiché tutti e tre i metodi illustrati nella tabella precedente sono implementati dall'archivio online, è possibile usare i parametri in modo flessibile.</span><span class="sxs-lookup"><span data-stu-id="0c904-158">Because all three of the methods shown in the preceding table are implemented by the online store, you have some flexibility in how you use the parameters.</span></span> <span data-ttu-id="0c904-159">L'idea è che si forniscano informazioni sufficienti per **GetListContents** per determinare l'elenco da recuperare e per **GetTemplate** per determinare la pagina di individuazione da visualizzare successivamente.</span><span class="sxs-lookup"><span data-stu-id="0c904-159">The idea is that you provide enough information for **GetListContents** to determine which list it should retrieve and for **GetTemplate** to determine which discovery page should be displayed next.</span></span> <span data-ttu-id="0c904-160">Gli esempi seguenti illustrano due possibilità.</span><span class="sxs-lookup"><span data-stu-id="0c904-160">The following examples illustrate two possibilities.</span></span>

<span data-ttu-id="0c904-161">**Esempio 1: elenco dinamico presente nel catalogo del negozio online**</span><span class="sxs-lookup"><span data-stu-id="0c904-161">**Example 1: A dynamic list that is in the online store's catalog**</span></span>

<span data-ttu-id="0c904-162">Si supponga di volere che il plug-in ottenga il contenuto dell'elenco dinamico con ID 6 nel catalogo del negozio online.</span><span class="sxs-lookup"><span data-stu-id="0c904-162">Suppose you want the plug-in to get the contents of the dynamic list that has an ID of 6 in the online store's catalog.</span></span> <span data-ttu-id="0c904-163">Si supponga che l'elenco 6 sia un elenco di tracce.</span><span class="sxs-lookup"><span data-stu-id="0c904-163">Assume that list 6 is a list of tracks.</span></span> <span data-ttu-id="0c904-164">È possibile fornire il plug-in con informazioni sufficienti effettuando la chiamata seguente.</span><span class="sxs-lookup"><span data-stu-id="0c904-164">You could provide the plug-in with enough information by making the following call.</span></span>


```C++
external.changeViewOnlineList(
   "CPListID", 6, "", 
   "Songs for Today", "CPTrackID", "ViewModeDetails");
```



<span data-ttu-id="0c904-165">Si noti che il parametro *params* è vuoto; il plug-in dispone di informazioni sufficienti negli altri parametri.</span><span class="sxs-lookup"><span data-stu-id="0c904-165">Note that the *Params* parameter is empty; the plug-in has enough information in the other parameters.</span></span>

<span data-ttu-id="0c904-166">**Esempio 2: elenco dinamico non presente nel catalogo del negozio online**</span><span class="sxs-lookup"><span data-stu-id="0c904-166">**Example 2: A dynamic list that is not in the online store's catalog**</span></span>

<span data-ttu-id="0c904-167">Si supponga di volere che il plug-in ottenga il contenuto di un elenco dinamico che non si trova nel catalogo del negozio online.</span><span class="sxs-lookup"><span data-stu-id="0c904-167">Suppose that you want the plug-in to get the contents of a dynamic list that is not in the online store's catalog.</span></span> <span data-ttu-id="0c904-168">Forse si è deciso di avere un elenco dinamico che include canzoni selezionate da un particolare artista.</span><span class="sxs-lookup"><span data-stu-id="0c904-168">Perhaps you have decided to have a dynamic list that includes songs picked by a particular artist.</span></span> <span data-ttu-id="0c904-169">Si supponga che l'ID dell'artista sia 2 nel catalogo del negozio online.</span><span class="sxs-lookup"><span data-stu-id="0c904-169">Assume the artist has an ID of 2 in the online store's catalog.</span></span> <span data-ttu-id="0c904-170">È possibile effettuare la chiamata seguente.</span><span class="sxs-lookup"><span data-stu-id="0c904-170">You could make the following call.</span></span>


```C++
external.changeViewOnlineList(
   "CPArtistID", 2, "songs picked by Sally", 
   "Sally Picks", "CPTrackID", "ViewModeDetails");
```



<span data-ttu-id="0c904-171">Si noti che i parametri *LocationType* e *LocationID* non specificano l'elenco.</span><span class="sxs-lookup"><span data-stu-id="0c904-171">Note that the *LocationType* and *LocationID* parameters do not specify the list.</span></span> <span data-ttu-id="0c904-172">Il parametro *params* specifica invece l'elenco.</span><span class="sxs-lookup"><span data-stu-id="0c904-172">Instead, the *Params* parameter specifies the list.</span></span> <span data-ttu-id="0c904-173">I parametri *LocationType* e *LocationID* vengono passati a **IWMPContentPartner:: GetListContents**, ma in questo caso **GetListContents** possono ignorarli.</span><span class="sxs-lookup"><span data-stu-id="0c904-173">The *LocationType* and *LocationID* parameters are passed to **IWMPContentPartner::GetListContents**, but in this case, **GetListContents** can ignore them.</span></span> <span data-ttu-id="0c904-174">I parametri *LocationType* e *LocationID* vengono passati anche a **IWMPContentPartner:: GetTemplate**, che può usarli per determinare la pagina di individuazione da visualizzare con l'elenco dinamico.</span><span class="sxs-lookup"><span data-stu-id="0c904-174">The *LocationType* and *LocationID* parameters are also passed to **IWMPContentPartner::GetTemplate**, which can use them to determine which discovery page should be displayed with the dynamic list.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c904-175">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0c904-175">Requirements</span></span>



| <span data-ttu-id="0c904-176">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c904-176">Requirement</span></span> | <span data-ttu-id="0c904-177">Valore</span><span class="sxs-lookup"><span data-stu-id="0c904-177">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0c904-178">Versione</span><span class="sxs-lookup"><span data-stu-id="0c904-178">Version</span></span><br/> | <span data-ttu-id="0c904-179">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="0c904-179">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="0c904-180">DLL</span><span class="sxs-lookup"><span data-stu-id="0c904-180">DLL</span></span><br/>     | <dl> <span data-ttu-id="0c904-181"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c904-181"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c904-182">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0c904-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c904-183">**Oggetto esterno per i negozi di tipo 1 online**</span><span class="sxs-lookup"><span data-stu-id="0c904-183">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="0c904-184">**IWMPContentPartner::GetListContents**</span><span class="sxs-lookup"><span data-stu-id="0c904-184">**IWMPContentPartner::GetListContents**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents)
</dt> <dt>

[<span data-ttu-id="0c904-185">**IWMPContentPartnerCallback::AddListContents**</span><span class="sxs-lookup"><span data-stu-id="0c904-185">**IWMPContentPartnerCallback::AddListContents**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-addlistcontents)
</dt> <dt>

[<span data-ttu-id="0c904-186">**IWMPContentPartner:: GetTemplate**</span><span class="sxs-lookup"><span data-stu-id="0c904-186">**IWMPContentPartner::GetTemplate**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate)
</dt> <dt>

[<span data-ttu-id="0c904-187">**Posizione e elemento selezionato**</span><span class="sxs-lookup"><span data-stu-id="0c904-187">**Location and Selected Item**</span></span>](location-and-selected-item.md)
</dt> </dl>

 

 






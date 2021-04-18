---
title: Metodo IWMPMediaCollection getByAttribute
description: Il metodo getByAttribute restituisce un'interfaccia IWMPPlaylist che corrisponde all'attributo specificato con il valore specificato.
ms.assetid: ece70a2c-38bc-4652-8319-efcde5f9720a
keywords:
- Metodo getByAttribute Windows Media Player
- Metodo getByAttribute Windows Media Player, interfaccia IWMPMediaCollection
- Interfaccia IWMPMediaCollection Windows Media Player, metodo getByAttribute
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByAttribute
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd7adba98fbfa450cd938b56ec6d91598b918d0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333642"
---
# <a name="iwmpmediacollectiongetbyattribute-method"></a><span data-ttu-id="9fdea-106">Metodo IWMPMediaCollection:: getByAttribute</span><span class="sxs-lookup"><span data-stu-id="9fdea-106">IWMPMediaCollection::getByAttribute method</span></span>

<span data-ttu-id="9fdea-107">Il metodo **getByAttribute** restituisce un'interfaccia **IWMPPlaylist** che corrisponde all'attributo specificato con il valore specificato.</span><span class="sxs-lookup"><span data-stu-id="9fdea-107">The **getByAttribute** method returns an **IWMPPlaylist** interface that corresponds to the specified attribute having the specified value.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fdea-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9fdea-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getByAttribute(
  System.String bstrAttribute,
  System.String bstrValue
);
```


```VB

Public Function getByAttribute( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrValue As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByAttribute
```





## <a name="parameters"></a><span data-ttu-id="9fdea-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="9fdea-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fdea-110">*bstrAttribute* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9fdea-110">*bstrAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fdea-111">**System. String** che rappresenta l'attributo specificato.</span><span class="sxs-lookup"><span data-stu-id="9fdea-111">The **System.String** that is the specified attribute.</span></span>

</dd> <dt>

<span data-ttu-id="9fdea-112">*bstrValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9fdea-112">*bstrValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fdea-113">**System. String** che corrisponde al valore specificato.</span><span class="sxs-lookup"><span data-stu-id="9fdea-113">The **System.String** that is the specified value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fdea-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9fdea-114">Return value</span></span>

<span data-ttu-id="9fdea-115">Interfaccia **wmplib. IWMPPlaylist** per gli elementi multimediali recuperati.</span><span class="sxs-lookup"><span data-stu-id="9fdea-115">A **WMPLib.IWMPPlaylist** interface for the retrieved media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fdea-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="9fdea-116">Remarks</span></span>

<span data-ttu-id="9fdea-117">Questo metodo può essere utilizzato per creare una query generica per gli elementi multimediali che corrispondono a un valore per un attributo nella libreria.</span><span class="sxs-lookup"><span data-stu-id="9fdea-117">This method can be used to create a generic query for media items that match a value for an attribute in the library.</span></span> <span data-ttu-id="9fdea-118">Questa operazione è utile nel caso di attributi definiti dall'utente.</span><span class="sxs-lookup"><span data-stu-id="9fdea-118">This is useful in the case of user-defined attributes.</span></span> <span data-ttu-id="9fdea-119">Se l'attributo non esiste, verrà generato un errore.</span><span class="sxs-lookup"><span data-stu-id="9fdea-119">If the attribute does not exist, an error will result.</span></span>

<span data-ttu-id="9fdea-120">È possibile utilizzare questo metodo per recuperare tutti gli elementi multimediali di un tipo specifico.</span><span class="sxs-lookup"><span data-stu-id="9fdea-120">You can use this method to retrieve all of the media items of a specific type.</span></span> <span data-ttu-id="9fdea-121">Usare il nome dell'attributo **mediaType** e uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="9fdea-121">Use the attribute name **MediaType** and one of the following values.</span></span>



| <span data-ttu-id="9fdea-122">Valore</span><span class="sxs-lookup"><span data-stu-id="9fdea-122">Value</span></span>    | <span data-ttu-id="9fdea-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9fdea-123">Description</span></span>                                               |
|----------|-----------------------------------------------------------|
| <span data-ttu-id="9fdea-124">Audio</span><span class="sxs-lookup"><span data-stu-id="9fdea-124">audio</span></span>    | <span data-ttu-id="9fdea-125">Musica e altri elementi solo audio</span><span class="sxs-lookup"><span data-stu-id="9fdea-125">Music and other audio-only items</span></span>                          |
| <span data-ttu-id="9fdea-126">altro</span><span class="sxs-lookup"><span data-stu-id="9fdea-126">other</span></span>    | <span data-ttu-id="9fdea-127">Altri elementi, ad esempio un file con estensione ASF o l'URL di un flusso.</span><span class="sxs-lookup"><span data-stu-id="9fdea-127">Other items, such as an .asf file or the URL of a stream.</span></span> |
| <span data-ttu-id="9fdea-128">Foto</span><span class="sxs-lookup"><span data-stu-id="9fdea-128">photo</span></span>    | <span data-ttu-id="9fdea-129">Elementi foto.</span><span class="sxs-lookup"><span data-stu-id="9fdea-129">Photo items.</span></span> <span data-ttu-id="9fdea-130">Richiede Windows Media Player 10.</span><span class="sxs-lookup"><span data-stu-id="9fdea-130">Requires Windows Media Player 10.</span></span>            |
| <span data-ttu-id="9fdea-131">playlist</span><span class="sxs-lookup"><span data-stu-id="9fdea-131">playlist</span></span> | <span data-ttu-id="9fdea-132">Playlist rappresentate come elementi multimediali.</span><span class="sxs-lookup"><span data-stu-id="9fdea-132">Playlists represented as media items.</span></span>                     |
| <span data-ttu-id="9fdea-133">radio</span><span class="sxs-lookup"><span data-stu-id="9fdea-133">radio</span></span>    | <span data-ttu-id="9fdea-134">Elementi della stazione di radio.</span><span class="sxs-lookup"><span data-stu-id="9fdea-134">Radio station items.</span></span> <span data-ttu-id="9fdea-135">Non usato da Windows Media Player 10.</span><span class="sxs-lookup"><span data-stu-id="9fdea-135">Not used by Windows Media Player 10.</span></span> |
| <span data-ttu-id="9fdea-136">Video</span><span class="sxs-lookup"><span data-stu-id="9fdea-136">video</span></span>    | <span data-ttu-id="9fdea-137">Elementi video.</span><span class="sxs-lookup"><span data-stu-id="9fdea-137">Video items.</span></span>                                              |



 

<span data-ttu-id="9fdea-138">Prima di chiamare questo metodo, è necessario disporre dell'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="9fdea-138">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="9fdea-139">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="9fdea-139">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="9fdea-140">Per informazioni sugli attributi supportati da Windows Media Player, vedere il [riferimento all'attributo](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="9fdea-140">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span>

<span data-ttu-id="9fdea-141">Esistono due modi per recuperare un'interfaccia **IWMPMediaCollection** e il comportamento del metodo **getByAttribute** dipende da quali di questi due modi si usano.</span><span class="sxs-lookup"><span data-stu-id="9fdea-141">There are two ways you ways you can retrieve an **IWMPMediaCollection** interface, and the behavior of the **getByAttribute** method depends on which of those two ways you use.</span></span> <span data-ttu-id="9fdea-142">Se si recupera l'interfaccia chiamando [AxWindowsMediaPlayer. mediacollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), il metodo **getByAttribute** restituisce tutti gli elementi multimediali nella libreria.</span><span class="sxs-lookup"><span data-stu-id="9fdea-142">If you retrieve the interface by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), then the **getByAttribute** method returns all the media items in the library.</span></span> <span data-ttu-id="9fdea-143">Tuttavia, se si recupera l'interfaccia chiamando [IWMPLibrary. mediacollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), il metodo **getByAttribute** restituisce solo gli elementi audio della raccolta con l'attributo e il valore specificati.</span><span class="sxs-lookup"><span data-stu-id="9fdea-143">However, if you retrieve the interface by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), then the **getByAttribute** method returns only the audio items in the library that have the specified attribute and value.</span></span>

## <a name="examples"></a><span data-ttu-id="9fdea-144">Esempio</span><span class="sxs-lookup"><span data-stu-id="9fdea-144">Examples</span></span>

<span data-ttu-id="9fdea-145">L'esempio di codice seguente usa **getByAttribute** per riprodurre tutto il contenuto dalla libreria dall'artista denominato triodo 48.</span><span class="sxs-lookup"><span data-stu-id="9fdea-145">The following code example uses **getByAttribute** to play all content from the library by the artist named Triode 48.</span></span> <span data-ttu-id="9fdea-146">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="9fdea-146">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to a playlist that contains media items by a particular artist.
WMPLib.IWMPPlaylist pl = player.mediaCollection.getByAttribute("Artist", "Triode 48");

// Make the new playlist the current one.
player.currentPlaylist = pl;

// Play the media items in the current playlist. 
player.Ctlcontrols.play();
```


```VB

' Get an interface to a playlist that contains media items by a particular artist.
Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByAttribute(&quot;Artist&quot;, &quot;Triode 48&quot;)

&#39; Make the new playlist the current one.
player.currentPlaylist = pl

&#39; Play the media items in the current playlist. 
player.Ctlcontrols.play()
```





## <a name="requirements"></a><span data-ttu-id="9fdea-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9fdea-147">Requirements</span></span>



| <span data-ttu-id="9fdea-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fdea-148">Requirement</span></span> | <span data-ttu-id="9fdea-149">Valore</span><span class="sxs-lookup"><span data-stu-id="9fdea-149">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fdea-150">Versione</span><span class="sxs-lookup"><span data-stu-id="9fdea-150">Version</span></span><br/>   | <span data-ttu-id="9fdea-151">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="9fdea-151">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="9fdea-152">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9fdea-152">Namespace</span></span><br/> | <span data-ttu-id="9fdea-153">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="9fdea-153">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="9fdea-154">Assembly</span><span class="sxs-lookup"><span data-stu-id="9fdea-154">Assembly</span></span><br/>  | <dl> <span data-ttu-id="9fdea-155"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="9fdea-155"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fdea-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9fdea-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fdea-157">**Interfaccia IWMPMediaCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9fdea-157">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9fdea-158">**Interfaccia IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9fdea-158">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9fdea-159">**IWMPPlaylistCollection. getAll (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9fdea-159">**IWMPPlaylistCollection.getAll (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getall--vb-and-c.md)
</dt> </dl>

 

 






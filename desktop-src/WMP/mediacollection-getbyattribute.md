---
title: Mediacollection. getByAttribute, metodo
description: Il metodo getByAttribute recupera una playlist di elementi multimediali che contengono un valore specificato per un attributo specificato.
ms.assetid: a89f9c52-c655-4420-858e-c0eed661856f
keywords:
- Metodo getByAttribute Windows Media Player
- Metodo getByAttribute Windows Media Player, classe Mediacollection
- Mediacollection (classe) Windows Media Player, metodo getByAttribute
topic_type:
- apiref
api_name:
- MediaCollection.getByAttribute
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 533823127364416f8f4492c82381e682173c5c78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330345"
---
# <a name="mediacollectiongetbyattribute-method"></a><span data-ttu-id="9ec7b-106">Mediacollection. getByAttribute, metodo</span><span class="sxs-lookup"><span data-stu-id="9ec7b-106">MediaCollection.getByAttribute method</span></span>

<span data-ttu-id="9ec7b-107">Il metodo **getByAttribute** recupera una playlist di elementi multimediali che contengono un valore specificato per un attributo specificato.</span><span class="sxs-lookup"><span data-stu-id="9ec7b-107">The **getByAttribute** method retrieves a playlist of media items that contain a specified value for a specified attribute.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ec7b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9ec7b-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getByAttribute(
  attribute,
  value
)
```



## <a name="parameters"></a><span data-ttu-id="9ec7b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="9ec7b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ec7b-110">*attributo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9ec7b-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ec7b-111">**Stringa** che indica il nome dell'attributo da cercare.</span><span class="sxs-lookup"><span data-stu-id="9ec7b-111">**String** indicating the name of the attribute to search.</span></span> <span data-ttu-id="9ec7b-112">Per informazioni sugli attributi supportati da Windows Media Player, vedere la Guida di [riferimento](attribute-reference.md)agli attributi di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="9ec7b-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ec7b-113">*valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="9ec7b-113">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ec7b-114">**Stringa** che indica il valore che l'attributo deve avere.</span><span class="sxs-lookup"><span data-stu-id="9ec7b-114">**String** indicating the value that the attribute should have.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ec7b-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9ec7b-115">Return value</span></span>

<span data-ttu-id="9ec7b-116">Questo metodo restituisce un oggetto **playlist** .</span><span class="sxs-lookup"><span data-stu-id="9ec7b-116">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ec7b-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="9ec7b-117">Remarks</span></span>

<span data-ttu-id="9ec7b-118">Questo metodo può essere utilizzato per creare una query generica per gli elementi multimediali che corrispondono a un valore per un attributo nel database.</span><span class="sxs-lookup"><span data-stu-id="9ec7b-118">This method can be used to create a generic query for media items that match a value for an attribute in the database.</span></span> <span data-ttu-id="9ec7b-119">Questa operazione è utile nel caso di attributi definiti dall'utente.</span><span class="sxs-lookup"><span data-stu-id="9ec7b-119">This is useful in the case of user-defined attributes.</span></span> <span data-ttu-id="9ec7b-120">Se l'attributo non esiste, verrà generato un errore.</span><span class="sxs-lookup"><span data-stu-id="9ec7b-120">If the attribute does not exist, an error will result.</span></span>

<span data-ttu-id="9ec7b-121">È possibile utilizzare questo metodo per recuperare tutti gli elementi multimediali di un tipo specifico.</span><span class="sxs-lookup"><span data-stu-id="9ec7b-121">You can use this method to retrieve all of the media items of a specific type.</span></span> <span data-ttu-id="9ec7b-122">Usare il nome di attributo "MediaType" e uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="9ec7b-122">Use the attribute name "MediaType" and one of the following values:</span></span>



| <span data-ttu-id="9ec7b-123">Valore</span><span class="sxs-lookup"><span data-stu-id="9ec7b-123">Value</span></span>    | <span data-ttu-id="9ec7b-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9ec7b-124">Description</span></span>                                                |
|----------|------------------------------------------------------------|
| <span data-ttu-id="9ec7b-125">Audio</span><span class="sxs-lookup"><span data-stu-id="9ec7b-125">audio</span></span>    | <span data-ttu-id="9ec7b-126">Musica e altri elementi solo audio.</span><span class="sxs-lookup"><span data-stu-id="9ec7b-126">Music and other audio-only items.</span></span>                          |
| <span data-ttu-id="9ec7b-127">playlist</span><span class="sxs-lookup"><span data-stu-id="9ec7b-127">playlist</span></span> | <span data-ttu-id="9ec7b-128">Playlist rappresentate come oggetti **multimediali** .</span><span class="sxs-lookup"><span data-stu-id="9ec7b-128">Playlists represented as **Media** objects.</span></span>                |
| <span data-ttu-id="9ec7b-129">radio</span><span class="sxs-lookup"><span data-stu-id="9ec7b-129">radio</span></span>    | <span data-ttu-id="9ec7b-130">Elementi della stazione di radio.</span><span class="sxs-lookup"><span data-stu-id="9ec7b-130">Radio station items.</span></span> <span data-ttu-id="9ec7b-131">Non usato da Windows Media Player 10.</span><span class="sxs-lookup"><span data-stu-id="9ec7b-131">Not used by Windows Media Player 10.</span></span>  |
| <span data-ttu-id="9ec7b-132">Video</span><span class="sxs-lookup"><span data-stu-id="9ec7b-132">video</span></span>    | <span data-ttu-id="9ec7b-133">Elementi video.</span><span class="sxs-lookup"><span data-stu-id="9ec7b-133">Video items.</span></span>                                               |
| <span data-ttu-id="9ec7b-134">Foto</span><span class="sxs-lookup"><span data-stu-id="9ec7b-134">photo</span></span>    | <span data-ttu-id="9ec7b-135">Elementi foto.</span><span class="sxs-lookup"><span data-stu-id="9ec7b-135">Photo items.</span></span> <span data-ttu-id="9ec7b-136">Richiede Windows Media Player 10.</span><span class="sxs-lookup"><span data-stu-id="9ec7b-136">Requires Windows Media Player 10.</span></span>             |
| <span data-ttu-id="9ec7b-137">altro</span><span class="sxs-lookup"><span data-stu-id="9ec7b-137">other</span></span>    | <span data-ttu-id="9ec7b-138">Altri elementi, ad esempio file ASF o URL per flussi multimediali.</span><span class="sxs-lookup"><span data-stu-id="9ec7b-138">Other items, such as ASF files or URLs to streaming media.</span></span> |



 

<span data-ttu-id="9ec7b-139">Per usare questo metodo, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="9ec7b-139">To use this method, read access to the library is required.</span></span> <span data-ttu-id="9ec7b-140">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="9ec7b-140">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="9ec7b-141">Esempio</span><span class="sxs-lookup"><span data-stu-id="9ec7b-141">Examples</span></span>

<span data-ttu-id="9ec7b-142">Nell'esempio JScript seguente viene utilizzato *mediacollection*. **getByAttribute** per riprodurre tutto il contenuto dalla libreria dall'artista denominato triodo 48.</span><span class="sxs-lookup"><span data-stu-id="9ec7b-142">The following JScript example uses *MediaCollection*.**getByAttribute** to play all content from the library by the artist named Triode 48.</span></span> <span data-ttu-id="9ec7b-143">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="9ec7b-143">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Get a playlist object filled with media items by a 
// particular artist.
var pl = Player.mediaCollection.getByAttribute("Artist", "Triode 48");

// Make the new playlist the current one.
Player.currentPlaylist = pl;

// Start Windows Media Player.
Player.controls.play();

```



## <a name="requirements"></a><span data-ttu-id="9ec7b-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9ec7b-144">Requirements</span></span>



| <span data-ttu-id="9ec7b-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ec7b-145">Requirement</span></span> | <span data-ttu-id="9ec7b-146">Valore</span><span class="sxs-lookup"><span data-stu-id="9ec7b-146">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9ec7b-147">Versione</span><span class="sxs-lookup"><span data-stu-id="9ec7b-147">Version</span></span><br/> | <span data-ttu-id="9ec7b-148">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="9ec7b-148">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="9ec7b-149">DLL</span><span class="sxs-lookup"><span data-stu-id="9ec7b-149">DLL</span></span><br/>     | <dl> <span data-ttu-id="9ec7b-150"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ec7b-150"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ec7b-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9ec7b-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ec7b-152">**Mediacollection (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="9ec7b-152">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="9ec7b-153">**Oggetto playlist**</span><span class="sxs-lookup"><span data-stu-id="9ec7b-153">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="9ec7b-154">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="9ec7b-154">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="9ec7b-155">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="9ec7b-155">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






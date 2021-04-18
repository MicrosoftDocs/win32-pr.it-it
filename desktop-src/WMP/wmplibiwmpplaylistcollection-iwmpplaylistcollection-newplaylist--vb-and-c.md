---
title: Metodo IWMPPlaylistCollection nuova playlist
description: Il metodo nuova playlist restituisce un'interfaccia IWMPPlaylist per una nuova playlist vuota nella libreria.
ms.assetid: cc0cb356-9a90-421c-8d1a-b79585f71124
keywords:
- Metodo nuova playlist Windows Media Player
- Metodo nuova playlist Windows Media Player, interfaccia IWMPPlaylistCollection
- Interfaccia IWMPPlaylistCollection Windows Media Player, metodo nuova playlist
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.newPlaylist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbc455c5815cee1aaac139886bca1d847ddc62b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324713"
---
# <a name="iwmpplaylistcollectionnewplaylist-method"></a><span data-ttu-id="4ea3f-106">Metodo IWMPPlaylistCollection:: nuova playlist</span><span class="sxs-lookup"><span data-stu-id="4ea3f-106">IWMPPlaylistCollection::newPlaylist method</span></span>

<span data-ttu-id="4ea3f-107">Il metodo **nuova playlist** restituisce un'interfaccia **IWMPPlaylist** per una nuova playlist vuota nella libreria.</span><span class="sxs-lookup"><span data-stu-id="4ea3f-107">The **newPlaylist** method returns an **IWMPPlaylist** interface for a new, empty playlist in the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ea3f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4ea3f-108">Syntax</span></span>


```CSharp
public IWMPPlaylist newPlaylist(
  System.String bstrName
);
```


```VB

Public Function newPlaylist( _
  ByVal bstrName As System.String _
) As IWMPPlaylist
Implements IWMPPlaylistCollection.newPlaylist
```





## <a name="parameters"></a><span data-ttu-id="4ea3f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="4ea3f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ea3f-110">*bstrName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4ea3f-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ea3f-111">**System. String** che rappresenta il nome della nuova playlist.</span><span class="sxs-lookup"><span data-stu-id="4ea3f-111">A **System.String** that is the name of the new playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ea3f-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4ea3f-112">Return value</span></span>

<span data-ttu-id="4ea3f-113">Interfaccia **wmplib. IWMPPlaylist** per la nuova playlist.</span><span class="sxs-lookup"><span data-stu-id="4ea3f-113">A **WMPLib.IWMPPlaylist** interface for the new playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ea3f-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="4ea3f-114">Remarks</span></span>

<span data-ttu-id="4ea3f-115">Questo metodo crea una playlist vuota nella libreria.</span><span class="sxs-lookup"><span data-stu-id="4ea3f-115">This method creates an empty playlist in the library.</span></span> <span data-ttu-id="4ea3f-116">Per riempire la playlist con elementi multimediali, usare **IWMPPlaylist. appendItem** o **IWMPPlaylist. InsertItem**.</span><span class="sxs-lookup"><span data-stu-id="4ea3f-116">To fill the playlist with media items, use **IWMPPlaylist.appendItem** or **IWMPPlaylist.insertItem**.</span></span>

<span data-ttu-id="4ea3f-117">Nella libreria sono consentite più playlist con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="4ea3f-117">Multiple playlists having the same name are permitted in the library.</span></span> <span data-ttu-id="4ea3f-118">Per evitare di creare un nome di playlist duplicato con questo metodo, usare il metodo **GetByName** e **IWMPPlaylistArray. Count** per individuare se una playlist con un determinato nome esiste già.</span><span class="sxs-lookup"><span data-stu-id="4ea3f-118">To avoid creating a duplicate playlist name with this method, use the **getByName** method and **IWMPPlaylistArray.count** to discover whether a playlist with a particular name already exists.</span></span>

<span data-ttu-id="4ea3f-119">Gli spazi iniziali e finali non sono consentiti nei nomi delle playlist e vengono rimossi automaticamente dal valore specificato per il parametro *bstrName* .</span><span class="sxs-lookup"><span data-stu-id="4ea3f-119">Leading and trailing spaces are not permitted in playlist names, and are automatically removed from the value specified for the *bstrName* parameter.</span></span>

<span data-ttu-id="4ea3f-120">Prima di chiamare questo metodo, è necessario disporre dell'accesso completo alla libreria.</span><span class="sxs-lookup"><span data-stu-id="4ea3f-120">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="4ea3f-121">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="4ea3f-121">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4ea3f-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="4ea3f-122">Examples</span></span>

<span data-ttu-id="4ea3f-123">Nell'esempio seguente viene creata una nuova playlist vuota denominata "Three", che viene aggiunta alla raccolta di playlist e viene restituita un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="4ea3f-123">The following example creates a new empty playlist called "ThreeList", adds it to the playlist collection, and returns an interface to it.</span></span> <span data-ttu-id="4ea3f-124">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="4ea3f-124">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a new empty playlist, named ThreeList, to the playlist collection.
WMPLib.IWMPPlaylist newList = player.playlistCollection.newPlaylist("ThreeList");
```


```VB

'  Add a new empty playlist, named ThreeList, to the playlist collection.
Dim newList As WMPLib.IWMPPlaylist = player.playlistCollection.newPlaylist(&quot;ThreeList&quot;)
```





## <a name="requirements"></a><span data-ttu-id="4ea3f-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4ea3f-125">Requirements</span></span>



| <span data-ttu-id="4ea3f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ea3f-126">Requirement</span></span> | <span data-ttu-id="4ea3f-127">Valore</span><span class="sxs-lookup"><span data-stu-id="4ea3f-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ea3f-128">Versione</span><span class="sxs-lookup"><span data-stu-id="4ea3f-128">Version</span></span><br/>   | <span data-ttu-id="4ea3f-129">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="4ea3f-129">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="4ea3f-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4ea3f-130">Namespace</span></span><br/> | <span data-ttu-id="4ea3f-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="4ea3f-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="4ea3f-132">Assembly</span><span class="sxs-lookup"><span data-stu-id="4ea3f-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4ea3f-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4ea3f-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ea3f-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4ea3f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ea3f-135">**Interfaccia IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4ea3f-135">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4ea3f-136">**IWMPPlaylist. appendItem (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4ea3f-136">**IWMPPlaylist.appendItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4ea3f-137">**IWMPPlaylist. insertItem (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4ea3f-137">**IWMPPlaylist.insertItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4ea3f-138">**IWMPPlaylistArray. Count (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4ea3f-138">**IWMPPlaylistArray.count (VB and C#)**</span></span>](wmplibiwmpplaylistarray-iwmpplaylistarray-count--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4ea3f-139">**Interfaccia IWMPPlaylistCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4ea3f-139">**IWMPPlaylistCollection Interface (VB and C#)**</span></span>](iwmpplaylistcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4ea3f-140">**IWMPPlaylistCollection. getByName (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4ea3f-140">**IWMPPlaylistCollection.getByName (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 






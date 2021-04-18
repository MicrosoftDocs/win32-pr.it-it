---
title: IWMPPlaylistCollection (metodo getByName)
description: Il metodo getByName restituisce un'interfaccia IWMPPlaylistArray che consente di accedere alle playlist con il nome specificato, se presenti.
ms.assetid: d41afab1-4103-4f59-a432-21a502499444
keywords:
- metodo getByName Media Player Windows
- metodo getByName Media Player Windows, interfaccia IWMPPlaylistCollection
- Interfaccia IWMPPlaylistCollection Windows Media Player, metodo getByName
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.getByName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e51f83b4db019286c04762a081e649fec282135e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331362"
---
# <a name="iwmpplaylistcollectiongetbyname-method"></a><span data-ttu-id="a52fa-106">Metodo IWMPPlaylistCollection:: getByName</span><span class="sxs-lookup"><span data-stu-id="a52fa-106">IWMPPlaylistCollection::getByName method</span></span>

<span data-ttu-id="a52fa-107">Il metodo **GetByName** restituisce un'interfaccia **IWMPPlaylistArray** che consente di accedere alle playlist con il nome specificato, se presenti.</span><span class="sxs-lookup"><span data-stu-id="a52fa-107">The **getByName** method returns a **IWMPPlaylistArray** interface that provides access to playlists with the specified name, if any exist.</span></span>

## <a name="syntax"></a><span data-ttu-id="a52fa-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a52fa-108">Syntax</span></span>


```CSharp
public IWMPPlaylistArray getByName(
  System.String bstrName
);
```


```VB

Public Function getByName( _
  ByVal bstrName As System.String _
) As IWMPPlaylistArray
Implements IWMPPlaylistCollection.getByName
```





## <a name="parameters"></a><span data-ttu-id="a52fa-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a52fa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a52fa-110">*bstrName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a52fa-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a52fa-111">**System. String** che rappresenta il nome della playlist.</span><span class="sxs-lookup"><span data-stu-id="a52fa-111">A **System.String** that is the name of the playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a52fa-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a52fa-112">Return value</span></span>

<span data-ttu-id="a52fa-113">Interfaccia **wmplib. IWMPPlaylistArray** per la matrice di playlist recuperata.</span><span class="sxs-lookup"><span data-stu-id="a52fa-113">A **WMPLib.IWMPPlaylistArray** interface for the retrieved array of playlists.</span></span>

## <a name="remarks"></a><span data-ttu-id="a52fa-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="a52fa-114">Remarks</span></span>

<span data-ttu-id="a52fa-115">Usare **IWMPPlaylistArray. Count** per determinare se esiste una playlist.</span><span class="sxs-lookup"><span data-stu-id="a52fa-115">Use **IWMPPlaylistArray.count** to determine whether a playlist exists.</span></span> <span data-ttu-id="a52fa-116">Se **count** è zero, la matrice è vuota.</span><span class="sxs-lookup"><span data-stu-id="a52fa-116">If **count** is zero, the array is empty.</span></span>

<span data-ttu-id="a52fa-117">Prima di chiamare questo metodo, è necessario disporre dell'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="a52fa-117">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="a52fa-118">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="a52fa-118">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a52fa-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="a52fa-119">Examples</span></span>

<span data-ttu-id="a52fa-120">Nell'esempio seguente viene usato il comando **GetByName** per controllare la raccolta di playlist per una playlist denominata "Preferiti--4 e 5 stelle con classificazione".</span><span class="sxs-lookup"><span data-stu-id="a52fa-120">The following example uses **getByName** to check the playlist collection for a playlist named "Favorites -- 4 and 5 star rated".</span></span> <span data-ttu-id="a52fa-121">Se esiste una playlist con lo stesso nome, **GetByName** la imposta come playlist corrente.</span><span class="sxs-lookup"><span data-stu-id="a52fa-121">If a playlist by that name exists, **getByName** sets it as the current playlist.</span></span> <span data-ttu-id="a52fa-122">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="a52fa-122">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get the count of the playlists named "Favorites -- 4 and 5 star rated".
int checkit = player.playlistCollection.getByName("Favorites -- 4 and 5 star rated").count;

// Since duplicate playlist names are allowed, the count returned
// will be either zero (no playlist) or greater than zero (playlist exists).
if (checkit > 0)
{
    // Retrieve a playlist array containing "Favorites -- 4 and 5 star rated".
    // Assume that there is only one playlist with that name, and assign it to the 
    // current playlist.
    player.currentPlaylist = player.playlistCollection.getByName("Favorites -- 4 and 5 star rated").Item(0);
}
```


```VB

'  Get the count of the playlists named &quot;Favorites -- 4 and 5 star rated&quot;.
Dim checkit As Integer = player.playlistCollection.getByName(&quot;Favorites -- 4 and 5 star rated&quot;).count

&#39;  Since duplicate playlist names are allowed, the count returned
&#39;  will be either zero (no playlist) or greater than zero (playlist exists).
If (checkit > 0) Then

    &#39;  Retrieve a playlist array object containing &quot;Favorites -- 4 and 5 star rated&quot;.
    &#39;  Assume that there is only one playlist with that name, and assign it to the 
    &#39;  current playlist.
    player.currentPlaylist = player.playlistCollection.getByName(&quot;Favorites -- 4 and 5 star rated&quot;).Item(0)

End If
```





## <a name="requirements"></a><span data-ttu-id="a52fa-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a52fa-123">Requirements</span></span>



| <span data-ttu-id="a52fa-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a52fa-124">Requirement</span></span> | <span data-ttu-id="a52fa-125">Valore</span><span class="sxs-lookup"><span data-stu-id="a52fa-125">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a52fa-126">Versione</span><span class="sxs-lookup"><span data-stu-id="a52fa-126">Version</span></span><br/>   | <span data-ttu-id="a52fa-127">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="a52fa-127">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="a52fa-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a52fa-128">Namespace</span></span><br/> | <span data-ttu-id="a52fa-129">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="a52fa-129">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a52fa-130">Assembly</span><span class="sxs-lookup"><span data-stu-id="a52fa-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a52fa-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a52fa-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a52fa-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a52fa-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a52fa-133">**Interfaccia IWMPPlaylistArray (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a52fa-133">**IWMPPlaylistArray Interface (VB and C#)**</span></span>](iwmpplaylistarray--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a52fa-134">**IWMPPlaylistArray. Count (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a52fa-134">**IWMPPlaylistArray.count (VB and C#)**</span></span>](wmplibiwmpplaylistarray-iwmpplaylistarray-count--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a52fa-135">**Interfaccia IWMPPlaylistCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a52fa-135">**IWMPPlaylistCollection Interface (VB and C#)**</span></span>](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 






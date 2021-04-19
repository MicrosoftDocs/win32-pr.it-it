---
title: Metodo IWMPMedia isMemberOf
description: Il metodo isMemberOf restituisce un valore che indica se l'elemento multimediale specificato è un membro della playlist specificata.
ms.assetid: 491e0dd5-38e5-47a5-9c94-f1d27d297f8d
keywords:
- Metodo isMemberOf Windows Media Player
- Metodo isMemberOf Windows Media Player, interfaccia IWMPMedia
- Interfaccia IWMPMedia Windows Media Player, metodo isMemberOf
topic_type:
- apiref
api_name:
- IWMPMedia.isMemberOf
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f627e9b2f0e1c4b226dda13d280d521ad52df2ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332391"
---
# <a name="iwmpmediaismemberof-method"></a><span data-ttu-id="c46f6-106">Metodo IWMPMedia:: isMemberOf</span><span class="sxs-lookup"><span data-stu-id="c46f6-106">IWMPMedia::isMemberOf method</span></span>

<span data-ttu-id="c46f6-107">Il metodo **isMemberOf** restituisce un valore che indica se l'elemento multimediale specificato è un membro della playlist specificata.</span><span class="sxs-lookup"><span data-stu-id="c46f6-107">The **isMemberOf** method returns a value indicating whether the specified media item is a member of the specified playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="c46f6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c46f6-108">Syntax</span></span>


```CSharp
public System.Boolean isMemberOf(
  IWMPPlaylist pPlaylist
);
```


```VB

Public Function isMemberOf( _
  ByVal pPlaylist As IWMPPlaylist _
) As System.Boolean
Implements IWMPMedia.isMemberOf
```





## <a name="parameters"></a><span data-ttu-id="c46f6-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c46f6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c46f6-110">*pPlaylist* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c46f6-110">*pPlaylist* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c46f6-111">Interfaccia **wmplib. IWMPPlaylist** .</span><span class="sxs-lookup"><span data-stu-id="c46f6-111">A **WMPLib.IWMPPlaylist** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c46f6-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c46f6-112">Return value</span></span>

<span data-ttu-id="c46f6-113">Valore **System. Boolean** che indica se l'elemento multimediale è un membro della playlist.</span><span class="sxs-lookup"><span data-stu-id="c46f6-113">A **System.Boolean** value that indicates whether the media item is a member of the playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="c46f6-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="c46f6-114">Remarks</span></span>

<span data-ttu-id="c46f6-115">Questo metodo non consente di controllare le playlist recuperate tramite l'interfaccia **IWMPMediaCollection** .</span><span class="sxs-lookup"><span data-stu-id="c46f6-115">This method cannot check playlists retrieved through the **IWMPMediaCollection** interface.</span></span> <span data-ttu-id="c46f6-116">Per verificare se un elemento multimediale è un membro di una determinata playlist denominata, recuperare la raccolta di playlist con la proprietà **AxWindowsMediaPlayer. PlaylistCollection** .</span><span class="sxs-lookup"><span data-stu-id="c46f6-116">To test whether a media item is a member of a particular named playlist, retrieve the playlist collection with the **AxWindowsMediaPlayer.playlistCollection** property.</span></span> <span data-ttu-id="c46f6-117">Una volta recuperata la raccolta, recuperare la singola playlist chiamando il metodo **IWMPPlaylistCollection. GetByName** .</span><span class="sxs-lookup"><span data-stu-id="c46f6-117">Once you retrieve the collection, retrieve the individual playlist by calling the **IWMPPlaylistCollection.getByName** method.</span></span>

<span data-ttu-id="c46f6-118">Prima di chiamare questo metodo, è necessario disporre dell'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="c46f6-118">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="c46f6-119">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="c46f6-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c46f6-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="c46f6-120">Examples</span></span>

<span data-ttu-id="c46f6-121">Nell'esempio seguente viene usato **isMemberOf** per verificare se l'elemento multimediale corrente è un membro della playlist denominata All Music.</span><span class="sxs-lookup"><span data-stu-id="c46f6-121">The following example uses **isMemberOf** to test whether the current media item is a member of the playlist named All Music.</span></span> <span data-ttu-id="c46f6-122">In caso contrario, l'elemento multimediale corrente viene aggiunto alla playlist.</span><span class="sxs-lookup"><span data-stu-id="c46f6-122">If it is not, the current media item is appended to the playlist.</span></span> <span data-ttu-id="c46f6-123">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="c46f6-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to the playlist named All Music.
WMPLib.IWMPPlaylist sPlaylist = player.playlistCollection.getByName("All Music").Item(0);

// Test whether the current media item is a member of the All Music playlist.
// If it is not a member, append the current media item to the playlist.
if (player.currentMedia.isMemberOf(sPlaylist) == false)
{
    sPlaylist.appendItem(player.currentMedia);
}
```


```VB

' Get an interface to the playlist named All Music.
Dim sPlaylist As WMPLib.IWMPPlaylist = player.playlistCollection.getByName(&quot;All Music&quot;).Item(0)

&#39; Test whether the current media item is a member of the All Music playlist.
&#39; If it is not a member, then append the current media item to the playlist.
If (player.currentMedia.isMemberOf(sPlaylist) = False) Then

    sPlaylist.appendItem(player.currentMedia)

End If
```





## <a name="requirements"></a><span data-ttu-id="c46f6-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c46f6-124">Requirements</span></span>



| <span data-ttu-id="c46f6-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c46f6-125">Requirement</span></span> | <span data-ttu-id="c46f6-126">Valore</span><span class="sxs-lookup"><span data-stu-id="c46f6-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c46f6-127">Versione</span><span class="sxs-lookup"><span data-stu-id="c46f6-127">Version</span></span><br/>   | <span data-ttu-id="c46f6-128">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="c46f6-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="c46f6-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c46f6-129">Namespace</span></span><br/> | <span data-ttu-id="c46f6-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="c46f6-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="c46f6-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="c46f6-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c46f6-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c46f6-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c46f6-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c46f6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c46f6-134">**AxWindowsMediaPlayer. PlaylistCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c46f6-134">**AxWindowsMediaPlayer.playlistCollection (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-playlistcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c46f6-135">**Interfaccia IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c46f6-135">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c46f6-136">**Interfaccia IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c46f6-136">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c46f6-137">**IWMPPlaylistCollection. getByName (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c46f6-137">**IWMPPlaylistCollection.getByName (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 






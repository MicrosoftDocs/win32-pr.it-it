---
title: AxWindowsMediaPlayer. nuova playlist, metodo
description: Il metodo nuova playlist restituisce un'interfaccia IWMPPlaylist per una nuova playlist.
ms.assetid: caee8ee5-6201-474d-a4cb-80e574f84f0b
keywords:
- Metodo nuova playlist Windows Media Player
- Metodo nuova playlist Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Windows Media Player, metodo nuova playlist
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.newPlaylist
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8dc82be7aae37b4c1334b79f84e9d607b4f73cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330008"
---
# <a name="axwindowsmediaplayernewplaylist-method"></a><span data-ttu-id="b3dc3-106">AxWindowsMediaPlayer. nuova playlist, metodo</span><span class="sxs-lookup"><span data-stu-id="b3dc3-106">AxWindowsMediaPlayer.newPlaylist method</span></span>

<span data-ttu-id="b3dc3-107">Il metodo nuova playlist restituisce un'interfaccia IWMPPlaylist per una nuova playlist.</span><span class="sxs-lookup"><span data-stu-id="b3dc3-107">The newPlaylist method returns an IWMPPlaylist interface for a new playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3dc3-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b3dc3-108">Syntax</span></span>


```CSharp
public IWMPPlaylist newPlaylist(
  System.String bstrName,
  System.String bstrURL
);
```


```VB

Public Function newPlaylist( _
  ByVal bstrName As System.String, _
  ByVal bstrURL As System.String _
) As IWMPPlaylist
```





## <a name="parameters"></a><span data-ttu-id="b3dc3-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b3dc3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3dc3-110">*bstrName*</span><span class="sxs-lookup"><span data-stu-id="b3dc3-110">*bstrName*</span></span> 
</dt> <dd>

<span data-ttu-id="b3dc3-111">**System. String** che rappresenta il nome della nuova playlist.</span><span class="sxs-lookup"><span data-stu-id="b3dc3-111">The **System.String** that is the name of the new playlist.</span></span>

</dd> <dt>

<span data-ttu-id="b3dc3-112">*bstrURL*</span><span class="sxs-lookup"><span data-stu-id="b3dc3-112">*bstrURL*</span></span> 
</dt> <dd>

<span data-ttu-id="b3dc3-113">**System. String** che rappresenta l'URL della playlist Windows Media Metafile utilizzata per inizializzare la nuova playlist.</span><span class="sxs-lookup"><span data-stu-id="b3dc3-113">The **System.String** that is the URL of the Windows Media metafile playlist that is used to initialize the new playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3dc3-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b3dc3-114">Return value</span></span>

<span data-ttu-id="b3dc3-115">Interfaccia WMPLib. IWMPPlaylist che rappresenta la playlist appena creata.</span><span class="sxs-lookup"><span data-stu-id="b3dc3-115">A WMPLib.IWMPPlaylist interface that represents the newly created playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3dc3-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="b3dc3-116">Remarks</span></span>

<span data-ttu-id="b3dc3-117">Se il parametro *bstrURL* è una stringa di lunghezza zero o null (""), questo metodo crea una **playlist** vuota.</span><span class="sxs-lookup"><span data-stu-id="b3dc3-117">If the *bstrURL* parameter is a null or zero-length string (""), this method creates an empty **playlist**.</span></span> <span data-ttu-id="b3dc3-118">Se il parametro *bstrName* è una stringa di lunghezza zero (""), questo metodo applica il nome del metafile corrente.</span><span class="sxs-lookup"><span data-stu-id="b3dc3-118">If the *bstrName* parameter is a zero-length string (""), this method applies the current metafile name.</span></span>

<span data-ttu-id="b3dc3-119">La nuova playlist creata con questo metodo non viene aggiunta alla libreria.</span><span class="sxs-lookup"><span data-stu-id="b3dc3-119">The new playlist created with this method is not added to the library.</span></span> <span data-ttu-id="b3dc3-120">Per aggiungere una nuova playlist alla libreria, usare IWMPPlaylistCollection. **importPlaylist** o IWMPPlaylistCollection. **nuova playlist**.</span><span class="sxs-lookup"><span data-stu-id="b3dc3-120">To add a new playlist to the library, use IWMPPlaylistCollection.**importPlaylist** or IWMPPlaylistCollection.**newPlaylist**.</span></span> <span data-ttu-id="b3dc3-121">Eventuali spazi iniziali o finali nel nome della playlist vengono rimossi automaticamente quando vengono aggiunti alla libreria.</span><span class="sxs-lookup"><span data-stu-id="b3dc3-121">Any leading or trailing spaces in the playlist name are automatically removed when it is added to the library.</span></span>

<span data-ttu-id="b3dc3-122">Poiché la libreria consente più playlist con lo stesso nome, è consigliabile verificare la presenza di una playlist con un nome specificato prima di aggiungerne una nuova.</span><span class="sxs-lookup"><span data-stu-id="b3dc3-122">Because the library allows multiple playlists with the same name, you may want to check for the presence of a playlist with a given name before adding a new one.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3dc3-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3dc3-123">Requirements</span></span>



| <span data-ttu-id="b3dc3-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3dc3-124">Requirement</span></span> | <span data-ttu-id="b3dc3-125">Valore</span><span class="sxs-lookup"><span data-stu-id="b3dc3-125">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3dc3-126">Versione</span><span class="sxs-lookup"><span data-stu-id="b3dc3-126">Version</span></span><br/>   | <span data-ttu-id="b3dc3-127">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="b3dc3-127">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="b3dc3-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b3dc3-128">Namespace</span></span><br/> | <span data-ttu-id="b3dc3-129">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="b3dc3-129">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="b3dc3-130">Assembly</span><span class="sxs-lookup"><span data-stu-id="b3dc3-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b3dc3-131"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b3dc3-131"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3dc3-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b3dc3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3dc3-133">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b3dc3-133">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b3dc3-134">**Interfaccia IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b3dc3-134">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b3dc3-135">**IWMPPlaylistCollection. importPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b3dc3-135">**IWMPPlaylistCollection.importPlaylist (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b3dc3-136">**IWMPPlaylistCollection. nuova playlist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b3dc3-136">**IWMPPlaylistCollection.newPlaylist (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> </dl>

 

 






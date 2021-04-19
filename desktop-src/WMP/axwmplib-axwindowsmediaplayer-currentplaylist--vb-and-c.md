---
title: Proprietà AxWindowsMediaPlayer. currentPlaylist
description: La proprietà currentPlaylist Ottiene o imposta l'interfaccia IWMPPlaylist corrente che fornisce un modo semplice per organizzare e modificare gli elementi multimediali in un elenco.
ms.assetid: d5a9f126-a628-499c-a012-8a47c6c987ef
keywords:
- Finestra delle proprietà di currentPlaylist Media Player
- Proprietà currentPlaylist Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Media Player Windows, proprietà currentPlaylist
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.currentPlaylist
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a0f5b91a2e65b81fd1f13da0bad5f77c5ea1415
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330129"
---
# <a name="axwindowsmediaplayercurrentplaylist-property"></a><span data-ttu-id="c44e5-106">Proprietà AxWindowsMediaPlayer. currentPlaylist</span><span class="sxs-lookup"><span data-stu-id="c44e5-106">AxWindowsMediaPlayer.currentPlaylist property</span></span>

<span data-ttu-id="c44e5-107">La proprietà currentPlaylist Ottiene o imposta l'interfaccia **IWMPPlaylist** corrente che fornisce un modo semplice per organizzare e modificare gli elementi multimediali in un elenco.</span><span class="sxs-lookup"><span data-stu-id="c44e5-107">The currentPlaylist property gets or sets the current **IWMPPlaylist** interface that provides an easy way to organize and manipulate media items in a list.</span></span>

## <a name="syntax"></a><span data-ttu-id="c44e5-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c44e5-108">Syntax</span></span>


```CSharp
public IWMPPlaylist currentPlaylist {get; set;}
```


```VB

Public Property currentPlaylist As IWMPPlaylist
```





## <a name="property-value"></a><span data-ttu-id="c44e5-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="c44e5-109">Property value</span></span>

<span data-ttu-id="c44e5-110">Interfaccia WMPLib. IWMPPlaylist che fornisce l'accesso alla playlist corrente.</span><span class="sxs-lookup"><span data-stu-id="c44e5-110">The WMPLib.IWMPPlaylist interface that provides access to the current playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="c44e5-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="c44e5-111">Remarks</span></span>

<span data-ttu-id="c44e5-112">Se la proprietà IWMPSettings. AutoStart (accessibile anche tramite AxWindowsMediaPlayer. Settings.**autostart**) è true, la riproduzione viene avviata automaticamente quando si imposta **currentPlaylist**.</span><span class="sxs-lookup"><span data-stu-id="c44e5-112">If the IWMPSettings.autoStart property (also accessed via AxWindowsMediaPlayer.settings.**autoStart**) is true, playback begins automatically whenever you set **currentPlaylist**.</span></span>

<span data-ttu-id="c44e5-113">Questa proprietà accetta un'interfaccia IWMPPlaylist, che può essere acquisita in diversi modi, ad esempio ottenendo il valore da *IWMPPlaylistArray*. **Elemento** o *IWMPPlaylistCollection*. proprietà **nuova playlist** .</span><span class="sxs-lookup"><span data-stu-id="c44e5-113">This property takes an IWMPPlaylist interface, which can be acquired in several ways, such as by getting the value from the *IWMPPlaylistArray*.**Item** or *IWMPPlaylistCollection*.**newPlaylist** properties.</span></span> <span data-ttu-id="c44e5-114">Per caricare un elemento della **playlist** usando un nome di file, impostare la proprietà URL o usare AxWindowsMediaPlayer. **nuova playlist**.</span><span class="sxs-lookup"><span data-stu-id="c44e5-114">To load a **playlist** item using a file name, set the URL property or use AxWindowsMediaPlayer.**newPlaylist**.</span></span>

## <a name="examples"></a><span data-ttu-id="c44e5-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="c44e5-115">Examples</span></span>

<span data-ttu-id="c44e5-116">Nell'esempio seguente viene recuperata la prima playlist nella libreria e viene utilizzata la proprietà currentPlaylist per impostare la playlist recuperata come playlist corrente e visualizzarne il nome.</span><span class="sxs-lookup"><span data-stu-id="c44e5-116">The following example retrieves the first playlist in the library and uses the currentPlaylist property to set the retrieved playlist as the current playlist, and display its name.</span></span> <span data-ttu-id="c44e5-117">L'oggetto AxWMPLib. AxWindowsMediaPlayer è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="c44e5-117">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to the first playlist from the library. 
WMPLib.IWMPPlaylist firstPlaylist = player.playlistCollection.getAll().Item(0);

// Make the retrieved playlist the current playlist.
player.currentPlaylist = firstPlaylist;

// Display the name of the current playlist.
currentPlaylistLabel.Text = ("Found first playlist. Name = " + player.currentPlaylist.name);
```


```VB

' Get an interface to the first playlist from the library. 
Dim firstPlaylist As WMPLib.IWMPPlaylist = player.playlistCollection.getAll().Item(0)

&#39; Make the retrieved playlist the current playlist.
player.currentPlaylist = firstPlaylist

&#39; Display the name of the current playlist.
currentPlaylistLabel.Text = (&quot;Found first playlist. Name = &quot; + player.currentPlaylist.name)
```





## <a name="requirements"></a><span data-ttu-id="c44e5-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c44e5-118">Requirements</span></span>



| <span data-ttu-id="c44e5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c44e5-119">Requirement</span></span> | <span data-ttu-id="c44e5-120">Valore</span><span class="sxs-lookup"><span data-stu-id="c44e5-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c44e5-121">Versione</span><span class="sxs-lookup"><span data-stu-id="c44e5-121">Version</span></span><br/>   | <span data-ttu-id="c44e5-122">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="c44e5-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="c44e5-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c44e5-123">Namespace</span></span><br/> | <span data-ttu-id="c44e5-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="c44e5-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="c44e5-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="c44e5-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c44e5-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c44e5-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c44e5-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c44e5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c44e5-128">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c44e5-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c44e5-129">**AxWindowsMediaPlayer. nuova playlist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c44e5-129">**AxWindowsMediaPlayer.newPlaylist (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-newplaylist.md)
</dt> <dt>

[<span data-ttu-id="c44e5-130">**AxWindowsMediaPlayer. Settings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c44e5-130">**AxWindowsMediaPlayer.settings (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-settings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c44e5-131">**Interfaccia IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c44e5-131">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c44e5-132">**IWMPPlaylistArray. Item (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c44e5-132">**IWMPPlaylistArray.Item (VB and C#)**</span></span>](wmplibiwmpplaylistarray-iwmpplaylistarray-item--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c44e5-133">**IWMPPlaylistCollection. nuova playlist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c44e5-133">**IWMPPlaylistCollection.newPlaylist (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c44e5-134">**IWMPSettings. AutoStart (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c44e5-134">**IWMPSettings.autoStart (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 






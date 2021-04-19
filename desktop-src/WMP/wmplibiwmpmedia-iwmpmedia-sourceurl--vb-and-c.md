---
title: Proprietà sourceURL di IWMPMedia
description: La proprietà sourceURL Ottiene l'URL dell'elemento multimediale.
ms.assetid: adaef82c-eeed-4cce-859b-c54b9c8fa085
keywords:
- Finestra delle proprietà di sourceURL Media Player
- Proprietà di sourceURL Media Player Windows, interfaccia IWMPMedia
- Interfaccia IWMPMedia Windows Media Player, proprietà sourceURL
topic_type:
- apiref
api_name:
- IWMPMedia.sourceURL
- IWMPMedia.get_sourceURL
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9ad2cdb2c0a67f65f7b0cf722d1b613307806d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328576"
---
# <a name="iwmpmediasourceurl-property"></a><span data-ttu-id="a5d1e-106">Proprietà IWMPMedia:: sourceURL</span><span class="sxs-lookup"><span data-stu-id="a5d1e-106">IWMPMedia::sourceURL property</span></span>

<span data-ttu-id="a5d1e-107">La proprietà **sourceURL** Ottiene l'URL dell'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="a5d1e-107">The **sourceURL** property gets the URL of the media item.</span></span>

<span data-ttu-id="a5d1e-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="a5d1e-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5d1e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a5d1e-109">Syntax</span></span>


```CSharp
public System.String sourceURL {get;}
```


```VB

Public ReadOnly Property sourceURL As System.String
```





## <a name="property-value"></a><span data-ttu-id="a5d1e-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a5d1e-110">Property value</span></span>

<span data-ttu-id="a5d1e-111">**System. String** che rappresenta l'URL di origine.</span><span class="sxs-lookup"><span data-stu-id="a5d1e-111">A **System.String** that is the source URL.</span></span>

## <a name="examples"></a><span data-ttu-id="a5d1e-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="a5d1e-112">Examples</span></span>

<span data-ttu-id="a5d1e-113">Nell'esempio seguente viene usato **sourceURL** per recuperare l'URL del primo elemento multimediale nella playlist "All Music"; l'URL dell'elemento multimediale viene quindi assegnato alla proprietà URL oggetto Player.</span><span class="sxs-lookup"><span data-stu-id="a5d1e-113">The following example uses **sourceURL** to retrieve the URL of the first media item in the "All Music" playlist; the URL of the media item is then assigned to the player object URL property.</span></span> <span data-ttu-id="a5d1e-114">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="a5d1e-114">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to the All Music Playlist. 
WMPLib.IWMPPlaylist pl = player.playlistCollection.getByName("All Music").Item(0);

// Store a WMPLib.IWMPMedia3 interface to the first media item in the playlist. 
WMPLib.IWMPMedia3 media = (WMPLib.IWMPMedia3)pl.get_Item(0);

// Change the URL property of the player to the URL of the media item.
player.URL = media.sourceURL;

// Play the media item.
player.Ctlcontrols.play();
```


```VB

' Get an interface to the All Music Playlist. 
Dim pl As WMPLib.IWMPPlaylist = player.playlistCollection.getByName(&quot;All Music&quot;).Item(0)

&#39; Store a WMPLib.IWMPMedia3 interface to the first media item in the playlist. 
Dim media As WMPLib.IWMPMedia3 = pl.Item(0)

&#39; Change the URL property of the player to the URL of the media item.
player.URL = Media.sourceURL

&#39; Play the media item.
player.Ctlcontrols.play()
```





## <a name="requirements"></a><span data-ttu-id="a5d1e-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a5d1e-115">Requirements</span></span>



| <span data-ttu-id="a5d1e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5d1e-116">Requirement</span></span> | <span data-ttu-id="a5d1e-117">Valore</span><span class="sxs-lookup"><span data-stu-id="a5d1e-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5d1e-118">Versione</span><span class="sxs-lookup"><span data-stu-id="a5d1e-118">Version</span></span><br/>   | <span data-ttu-id="a5d1e-119">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="a5d1e-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="a5d1e-120">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a5d1e-120">Namespace</span></span><br/> | <span data-ttu-id="a5d1e-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="a5d1e-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a5d1e-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="a5d1e-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a5d1e-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a5d1e-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5d1e-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a5d1e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5d1e-125">**Interfaccia IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a5d1e-125">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 






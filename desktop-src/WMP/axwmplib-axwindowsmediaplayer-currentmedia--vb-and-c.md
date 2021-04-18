---
title: Proprietà AxWindowsMediaPlayer. currentMedia
description: La proprietà currentMedia Ottiene o imposta l'interfaccia IWMPMedia che corrisponde all'elemento multimediale corrente.
ms.assetid: 814ccb1d-713d-4b91-b225-d2199a7c9b6b
keywords:
- Finestra delle proprietà di currentMedia Media Player
- Proprietà currentMedia Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Media Player Windows, proprietà currentMedia
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.currentMedia
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3720a36d2a1969c652ed757f31301cf6a9ead706
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331493"
---
# <a name="axwindowsmediaplayercurrentmedia-property"></a><span data-ttu-id="94c92-106">Proprietà AxWindowsMediaPlayer. currentMedia</span><span class="sxs-lookup"><span data-stu-id="94c92-106">AxWindowsMediaPlayer.currentMedia property</span></span>

<span data-ttu-id="94c92-107">La proprietà currentMedia Ottiene o imposta l'interfaccia IWMPMedia che corrisponde all'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="94c92-107">The currentMedia property gets or sets the IWMPMedia interface that corresponds to the current media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="94c92-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="94c92-108">Syntax</span></span>


```CSharp
public IWMPMedia currentMedia {get; set;}
```


```VB

Public Property currentMedia As IWMPMedia
```





## <a name="property-value"></a><span data-ttu-id="94c92-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="94c92-109">Property value</span></span>

<span data-ttu-id="94c92-110">Interfaccia WMPLib. IWMPMedia che fornisce l'accesso all'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="94c92-110">The WMPLib.IWMPMedia interface that provides access to the current media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="94c92-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="94c92-111">Remarks</span></span>

<span data-ttu-id="94c92-112">Se AxWindowsMediaPlayer. Settings. la proprietà **autostart** è true, la riproduzione viene avviata automaticamente quando si imposta **currentMedia**.</span><span class="sxs-lookup"><span data-stu-id="94c92-112">If the AxWindowsMediaPlayer.settings.**autoStart** property is true, playback begins automatically whenever you set **currentMedia**.</span></span>

<span data-ttu-id="94c92-113">È possibile recuperare un'interfaccia IWMPMedia per un determinato elemento multimediale tramite la proprietà IWMPPlaylist. Item (il metodo IWMPPlaylist. Get \_ Item in C#).</span><span class="sxs-lookup"><span data-stu-id="94c92-113">You can retrieve an IWMPMedia interface for a given media item through the IWMPPlaylist.Item property (the IWMPPlaylist.get\_Item method in C#).</span></span> <span data-ttu-id="94c92-114">Per caricare un elemento multimediale usando un nome di file, impostare la proprietà URL o usare newMedia.</span><span class="sxs-lookup"><span data-stu-id="94c92-114">To load a media item using a file name, set the URL property or use newMedia.</span></span>

## <a name="examples"></a><span data-ttu-id="94c92-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="94c92-115">Examples</span></span>

<span data-ttu-id="94c92-116">Nell'esempio seguente viene recuperato il primo elemento multimediale nella libreria e viene utilizzata la proprietà currentMedia per impostare l'elemento multimediale recuperato come elemento multimediale corrente e visualizzarne il nome.</span><span class="sxs-lookup"><span data-stu-id="94c92-116">The following example retrieves the first media item in the library and uses the currentMedia property to set the retrieved media item as the current media item and display its name.</span></span> <span data-ttu-id="94c92-117">L'oggetto AxWMPLib. AxWindowsMediaPlayer è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="94c92-117">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to the first media item in the library. 
WMPLib.IWMPMedia3 firstMedia = (WMPLib.IWMPMedia3)player.mediaCollection.getAll().get_Item(0);

// Make the retrieved media item the current media item.
player.currentMedia = firstMedia;

// Display the name of the current media item.
currentMediaLabel.Text = ("Found first media item. Name = " + player.currentMedia.name);
```


```VB

' Get an interface to the first media item in the library. 
Dim firstMedia As WMPLib.IWMPMedia3 = player.mediaCollection.getAll().Item(0)

&#39; Make the retrieved media item the current media item.
player.currentMedia = firstMedia

&#39; Display the name of the current media item.
currentMediaLabel.Text = (&quot;Found first media item. Name = &quot; + player.currentMedia.name)
```





## <a name="requirements"></a><span data-ttu-id="94c92-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="94c92-118">Requirements</span></span>



| <span data-ttu-id="94c92-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="94c92-119">Requirement</span></span> | <span data-ttu-id="94c92-120">Valore</span><span class="sxs-lookup"><span data-stu-id="94c92-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94c92-121">Versione</span><span class="sxs-lookup"><span data-stu-id="94c92-121">Version</span></span><br/>   | <span data-ttu-id="94c92-122">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="94c92-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="94c92-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="94c92-123">Namespace</span></span><br/> | <span data-ttu-id="94c92-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="94c92-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="94c92-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="94c92-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="94c92-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="94c92-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94c92-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="94c92-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94c92-128">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="94c92-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="94c92-129">**AxWindowsMediaPlayer. newMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="94c92-129">**AxWindowsMediaPlayer.newMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-newmedia.md)
</dt> <dt>

[<span data-ttu-id="94c92-130">**AxWindowsMediaPlayer. URL (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="94c92-130">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="94c92-131">**Interfaccia IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="94c92-131">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="94c92-132">**IWMPPlaylist. Item (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="94c92-132">**IWMPPlaylist.Item (VB and C#)**</span></span>](iwmpplaylist-item--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="94c92-133">**IWMPSettings. AutoStart (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="94c92-133">**IWMPSettings.autoStart (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 






---
title: IWMPCdrom playlist (proprietà)
description: La proprietà playlist ottiene un'interfaccia IWMPPlaylist che rappresenta le tracce del CD attualmente presenti nell'unità CD o le voci del titolo a livello di radice per un DVD.
ms.assetid: 09c3db45-6586-4a5b-b72c-77c64473bdd0
keywords:
- Finestre delle proprietà della playlist Media Player
- Proprietà playlist Windows Media Player, interfaccia IWMPCdrom
- Interfaccia IWMPCdrom Windows Media Player, proprietà playlist
topic_type:
- apiref
api_name:
- IWMPCdrom.Playlist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a386881c8416f4ea1881f3ccd68ee4291aa3fa84
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329673"
---
# <a name="iwmpcdromplaylist-property"></a><span data-ttu-id="f84ae-106">IWMPCdrom::P proprietà laylist</span><span class="sxs-lookup"><span data-stu-id="f84ae-106">IWMPCdrom::Playlist property</span></span>

<span data-ttu-id="f84ae-107">La proprietà **playlist** ottiene un'interfaccia **IWMPPlaylist** che rappresenta le tracce del CD attualmente presenti nell'unità CD o le voci del titolo a livello di radice per un DVD.</span><span class="sxs-lookup"><span data-stu-id="f84ae-107">The **Playlist** property gets an **IWMPPlaylist** interface representing the tracks on the CD currently in the CD drive or the root-level title entries for a DVD.</span></span>

## <a name="syntax"></a><span data-ttu-id="f84ae-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f84ae-108">Syntax</span></span>


```CSharp
public IWMPPlaylist Playlist {get; set;}
```


```VB

Public ReadOnly Property Playlist As IWMPPlaylist
```





## <a name="property-value"></a><span data-ttu-id="f84ae-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f84ae-109">Property value</span></span>

<span data-ttu-id="f84ae-110">Interfaccia **wmplib. IWMPPlaylist** .</span><span class="sxs-lookup"><span data-stu-id="f84ae-110">A **WMPLib.IWMPPlaylist** interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="f84ae-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="f84ae-111">Remarks</span></span>

<span data-ttu-id="f84ae-112">In genere, il contenuto basato su DVD è organizzato in titoli.</span><span class="sxs-lookup"><span data-stu-id="f84ae-112">Typically, DVD-based content organized into titles.</span></span> <span data-ttu-id="f84ae-113">Ogni titolo contiene uno o più capitoli.</span><span class="sxs-lookup"><span data-stu-id="f84ae-113">Each title contains one or more chapters.</span></span> <span data-ttu-id="f84ae-114">Ogni DVD viene creato in modo diverso, quindi la modalità di utilizzo dei titoli e dei capitoli spetta all'autore del contenuto.</span><span class="sxs-lookup"><span data-stu-id="f84ae-114">Each DVD is authored differently, so how titles and chapters are used is up to the content author.</span></span>

<span data-ttu-id="f84ae-115">Per un DVD, questa proprietà ottiene una playlist che contiene come primo elemento un'interfaccia **IWMPMedia** denominata "DVD".</span><span class="sxs-lookup"><span data-stu-id="f84ae-115">For a DVD, this property gets a playlist that contains as the first item an **IWMPMedia** interface named "DVD".</span></span> <span data-ttu-id="f84ae-116">Questa interfaccia rappresenta il supporto DVD.</span><span class="sxs-lookup"><span data-stu-id="f84ae-116">This interface represents the DVD media.</span></span> <span data-ttu-id="f84ae-117">La riproduzione dell'elemento comporta la riproduzione del DVD dall'inizio se è la prima riproduzione dopo l'inserimento di un nuovo DVD o la ripresa della riproduzione se il DVD è uguale all'ultimo DVD visualizzato.</span><span class="sxs-lookup"><span data-stu-id="f84ae-117">Playing the item results in the DVD playing from the beginning if it is the first play after inserting a new DVD, or resuming playback if the DVD is the same as the last DVD viewed.</span></span> <span data-ttu-id="f84ae-118">Impostando questo elemento come elemento corrente durante la riproduzione, il DVD verrà riprodotto dall'inizio.</span><span class="sxs-lookup"><span data-stu-id="f84ae-118">Setting this item as the current item during playback results in the DVD playing from the beginning.</span></span>

<span data-ttu-id="f84ae-119">Gli elementi aggiuntivi, rappresentati dalle interfacce **IWMPMedia** , nella playlist sono titoli di DVD rappresentati da Playlist nidificate.</span><span class="sxs-lookup"><span data-stu-id="f84ae-119">Additional items (represented by **IWMPMedia** interfaces) in the playlist are DVD titles that are represented by nested playlists.</span></span> <span data-ttu-id="f84ae-120">Quando si imposta **IWMPControls. CurrentItem** in modo che corrisponda a uno di questi elementi nidificati della playlist, Windows Media Player imposta automaticamente la playlist nidificata come playlist corrente dopo l'inizio della riproduzione del capitolo.</span><span class="sxs-lookup"><span data-stu-id="f84ae-120">When you set **IWMPControls.currentItem** to equal one of these nested playlist items, Windows Media Player automatically sets the nested playlist as the current playlist after chapter playback begins.</span></span> <span data-ttu-id="f84ae-121">È quindi possibile usare le proprietà dell'interfaccia **IWMPPlaylist** , i metodi e gli eventi associati per lavorare con i capitoli DVD, che sono anche elementi della playlist.</span><span class="sxs-lookup"><span data-stu-id="f84ae-121">You can then use the **IWMPPlaylist** interface properties, methods and associated events to work with DVD chapters, which are also playlist items.</span></span>

<span data-ttu-id="f84ae-122">Per recuperare il valore di questa proprietà, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="f84ae-122">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="f84ae-123">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="f84ae-123">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f84ae-124">Esempio</span><span class="sxs-lookup"><span data-stu-id="f84ae-124">Examples</span></span>

<span data-ttu-id="f84ae-125">Nell'esempio seguente viene usata la **playlist** per inserire una casella di testo a più righe, denominata testo, con l'elenco di tracce del CD audio attualmente presente nella prima unità CD.</span><span class="sxs-lookup"><span data-stu-id="f84ae-125">The following example uses **Playlist** to fill a multi-line text box, named myText, with the track list of the audio CD currently in the first CD drive.</span></span> <span data-ttu-id="f84ae-126">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="f84ae-126">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get an interface that provides access to the CD playlist.
WMPLib.IWMPPlaylist playlist = player.cdromCollection.Item(0).Playlist;

// Create a string array to hold the track list.
String[] trackList = new String[playlist.count];

// Iterate through the CD playlist.
for (int i = 0; i < playlist.count; i++)
{
    trackList[i]= playlist.get_Item(i).name;
}

// Display the list of CD tracks in a multi-line text box.
myText.Lines = trackList;
```


```VB

'  Get an interface that provides access to the CD playlist.
Dim playlist As WMPLib.IWMPPlaylist = player.cdromCollection.Item(0).Playlist

&#39;  Create a string array to hold the track list.
Dim trackList(playlist.count) As String

&#39;  Iterate through the CD playlist.
For i As Integer = 0 To (playlist.count - 1)

    trackList(i) = playlist.Item(i).name

Next i

&#39;  Display the list of CD tracks in a multi-line text box.
myText.Lines = trackList
```





## <a name="requirements"></a><span data-ttu-id="f84ae-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f84ae-127">Requirements</span></span>



| <span data-ttu-id="f84ae-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f84ae-128">Requirement</span></span> | <span data-ttu-id="f84ae-129">Valore</span><span class="sxs-lookup"><span data-stu-id="f84ae-129">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f84ae-130">Versione</span><span class="sxs-lookup"><span data-stu-id="f84ae-130">Version</span></span><br/>   | <span data-ttu-id="f84ae-131">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="f84ae-131">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="f84ae-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f84ae-132">Namespace</span></span><br/> | <span data-ttu-id="f84ae-133">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="f84ae-133">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f84ae-134">Assembly</span><span class="sxs-lookup"><span data-stu-id="f84ae-134">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f84ae-135"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f84ae-135"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f84ae-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f84ae-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f84ae-137">**Interfaccia IWMPCdrom (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f84ae-137">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f84ae-138">**IWMPControls. currentItem (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f84ae-138">**IWMPControls.currentItem (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f84ae-139">**Interfaccia IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f84ae-139">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f84ae-140">**Interfaccia IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f84ae-140">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f84ae-141">**IWMPSettings2. mediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f84ae-141">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f84ae-142">**IWMPSettings2. requestMediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f84ae-142">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 






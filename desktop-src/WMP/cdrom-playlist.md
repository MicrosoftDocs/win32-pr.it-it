---
title: Cdrom. playlist
description: La proprietà playlist recupera un oggetto playlist che rappresenta le tracce del CD attualmente presenti nell'unità CD o le voci del titolo a livello di radice per DVD.
ms.assetid: 71c76b6c-1344-4d45-b86b-7e49be44dba8
keywords:
- Windows Media Player cdrom. playlist
topic_type:
- apiref
api_name:
- Cdrom.playlist
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcdb50daa169c6f6eb0690de376abd4433ffe130
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301604"
---
# <a name="cdromplaylist"></a><span data-ttu-id="6ac15-104">Cdrom. playlist</span><span class="sxs-lookup"><span data-stu-id="6ac15-104">Cdrom.playlist</span></span>

<span data-ttu-id="6ac15-105">La proprietà **playlist** recupera un oggetto **playlist** che rappresenta le tracce del CD attualmente presenti nell'unità CD o le voci del titolo a livello di radice per DVD.</span><span class="sxs-lookup"><span data-stu-id="6ac15-105">The **playlist** property retrieves a **Playlist** object representing the tracks on the CD currently in the CD drive or the root-level title entries for DVD.</span></span>

``` syntax
player.cdromCollection.item(
        index
        ).playlist
      
```

## <a name="possible-values"></a><span data-ttu-id="6ac15-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="6ac15-106">Possible Values</span></span>

<span data-ttu-id="6ac15-107">Questa proprietà è un oggetto **playlist** di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="6ac15-107">This property is a read-only **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ac15-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="6ac15-108">Remarks</span></span>

<span data-ttu-id="6ac15-109">In genere, i DVD sono organizzati in titoli.</span><span class="sxs-lookup"><span data-stu-id="6ac15-109">Typically, DVDs are organized into titles.</span></span> <span data-ttu-id="6ac15-110">Ogni titolo contiene uno o più capitoli.</span><span class="sxs-lookup"><span data-stu-id="6ac15-110">Each title contains one or more chapters.</span></span> <span data-ttu-id="6ac15-111">Ogni DVD viene creato in modo diverso, quindi la modalità di utilizzo dei titoli e dei capitoli spetta all'autore del contenuto.</span><span class="sxs-lookup"><span data-stu-id="6ac15-111">Each DVD is authored differently, so how titles and chapters are used is up to the content author.</span></span>

<span data-ttu-id="6ac15-112">Per il DVD, questo metodo recupera una playlist che contiene come primo elemento un oggetto **multimediale** che rappresenta il supporto DVD.</span><span class="sxs-lookup"><span data-stu-id="6ac15-112">For DVD, this method retrieves a playlist that contains as the first item a **Media** object that represents the DVD media.</span></span> <span data-ttu-id="6ac15-113">La riproduzione dell'elemento comporta la riproduzione del DVD dall'inizio se è la prima riproduzione dopo l'inserimento di un nuovo DVD o la ripresa della riproduzione se il DVD è uguale all'ultimo DVD visualizzato.</span><span class="sxs-lookup"><span data-stu-id="6ac15-113">Playing the item results in the DVD playing from the beginning if it is the first play after inserting a new DVD, or resuming playback if the DVD is the same as the last DVD viewed.</span></span> <span data-ttu-id="6ac15-114">Impostando questo elemento come quello corrente durante la riproduzione, il DVD viene riprodotto dall'inizio.</span><span class="sxs-lookup"><span data-stu-id="6ac15-114">Setting this item as the current one during playback results in the DVD playing from the beginning.</span></span>

<span data-ttu-id="6ac15-115">Gli elementi aggiuntivi (oggetti **multimediali** ) nella playlist sono titoli di DVD rappresentati da Playlist nidificate.</span><span class="sxs-lookup"><span data-stu-id="6ac15-115">Additional items (**Media** objects) in the playlist are DVD titles that are represented by nested playlists.</span></span> <span data-ttu-id="6ac15-116">Quando si specificano i *controlli*. **CurrentItem** è uguale a uno di questi elementi nidificati della playlist, Windows Media Player imposta automaticamente la playlist nidificata come *Player*. **currentPlaylist** dopo l'inizio della riproduzione del capitolo.</span><span class="sxs-lookup"><span data-stu-id="6ac15-116">When you specify *Controls*.**currentItem** to equal one of these nested playlist items, Windows Media Player automatically sets the nested playlist as *Player*.**currentPlaylist** after chapter playback begins.</span></span> <span data-ttu-id="6ac15-117">È quindi possibile usare le proprietà, i metodi e gli eventi dell'oggetto **currentPlaylist** per lavorare con i capitoli DVD, che sono anche elementi della playlist.</span><span class="sxs-lookup"><span data-stu-id="6ac15-117">You can then use the **currentPlaylist** object properties, methods, and events to work with DVD chapters, which are also playlist items.</span></span>

<span data-ttu-id="6ac15-118">Per recuperare il valore di questa proprietà, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="6ac15-118">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="6ac15-119">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="6ac15-119">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="6ac15-120">**Windows Media Player 10 Mobile:** Questa proprietà non è supportata.</span><span class="sxs-lookup"><span data-stu-id="6ac15-120">**Windows Media Player 10 Mobile:** This property is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="6ac15-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="6ac15-121">Examples</span></span>

<span data-ttu-id="6ac15-122">Nell'esempio seguente viene usato *CDROM*. **playlist** per inserire un elemento di testo HTML, denominato testo, con i titoli del CD audio attualmente presenti nella prima unità CD.</span><span class="sxs-lookup"><span data-stu-id="6ac15-122">The following example uses *Cdrom*.**playlist** to fill an HTML text element, named myText, with the titles of the audio CD currently in the first CD drive.</span></span> <span data-ttu-id="6ac15-123">Usare *cdromcollection*. **conteggio** per determinare il numero di unità CD disponibili.</span><span class="sxs-lookup"><span data-stu-id="6ac15-123">Use *CdromCollection*.**count** to determine the number of available CD drives.</span></span> <span data-ttu-id="6ac15-124">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="6ac15-124">The **Player** object was created with ID = "Player".</span></span>


```
// Store the CD playlist object.
var pl = Player.cdromCollection.Item(0).Playlist;

// Iterate through the CD track list.
for(var i = 0; i < pl.count; i++){

   // Print each CD track name.
   myText.value += pl.Item(i).name + "\n"; 
}
```



## <a name="requirements"></a><span data-ttu-id="6ac15-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6ac15-125">Requirements</span></span>



| <span data-ttu-id="6ac15-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ac15-126">Requirement</span></span> | <span data-ttu-id="6ac15-127">Valore</span><span class="sxs-lookup"><span data-stu-id="6ac15-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6ac15-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6ac15-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6ac15-129">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6ac15-129">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6ac15-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6ac15-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6ac15-131">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6ac15-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6ac15-132">Versione</span><span class="sxs-lookup"><span data-stu-id="6ac15-132">Version</span></span><br/>                  | <span data-ttu-id="6ac15-133">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="6ac15-133">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="6ac15-134">DLL</span><span class="sxs-lookup"><span data-stu-id="6ac15-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ac15-135"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ac15-135"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ac15-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6ac15-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ac15-137">**Oggetto cdrom**</span><span class="sxs-lookup"><span data-stu-id="6ac15-137">**Cdrom Object**</span></span>](cdrom-object.md)
</dt> <dt>

[<span data-ttu-id="6ac15-138">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="6ac15-138">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="6ac15-139">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="6ac15-139">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






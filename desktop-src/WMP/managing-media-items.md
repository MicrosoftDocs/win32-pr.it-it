---
title: Gestione di elementi multimediali
description: Gestione di elementi multimediali
ms.assetid: fba1df60-d603-4e37-a021-8fa618144149
keywords:
- Windows Media Player, libreria
- Modello a oggetti di Windows Media Player, libreria
- modello a oggetti, libreria
- Windows Media Player Mobile, libreria per il modello a oggetti
- Controllo ActiveX di Windows Media Player, libreria per il modello a oggetti
- Controllo ActiveX Windows Media Player Mobile, libreria per il modello a oggetti
- Controllo ActiveX, libreria per il modello a oggetti
- Windows Media Player Library, gestione di elementi multimediali
- libreria, gestione di elementi multimediali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b8003de49de9b7e4e51aabeffa222fb649ddef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116925"
---
# <a name="managing-media-items"></a><span data-ttu-id="36a8c-112">Gestione di elementi multimediali</span><span class="sxs-lookup"><span data-stu-id="36a8c-112">Managing Media Items</span></span>

<span data-ttu-id="36a8c-113">Un oggetto **multimediale** rappresenta un elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="36a8c-113">A **Media** object represents one media item.</span></span> <span data-ttu-id="36a8c-114">Dispone di proprietà e metodi che è possibile utilizzare per recuperare le informazioni e visualizzarle all'utente o per eseguire azioni diverse in base al valore recuperato.</span><span class="sxs-lookup"><span data-stu-id="36a8c-114">It has properties and methods you can use to retrieve information and display it to the user, or to take different actions based on the value you retrieve.</span></span>

<span data-ttu-id="36a8c-115">Gran parte del lavoro con gli oggetti **multimediali** riguarda i metadati relativi al contenuto dell'elemento multimediale, denominato attributi.</span><span class="sxs-lookup"><span data-stu-id="36a8c-115">Much of your work with **Media** objects involves metadata about the content of the media item, called the attributes.</span></span> <span data-ttu-id="36a8c-116">Nell'argomento [attributi elemento multimediale](media-item-attributes.md) viene descritto come leggere e modificare i valori di attributo.</span><span class="sxs-lookup"><span data-stu-id="36a8c-116">The topic [Media Item Attributes](media-item-attributes.md) describes how to read and change attribute values.</span></span> <span data-ttu-id="36a8c-117">Oltre a questo argomento, vedere le [linee guida sull'utilizzo dei metadati di Windows Media](/previous-versions/ms867702(v=msdn.10)) nel sito Web Microsoft per ulteriori informazioni sugli attributi e sul relativo utilizzo.</span><span class="sxs-lookup"><span data-stu-id="36a8c-117">In addition to this topic, see the [Windows Media Metadata Usage Guidelines](/previous-versions/ms867702(v=msdn.10)) on the Microsoft website for more information about the attributes and their use.</span></span>

<span data-ttu-id="36a8c-118">L'oggetto **multimediale** dispone di proprietà e metodi che recuperano direttamente alcuni attributi, ad esempio il nome o la durata dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="36a8c-118">The **Media** object has properties and methods that retrieve some attributes directly, such as the name or duration of the item.</span></span> <span data-ttu-id="36a8c-119">Per gli elementi video, è possibile recuperare l'altezza e la larghezza dell'immagine ed è possibile recuperare le informazioni sul marcatore in base al nome o all'indice di un marcatore.</span><span class="sxs-lookup"><span data-stu-id="36a8c-119">For video items, you can retrieve the height and width of the image, and you can retrieve marker information based on the name or index of a marker.</span></span> <span data-ttu-id="36a8c-120">È anche possibile determinare se un particolare elemento multimediale è incluso in una determinata playlist.</span><span class="sxs-lookup"><span data-stu-id="36a8c-120">You can also determine whether a particular media item is included in a particular playlist.</span></span>

## <a name="retrieving-a-media-object"></a><span data-ttu-id="36a8c-121">Recupero di un oggetto multimediale</span><span class="sxs-lookup"><span data-stu-id="36a8c-121">Retrieving a Media Object</span></span>

<span data-ttu-id="36a8c-122">È possibile accedere rapidamente all'elemento multimediale corrente usando il *lettore*. proprietà **currentMedia** .</span><span class="sxs-lookup"><span data-stu-id="36a8c-122">You can quickly access the current media item by using the *Player*.**currentMedia** property.</span></span>

<span data-ttu-id="36a8c-123">In questo argomento, l'oggetto **Player** è stato definito nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="36a8c-123">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="36a8c-124">Nell'esempio C# seguente viene recuperato un oggetto **multimediale** che rappresenta l'elemento corrente.</span><span class="sxs-lookup"><span data-stu-id="36a8c-124">The following C# example retrieves a **Media** object representing the current item.</span></span>


```C++
IWMPMedia media;
media = Player.currentMedia;

```



<span data-ttu-id="36a8c-125">È possibile creare un nuovo elemento multimediale da un file multimediale digitale usando il *lettore*. metodo **newMedia** .</span><span class="sxs-lookup"><span data-stu-id="36a8c-125">You can create a new media item from a digital media file by using the *Player*.**newMedia** method.</span></span> <span data-ttu-id="36a8c-126">Il metodo passa il percorso URL a un file multimediale digitale e restituisce un riferimento al nuovo oggetto **multimediale** .</span><span class="sxs-lookup"><span data-stu-id="36a8c-126">You pass the method the URL path to a digital media file, and it returns a reference to the new **Media** object.</span></span> <span data-ttu-id="36a8c-127">Il metodo non aggiunge direttamente il nuovo oggetto alla libreria.</span><span class="sxs-lookup"><span data-stu-id="36a8c-127">The method does not add the new object to the library directly.</span></span> <span data-ttu-id="36a8c-128">Tuttavia, è possibile passare l'oggetto alla *playlist*. metodo **appendItem** o *playlist*. metodo **InsertItem** .</span><span class="sxs-lookup"><span data-stu-id="36a8c-128">However, you can pass the object to the *Playlist*.**appendItem** method or the *Playlist*.**insertItem** method.</span></span>

<span data-ttu-id="36a8c-129">Nell'esempio C# seguente viene creato un oggetto **multimediale** basato su uno degli esempi di supporti digitali installati con Windows Media Player SDK.</span><span class="sxs-lookup"><span data-stu-id="36a8c-129">The following C# example creates a **Media** object based on one of the digital media samples installed with the Windows Media Player SDK.</span></span>


```C++
IWMPMedia media;
media = Player.newMedia("C:\\WMSDK\\WMPSDK10\\samples\\media\\laure.wma");

```



> [!Note]  
> <span data-ttu-id="36a8c-130">È necessario includere due barre rovesciate ( \) caratteri (o usare il carattere @ in C#) in una stringa per rappresentare un carattere barra rovesciata effettivo.</span><span class="sxs-lookup"><span data-stu-id="36a8c-130">You must include two backslash (\) characters (or use the @ character in C#) in a string to represent one actual backslash character.</span></span> <span data-ttu-id="36a8c-131">Questo perché C# usa un singolo carattere barra rovesciata per definire una sequenza di escape.</span><span class="sxs-lookup"><span data-stu-id="36a8c-131">This is because C# uses a single backslash character to define an escape sequence.</span></span>

 

<span data-ttu-id="36a8c-132">È possibile creare un nuovo elemento multimediale da un file multimediale digitale e aggiungerlo alla libreria in un unico passaggio usando *mediacollection*. **aggiungere** il metodo.</span><span class="sxs-lookup"><span data-stu-id="36a8c-132">You can create a new media item from a digital media file and add it to the library in one step by using the *MediaCollection*.**add** method.</span></span> <span data-ttu-id="36a8c-133">Come il *lettore*. metodo **newMedia** , il metodo **Add** accetta un percorso di un file multimediale digitale.</span><span class="sxs-lookup"><span data-stu-id="36a8c-133">Like the *Player*.**newMedia** method, the **add** method takes a path to a digital media file.</span></span>

<span data-ttu-id="36a8c-134">Nell'esempio C# seguente viene creato un oggetto **multimediale** basato su uno dei file di esempio SDK e tale oggetto viene aggiunto alla libreria.</span><span class="sxs-lookup"><span data-stu-id="36a8c-134">The following C# example creates a **Media** object based on one of the SDK sample files and adds that object to the library.</span></span>


```C++
IWMPMedia media;
media = Player.mediaCollection.add("C:\\WMSDK\\WMPSDK10\\samples\\media\\laure.wma");

```



<span data-ttu-id="36a8c-135">È possibile recuperare un oggetto **multimediale** che rappresenta un elemento multimediale in una playlist usando la *playlist*. metodo **Item** .</span><span class="sxs-lookup"><span data-stu-id="36a8c-135">You can retrieve a **Media** object representing a media item in a playlist by using the *Playlist*.**item** method.</span></span> <span data-ttu-id="36a8c-136">Nell'esempio C# seguente viene recuperato il sesto elemento multimediale dalla playlist corrente.</span><span class="sxs-lookup"><span data-stu-id="36a8c-136">The following C# example retrieves the sixth media item from the current playlist.</span></span>


```C++
IWMPMedia media;
media = Player.currentPlaylist.get_Item(5);

```



## <a name="related-topics"></a><span data-ttu-id="36a8c-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="36a8c-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36a8c-138">**Controls. currentItem**</span><span class="sxs-lookup"><span data-stu-id="36a8c-138">**Controls.currentItem**</span></span>](controls-currentitem.md)
</dt> <dt>

[<span data-ttu-id="36a8c-139">**Gestione delle playlist**</span><span class="sxs-lookup"><span data-stu-id="36a8c-139">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="36a8c-140">**Oggetto multimediale**</span><span class="sxs-lookup"><span data-stu-id="36a8c-140">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="36a8c-141">**Mediacollection. Add**</span><span class="sxs-lookup"><span data-stu-id="36a8c-141">**MediaCollection.add**</span></span>](mediacollection-add.md)
</dt> <dt>

[<span data-ttu-id="36a8c-142">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="36a8c-142">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="36a8c-143">**Player. newMedia**</span><span class="sxs-lookup"><span data-stu-id="36a8c-143">**Player.newMedia**</span></span>](player-newmedia.md)
</dt> <dt>

[<span data-ttu-id="36a8c-144">**Playlist. Item**</span><span class="sxs-lookup"><span data-stu-id="36a8c-144">**Playlist.item**</span></span>](playlist-item.md)
</dt> <dt>

[<span data-ttu-id="36a8c-145">**Utilizzo della libreria**</span><span class="sxs-lookup"><span data-stu-id="36a8c-145">**Working with the Library**</span></span>](working-with-the-library.md)
</dt> </dl>

 

 





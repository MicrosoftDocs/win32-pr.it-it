---
title: Gestione degli elementi multimediali
description: Gestione degli elementi multimediali
ms.assetid: fba1df60-d603-4e37-a021-8fa618144149
keywords:
- Windows Media Player,library
- Windows Media Player a oggetti, libreria
- modello a oggetti, libreria
- Windows Media Player Mobile, libreria per il modello a oggetti
- Windows Media Player controllo ActiveX, libreria per il modello a oggetti
- Windows Media Player controllo ActiveX mobile, libreria per il modello a oggetti
- Controllo ActiveX, libreria per il modello a oggetti
- Windows Media Player libreria, gestione di elementi multimediali
- libreria, gestione di elementi multimediali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf984c2f884ae828bd6426dd2a3f6da19a78ddea
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386890"
---
# <a name="managing-media-items"></a><span data-ttu-id="ff09f-112">Gestione degli elementi multimediali</span><span class="sxs-lookup"><span data-stu-id="ff09f-112">Managing Media Items</span></span>

<span data-ttu-id="ff09f-113">Un **oggetto Media** rappresenta un elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="ff09f-113">A **Media** object represents one media item.</span></span> <span data-ttu-id="ff09f-114">Include proprietà e metodi che è possibile usare per recuperare informazioni e visualizzarle all'utente o per eseguire azioni diverse in base al valore recuperato.</span><span class="sxs-lookup"><span data-stu-id="ff09f-114">It has properties and methods you can use to retrieve information and display it to the user, or to take different actions based on the value you retrieve.</span></span>

<span data-ttu-id="ff09f-115">Gran parte del lavoro con **gli oggetti Multimediali** comporta metadati relativi al contenuto dell'elemento multimediale, denominati attributi.</span><span class="sxs-lookup"><span data-stu-id="ff09f-115">Much of your work with **Media** objects involves metadata about the content of the media item, called the attributes.</span></span> <span data-ttu-id="ff09f-116">L'argomento [Attributi elemento multimediale](media-item-attributes.md) descrive come leggere e modificare i valori degli attributi.</span><span class="sxs-lookup"><span data-stu-id="ff09f-116">The topic [Media Item Attributes](media-item-attributes.md) describes how to read and change attribute values.</span></span> <span data-ttu-id="ff09f-117">Oltre a questo argomento, vedere le linee guida per l'utilizzo dei metadati di [Windows Media](/previous-versions/ms867702(v=msdn.10)) nel sito Web Microsoft per altre informazioni sugli attributi e sul relativo utilizzo.</span><span class="sxs-lookup"><span data-stu-id="ff09f-117">In addition to this topic, see the [Windows Media Metadata Usage Guidelines](/previous-versions/ms867702(v=msdn.10)) on the Microsoft website for more information about the attributes and their use.</span></span>

<span data-ttu-id="ff09f-118">**L'oggetto Media** dispone di proprietà e metodi che recuperano direttamente alcuni attributi, ad esempio il nome o la durata dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="ff09f-118">The **Media** object has properties and methods that retrieve some attributes directly, such as the name or duration of the item.</span></span> <span data-ttu-id="ff09f-119">Per gli elementi video, è possibile recuperare l'altezza e la larghezza dell'immagine ed è possibile recuperare le informazioni sul marcatore in base al nome o all'indice di un marcatore.</span><span class="sxs-lookup"><span data-stu-id="ff09f-119">For video items, you can retrieve the height and width of the image, and you can retrieve marker information based on the name or index of a marker.</span></span> <span data-ttu-id="ff09f-120">È anche possibile determinare se un particolare elemento multimediale è incluso in una playlist specifica.</span><span class="sxs-lookup"><span data-stu-id="ff09f-120">You can also determine whether a particular media item is included in a particular playlist.</span></span>

## <a name="retrieving-a-media-object"></a><span data-ttu-id="ff09f-121">Recupero di un oggetto multimediale</span><span class="sxs-lookup"><span data-stu-id="ff09f-121">Retrieving a Media Object</span></span>

<span data-ttu-id="ff09f-122">È possibile accedere rapidamente all'elemento multimediale corrente usando *player*. **proprietà currentMedia.**</span><span class="sxs-lookup"><span data-stu-id="ff09f-122">You can quickly access the current media item by using the *Player*.**currentMedia** property.</span></span>

<span data-ttu-id="ff09f-123">In questo argomento **l'oggetto Player** è stato definito nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="ff09f-123">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="ff09f-124">Nell'esempio C# seguente viene recuperato un **oggetto Media** che rappresenta l'elemento corrente.</span><span class="sxs-lookup"><span data-stu-id="ff09f-124">The following C# example retrieves a **Media** object representing the current item.</span></span>


```C++
IWMPMedia media;
media = Player.currentMedia;

```



<span data-ttu-id="ff09f-125">È possibile creare un nuovo elemento multimediale da un file multimediale digitale usando il *lettore*. **Metodo newMedia.**</span><span class="sxs-lookup"><span data-stu-id="ff09f-125">You can create a new media item from a digital media file by using the *Player*.**newMedia** method.</span></span> <span data-ttu-id="ff09f-126">Il metodo passa il percorso URL a un file multimediale digitale e restituisce un riferimento al nuovo **oggetto Media.**</span><span class="sxs-lookup"><span data-stu-id="ff09f-126">You pass the method the URL path to a digital media file, and it returns a reference to the new **Media** object.</span></span> <span data-ttu-id="ff09f-127">Il metodo non aggiunge direttamente il nuovo oggetto alla libreria.</span><span class="sxs-lookup"><span data-stu-id="ff09f-127">The method does not add the new object to the library directly.</span></span> <span data-ttu-id="ff09f-128">Tuttavia, è possibile passare l'oggetto alla *playlist*. **Metodo appendItem** o *playlist*. **Metodo insertItem.**</span><span class="sxs-lookup"><span data-stu-id="ff09f-128">However, you can pass the object to the *Playlist*.**appendItem** method or the *Playlist*.**insertItem** method.</span></span>

<span data-ttu-id="ff09f-129">L'esempio C# seguente crea un **oggetto Media** in base a uno degli esempi di supporti digitali installati con Windows Media Player SDK.</span><span class="sxs-lookup"><span data-stu-id="ff09f-129">The following C# example creates a **Media** object based on one of the digital media samples installed with the Windows Media Player SDK.</span></span>


```C++
IWMPMedia media;
media = Player.newMedia("C:\\WMSDK\\WMPSDK10\\samples\\media\\laure.wma");

```



> [!Note]  
> <span data-ttu-id="ff09f-130">È necessario includere due caratteri barra rovesciata ( ) (o usare il carattere @ in C#) in una stringa per rappresentare un carattere barra \\ rovesciata effettiva.</span><span class="sxs-lookup"><span data-stu-id="ff09f-130">You must include two backslash (\\) characters (or use the @ character in C#) in a string to represent one actual backslash character.</span></span> <span data-ttu-id="ff09f-131">Questo perché C# usa un singolo carattere barra rovesciata per definire una sequenza di escape.</span><span class="sxs-lookup"><span data-stu-id="ff09f-131">This is because C# uses a single backslash character to define an escape sequence.</span></span>

 

<span data-ttu-id="ff09f-132">È possibile creare un nuovo elemento multimediale da un file multimediale digitale e aggiungerlo alla libreria in un unico passaggio usando *MediaCollection*. **Metodo add.**</span><span class="sxs-lookup"><span data-stu-id="ff09f-132">You can create a new media item from a digital media file and add it to the library in one step by using the *MediaCollection*.**add** method.</span></span> <span data-ttu-id="ff09f-133">Come il *lettore*. **newMedia,** il **metodo add** accetta un percorso a un file multimediale digitale.</span><span class="sxs-lookup"><span data-stu-id="ff09f-133">Like the *Player*.**newMedia** method, the **add** method takes a path to a digital media file.</span></span>

<span data-ttu-id="ff09f-134">Nell'esempio C# seguente viene creato un **oggetto Media** basato su uno dei file di esempio dell'SDK e tale oggetto viene aggiunto alla libreria.</span><span class="sxs-lookup"><span data-stu-id="ff09f-134">The following C# example creates a **Media** object based on one of the SDK sample files and adds that object to the library.</span></span>


```C++
IWMPMedia media;
media = Player.mediaCollection.add("C:\\WMSDK\\WMPSDK10\\samples\\media\\laure.wma");

```



<span data-ttu-id="ff09f-135">È possibile recuperare un **oggetto Media** che rappresenta un elemento multimediale in una playlist usando *playlist*. **metodo item.**</span><span class="sxs-lookup"><span data-stu-id="ff09f-135">You can retrieve a **Media** object representing a media item in a playlist by using the *Playlist*.**item** method.</span></span> <span data-ttu-id="ff09f-136">Nell'esempio C# seguente viene recuperato il sesto elemento multimediale dalla playlist corrente.</span><span class="sxs-lookup"><span data-stu-id="ff09f-136">The following C# example retrieves the sixth media item from the current playlist.</span></span>


```C++
IWMPMedia media;
media = Player.currentPlaylist.get_Item(5);

```



## <a name="related-topics"></a><span data-ttu-id="ff09f-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ff09f-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff09f-138">**Controls.currentItem**</span><span class="sxs-lookup"><span data-stu-id="ff09f-138">**Controls.currentItem**</span></span>](controls-currentitem.md)
</dt> <dt>

[<span data-ttu-id="ff09f-139">**Gestione delle playlist**</span><span class="sxs-lookup"><span data-stu-id="ff09f-139">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="ff09f-140">**Oggetto multimediale**</span><span class="sxs-lookup"><span data-stu-id="ff09f-140">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="ff09f-141">**MediaCollection.add**</span><span class="sxs-lookup"><span data-stu-id="ff09f-141">**MediaCollection.add**</span></span>](mediacollection-add.md)
</dt> <dt>

[<span data-ttu-id="ff09f-142">**Player.currentMedia**</span><span class="sxs-lookup"><span data-stu-id="ff09f-142">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="ff09f-143">**Player.newMedia**</span><span class="sxs-lookup"><span data-stu-id="ff09f-143">**Player.newMedia**</span></span>](player-newmedia.md)
</dt> <dt>

[<span data-ttu-id="ff09f-144">**Playlist.item**</span><span class="sxs-lookup"><span data-stu-id="ff09f-144">**Playlist.item**</span></span>](playlist-item.md)
</dt> <dt>

[<span data-ttu-id="ff09f-145">**Uso della libreria**</span><span class="sxs-lookup"><span data-stu-id="ff09f-145">**Working with the Library**</span></span>](working-with-the-library.md)
</dt> </dl>

 

 





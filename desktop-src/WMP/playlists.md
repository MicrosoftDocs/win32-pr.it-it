---
title: Playlist
description: Playlist
ms.assetid: b1ac9208-33d1-448f-9e2e-920fad9c6add
keywords:
- Media Player di Windows, playlist
- Modello a oggetti di Windows Media Player, playlist
- modello a oggetti, playlist
- Controllo ActiveX di Windows Media Player, playlist
- Controllo ActiveX, playlist
- Controllo ActiveX Windows Media Player Mobile, playlist
- Windows Media Player Mobile, playlist
- playlist, migrazione
- Playlist Windows Media Metafile, migrazione
- playlist di metafile, migrazione
- Guida alla migrazione, playlist
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 124c07a6bd3aec0bebd235678e9fa8a5f069ec73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044447"
---
# <a name="playlists"></a><span data-ttu-id="3f0c9-114">Playlist</span><span class="sxs-lookup"><span data-stu-id="3f0c9-114">Playlists</span></span>

<span data-ttu-id="3f0c9-115">Il modello a oggetti del controllo ActiveX di Windows Media Player 6,4 include quattro metodi e una proprietà per l'utilizzo delle playlist di metafile di Windows Media:</span><span class="sxs-lookup"><span data-stu-id="3f0c9-115">The Windows Media Player 6.4 ActiveX control object model includes four methods and one property for working with Windows Media metafile playlists:</span></span>

-   <span data-ttu-id="3f0c9-116">*Player6*. **GetCurrentEntry**</span><span class="sxs-lookup"><span data-stu-id="3f0c9-116">*Player6*.**GetCurrentEntry**</span></span>
-   <span data-ttu-id="3f0c9-117">*Player6*. **SetCurrentEntry**</span><span class="sxs-lookup"><span data-stu-id="3f0c9-117">*Player6*.**SetCurrentEntry**</span></span>
-   <span data-ttu-id="3f0c9-118">*Player6*. **GetMediaParameter**</span><span class="sxs-lookup"><span data-stu-id="3f0c9-118">*Player6*.**GetMediaParameter**</span></span>
-   <span data-ttu-id="3f0c9-119">*Player6*. **GetMediaParameterName**</span><span class="sxs-lookup"><span data-stu-id="3f0c9-119">*Player6*.**GetMediaParameterName**</span></span>
-   <span data-ttu-id="3f0c9-120">*Player6*. **EntryCount**.</span><span class="sxs-lookup"><span data-stu-id="3f0c9-120">*Player6*.**EntryCount**.</span></span>

<span data-ttu-id="3f0c9-121">Insieme, offrono funzionalità limitate per lo spostamento in un metafile della playlist con estensione asx e per il recupero di informazioni sulle voci contenute nella playlist.</span><span class="sxs-lookup"><span data-stu-id="3f0c9-121">Together, these provide limited functionality for navigating a playlist metafile with an .asx file name extension and retrieving information about the entries contained in the playlist.</span></span>

<span data-ttu-id="3f0c9-122">In Windows Media Player 7 è stato introdotto "Catalogo multimediale".</span><span class="sxs-lookup"><span data-stu-id="3f0c9-122">Windows Media Player 7 introduced "Media Library."</span></span> <span data-ttu-id="3f0c9-123">La libreria consente agli utenti di organizzare il contenuto multimediale digitale, nonché di creare playlist personalizzate che possono essere gestite dall'interfaccia utente grafica del lettore.</span><span class="sxs-lookup"><span data-stu-id="3f0c9-123">The library allows users to organize their digital media content, as well as to create custom playlists that can be managed from the Player graphical user interface.</span></span> <span data-ttu-id="3f0c9-124">Il modello a oggetti del controllo ActiveX di Windows Media Player 7 o versione successiva fornisce il supporto per l'utilizzo delle playlist della libreria, nonché delle playlist contenute nei file di Windows Media con estensione asx.</span><span class="sxs-lookup"><span data-stu-id="3f0c9-124">The Windows Media Player 7 or later ActiveX control object model provides support for working with library playlists, as well as playlists contained in Windows Media metafiles with an .asx file name extension.</span></span>

> [!Note]  
> <span data-ttu-id="3f0c9-125">Per motivi di sicurezza, l'utente deve concedere i diritti di accesso alla libreria prima che il programma possa modificare il contenuto.</span><span class="sxs-lookup"><span data-stu-id="3f0c9-125">For security reasons, the user must grant access rights to the library before your program can manipulate its content.</span></span> <span data-ttu-id="3f0c9-126">I diritti di accesso possono essere richiesti e concessi solo tramite il modello a oggetti di Windows Media Player 9 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="3f0c9-126">Access rights can only be requested and granted through the Windows Media Player 9 Series or later object model.</span></span> <span data-ttu-id="3f0c9-127">Per informazioni dettagliate sui diritti di accesso, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="3f0c9-127">For details about access rights, see [Library Access](library-access.md).</span></span>

 

<span data-ttu-id="3f0c9-128">Il modello a oggetti di Windows Media Player 7 o versione successiva include tre oggetti per la gestione delle playlist.</span><span class="sxs-lookup"><span data-stu-id="3f0c9-128">The Windows Media Player 7 or later object model includes three objects for handling playlists.</span></span> <span data-ttu-id="3f0c9-129">L'oggetto **PlaylistCollection** fornisce funzionalità per l'organizzazione delle playlist; rappresenta l'intera raccolta di playlist nella libreria dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3f0c9-129">The **PlaylistCollection** object provides functionality for organizing playlists; it represents the entire collection of playlists in the user's library.</span></span> <span data-ttu-id="3f0c9-130">L'oggetto **PlaylistArray** fornisce un modo per recuperare una playlist specifica dall'oggetto **PlaylistCollection** usando un numero di indice; due dei metodi dell'oggetto **PlaylistCollection** recuperano un oggetto **PlaylistArray** .</span><span class="sxs-lookup"><span data-stu-id="3f0c9-130">The **PlaylistArray** object provides a way to retrieve a specific playlist from the **PlaylistCollection** object by using an index number; two of the **PlaylistCollection** object methods retrieve a **PlaylistArray** object.</span></span> <span data-ttu-id="3f0c9-131">L'oggetto **playlist** fornisce le proprietà e i metodi necessari per modificare gli elementi multimediali contenuti in una singola playlist.</span><span class="sxs-lookup"><span data-stu-id="3f0c9-131">The **Playlist** object provides the properties and methods necessary to manipulate media items contained in a single playlist.</span></span>

<span data-ttu-id="3f0c9-132">Ad esempio, poiché ogni playlist nella libreria ha un nome univoco, è possibile recuperare una playlist dalla libreria usando *PlaylistCollection*. metodo **GetByName** :</span><span class="sxs-lookup"><span data-stu-id="3f0c9-132">As an example, since each playlist in the library has a unique name, you can retrieve a playlist from the library using the *PlaylistCollection*.**getByName** method:</span></span>


```C++
// Retrieve a PlaylistArray object that contains 
// exactly one Playlist object.
var plarray = WMP9.playlistCollection.getByName("MyPlaylist");

// Get the Playlist object from the PlaylistArray object.
// The Playlist object has index number zero.
var pl = plarray.item(0);

// Make the retrieved playlist the current playlist.
WMP9.currentPlaylist = pl;

```



<span data-ttu-id="3f0c9-133">Si vuole usare più spesso la playlist corrente.</span><span class="sxs-lookup"><span data-stu-id="3f0c9-133">You will most frequently want to work with the current playlist.</span></span> <span data-ttu-id="3f0c9-134">Sebbene sia possibile usare diversi oggetti playlist, solo uno può essere recuperato dal *lettore*. proprietà **currentPlaylist** in un determinato momento: quello che Windows Media Player sta elaborando in quel momento.</span><span class="sxs-lookup"><span data-stu-id="3f0c9-134">While it is possible to use several playlist objects, only one can be retrieved by the *Player*.**currentPlaylist** property at any given time: the one that Windows Media Player is processing at that moment.</span></span>

<span data-ttu-id="3f0c9-135">Quando Windows Media Player 7 o versione successiva riproduce un metafile di Windows Media con estensione asx, viene innanzitutto creato un oggetto **playlist** .</span><span class="sxs-lookup"><span data-stu-id="3f0c9-135">When Windows Media Player 7 or later plays a Windows Media metafile with an .asx file name extension, it first creates a **Playlist** object.</span></span> <span data-ttu-id="3f0c9-136">Quindi, riempie l'oggetto con le informazioni dalla playlist. asx, quindi rende l'oggetto **playlist** corrente la playlist corrente.</span><span class="sxs-lookup"><span data-stu-id="3f0c9-136">Next, it fills the object with the information from the .asx playlist, and then makes that **Playlist** object the current playlist.</span></span> <span data-ttu-id="3f0c9-137">Ciò significa che è possibile utilizzare le proprietà e i metodi associati all'oggetto **playlist** per modificare le playlist. asx esattamente come si gestiranno le playlist nella libreria.</span><span class="sxs-lookup"><span data-stu-id="3f0c9-137">This means that you can use the properties and methods associated with the **Playlist** object to manipulate .asx playlists exactly as you would handle playlists in the library.</span></span> <span data-ttu-id="3f0c9-138">Ad esempio, per recuperare il numero di voci in una playlist con estensione asx usando il modello a oggetti della versione 6,4, usare *Player6*. Proprietà **EntryCount** :</span><span class="sxs-lookup"><span data-stu-id="3f0c9-138">For instance, to retrieve the number of entries in an .asx playlist using the version 6.4 object model, you use the *Player6*.**EntryCount** property:</span></span>


```C++
var entrycount = WMP64.EntryCount;

```



<span data-ttu-id="3f0c9-139">Quando si usa il modello a oggetti di Windows Media Player 7 o versione successiva, si usa la *playlist*. proprietà **count** :</span><span class="sxs-lookup"><span data-stu-id="3f0c9-139">When using the Windows Media Player 7 or later object model, you use the *Playlist*.**count** property:</span></span>


```C++
var entrycount = WMP9.currentPlaylist.count;

```



<span data-ttu-id="3f0c9-140">Quando si usa il controllo versione 6,4, è possibile usare *Player6*. Metodo **GetCurrentEntry** per recuperare l'indice della voce corrente in una playlist. asx:</span><span class="sxs-lookup"><span data-stu-id="3f0c9-140">When using the version 6.4 control, you can use the *Player6*.**GetCurrentEntry** method to retrieve the index of the current entry in an .asx playlist:</span></span>


```C++
var entrynum = WMP64.GetCurrentEntry();

```



<span data-ttu-id="3f0c9-141">È possibile ottenere lo stesso risultato usando il modello a oggetti di Windows Media Player 7 o versione successiva nello script.</span><span class="sxs-lookup"><span data-stu-id="3f0c9-141">You can achieve the same result by using the Windows Media Player 7 or later object model in script.</span></span> <span data-ttu-id="3f0c9-142">Nell'esempio JScript seguente viene confrontato l'oggetto multimediale corrente con ogni elemento della playlist.</span><span class="sxs-lookup"><span data-stu-id="3f0c9-142">The following JScript example compares the current media object to each item in the playlist.</span></span> <span data-ttu-id="3f0c9-143">Quando il *supporto*.  il risultato è true. una finestra di messaggio Visualizza l'indice dell'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="3f0c9-143">When *Media*.**isIdentical** returns true, a message box displays the index of the current media item.</span></span>


```C++
function matchit(){
// Store the current playlist object in a variable.
var pl = WMP9.currentPlaylist;

// Loop through the playlist one entry at a time.
  for (var i = 0; i < pl.count; i++){

   // Test whether the current media item matches 
   // the item in the playlist at the current loop index.
   if (WMP9.currentmedia.isIdentical(pl.item(i))){

       // They match, display the index.
       var message = "Current media at index: " + i;
       alert(message);

       // Exit the function, don't continue looping!
       return;
      }
  }
}

```



<span data-ttu-id="3f0c9-144">Per specificare l'indice della voce corrente in una playlist. asx, usare *Player6*. **SetCurrentEntry**.</span><span class="sxs-lookup"><span data-stu-id="3f0c9-144">To specify the index of the current entry in an .asx playlist, you use *Player6*.**SetCurrentEntry**.</span></span> <span data-ttu-id="3f0c9-145">Gli indici di voci della playlist nella versione 6,4 iniziano con 1, quindi per rendere la seconda voce in una playlist di metafile quella corrente, usare la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="3f0c9-145">Playlist entry indexes in version 6.4 start with 1, so to make the second entry in a metafile playlist the current one, use the following syntax:</span></span>


```C++
WMP6.SetCurrentEntry(2);

```



<span data-ttu-id="3f0c9-146">Gli indici di voci della playlist sono basati su zero in Windows Media Player 7 o versioni successive. per rendere la seconda voce in una playlist di metafile quella corrente, quando si usa il modello a oggetti di Windows Media Player 7 o versione successiva, usare la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="3f0c9-146">Playlist entry indexes are zero-based in Windows Media Player 7 or later; to make the second entry in a metafile playlist the current one, when using the Windows Media Player 7 or later object model, use the following syntax:</span></span>


```C++
WMP9.controls.currentItem = WMP9.currentPlaylist.item(1);

```



<span data-ttu-id="3f0c9-147">Nell'esempio JScript riportato di seguito viene illustrata una funzione che accetta un numero di indice come parametro e quindi rende la voce della playlist corrispondente all'indice dell'elemento multimediale corrente:</span><span class="sxs-lookup"><span data-stu-id="3f0c9-147">The following JScript example demonstrates a function that accepts an index number as a parameter, and then makes the playlist entry that corresponds to the index the current media item:</span></span>


```C++
function setindex(idx){
// Store the current playlist in a variable.
var pl = WMP9.currentPlaylist;

// Get the first playlist entry.
var firstmedia = pl.item(0);

// Start the Player to allow navigation within the playlist.
WMP9.controls.playItem(firstmedia);

// Test whether idx is within a valid range.
   if (idx < pl.count && idx >= 0){

     // Set the currentItem to the desired playlist item.
     WMP9.controls.currentItem = pl.item(idx);

     // Display the name of the media item.
     alert(WMP9.currentMedia.name);
     return true;
 }

// The index is out of range, stop the Player, alert the user.
WMP9.controls.stop();
alert("Index out of range");
return false;
}

```



<span data-ttu-id="3f0c9-148">I metafile di Windows Media possono contenere elementi di parametri personalizzati, che è possibile specificare usando il **<PARAM>** tag.</span><span class="sxs-lookup"><span data-stu-id="3f0c9-148">Windows Media metafiles can contain custom parameter elements, which you specify by using the **<PARAM>** tag.</span></span> <span data-ttu-id="3f0c9-149">Quando si usa il modello a oggetti versione 6,4, è possibile recuperare il nome di un parametro specifico con *Player6*. Metodo **GetMediaParameterName** .</span><span class="sxs-lookup"><span data-stu-id="3f0c9-149">When using the version 6.4 object model, you can retrieve the name of a particular parameter with the *Player6*.**GetMediaParameterName** method.</span></span> <span data-ttu-id="3f0c9-150">Nell'esempio JScript seguente viene recuperato il nome del primo parametro nella prima voce di una playlist. asx:</span><span class="sxs-lookup"><span data-stu-id="3f0c9-150">The following JScript example retrieves the name of the first parameter in the first entry of an .asx playlist:</span></span>


```C++
var paramname = WMP6.GetMediaParameterName(1,1);

```



<span data-ttu-id="3f0c9-151">Analogamente, è possibile recuperare il valore associato al parametro usando *Player6*. **GetMediaParameter**:</span><span class="sxs-lookup"><span data-stu-id="3f0c9-151">Similarly, you can retrieve the value associated with the parameter using *Player6*.**GetMediaParameter**:</span></span>


```C++
var paramvalue = WMP6.GetMediaParameter(1, paramname);

```



<span data-ttu-id="3f0c9-152">Nell'esempio di codice JScript seguente viene usato il modello a oggetti di Windows Media Player 7 o versione successiva per recuperare il nome e il valore del parametro dalla prima voce di una playlist. asx:</span><span class="sxs-lookup"><span data-stu-id="3f0c9-152">The following JScript example uses the Windows Media Player 7 or later object model to retrieve the parameter name and value from the first entry in an .asx playlist:</span></span>


```C++
function getattribute(){
// Store the first playlist entry as a Media object.
var firstmedia = WMP9.currentplaylist.item(0);

// Get the name of the first parameter in the object named firstmedia.
var attname = firstmedia.getAttributeName(0);

// Get the value of the first parameter in the object named firstmedia.
var attval = firstmedia.getItemInfo(attname);

// Display the information.
alert(attname + ": " + attval);
}

```



<span data-ttu-id="3f0c9-153">È possibile usare *PlaylistCollection*. metodo **importPlaylist** per aggiungere una playlist. asx alla libreria.</span><span class="sxs-lookup"><span data-stu-id="3f0c9-153">You can use the *PlaylistCollection*.**importPlaylist** method to add an .asx playlist to the library.</span></span> <span data-ttu-id="3f0c9-154">Una volta importato, la playlist del metafile diventa una playlist di libreria, in modo da poterla modificare usando tutte le proprietà e i metodi a sua disposizione.</span><span class="sxs-lookup"><span data-stu-id="3f0c9-154">Once imported, the metafile playlist becomes a library playlist, so you can manipulate it using all the properties and methods at your disposal.</span></span> <span data-ttu-id="3f0c9-155">L'utente deve concedere diritti di accesso completi alla libreria per consentire all'applicazione di usare il metodo **importPlaylist** .</span><span class="sxs-lookup"><span data-stu-id="3f0c9-155">The user must grant full access rights to the library for your application to be able to use the **importPlaylist** method.</span></span>

<span data-ttu-id="3f0c9-156">È possibile usare *PlaylistCollection*. **GetByName** per verificare se esiste una playlist.</span><span class="sxs-lookup"><span data-stu-id="3f0c9-156">You can use *PlaylistCollection*.**getByName** to test whether a playlist exists.</span></span> <span data-ttu-id="3f0c9-157">Questo metodo restituisce sempre un oggetto **PlaylistArray** valido.</span><span class="sxs-lookup"><span data-stu-id="3f0c9-157">This method always returns a valid **PlaylistArray** object.</span></span> <span data-ttu-id="3f0c9-158">Se la matrice di playlist recuperata contiene esattamente una playlist, esiste una playlist con tale nome nella libreria.</span><span class="sxs-lookup"><span data-stu-id="3f0c9-158">If the playlist array retrieved contains exactly one playlist, then there exists a playlist with that name in the library.</span></span> <span data-ttu-id="3f0c9-159">In caso contrario, la matrice della playlist non conterrà alcun oggetto playlist; Ciò significa che nella libreria non è presente alcuna playlist con il nome passato come argomento al metodo **GetByName** .</span><span class="sxs-lookup"><span data-stu-id="3f0c9-159">Otherwise, the playlist array will contain no playlist object; this means there is no playlist in the library with the name passed as an argument to the **getByName** method.</span></span> <span data-ttu-id="3f0c9-160">Nell'esempio JScript seguente viene illustrato quanto segue:</span><span class="sxs-lookup"><span data-stu-id="3f0c9-160">The following JScript example demonstrates this:</span></span>


```C++
// Specify an .asx playlist file.
WMP9.URL = "https://www.microsoft.com/someplaylist.asx";

// Open the playlist and start playing the content.
WMP9.controls.play();

// Store the current playlist object.
var pl = WMP9.currentPlaylist;

// Attempt to retrieve from the library 
// a playlist having the same name as the current playlist.
var plarray = WMP9.playlistCollection.getByName(pl.name);

// Test whether the PlaylistArray object, plarray, contains
// a Playlist object.
if (!plarray.count)
   
   // If plarray contains no playlist, then import 
   // the current one.
   WMP9.playlistCollection.importPlaylist(pl);
}

```



## <a name="related-topics"></a><span data-ttu-id="3f0c9-161">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3f0c9-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f0c9-162">**Gestione delle playlist**</span><span class="sxs-lookup"><span data-stu-id="3f0c9-162">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="3f0c9-163">**Guida alla migrazione del modello a oggetti**</span><span class="sxs-lookup"><span data-stu-id="3f0c9-163">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> <dt>

[<span data-ttu-id="3f0c9-164">**Oggetto playlist**</span><span class="sxs-lookup"><span data-stu-id="3f0c9-164">**Playlist Object**</span></span>](playlist-object.md)
</dt> </dl>

 

 





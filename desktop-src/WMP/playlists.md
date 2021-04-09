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
# <a name="playlists"></a>Playlist

Il modello a oggetti del controllo ActiveX di Windows Media Player 6,4 include quattro metodi e una proprietà per l'utilizzo delle playlist di metafile di Windows Media:

-   *Player6*. **GetCurrentEntry**
-   *Player6*. **SetCurrentEntry**
-   *Player6*. **GetMediaParameter**
-   *Player6*. **GetMediaParameterName**
-   *Player6*. **EntryCount**.

Insieme, offrono funzionalità limitate per lo spostamento in un metafile della playlist con estensione asx e per il recupero di informazioni sulle voci contenute nella playlist.

In Windows Media Player 7 è stato introdotto "Catalogo multimediale". La libreria consente agli utenti di organizzare il contenuto multimediale digitale, nonché di creare playlist personalizzate che possono essere gestite dall'interfaccia utente grafica del lettore. Il modello a oggetti del controllo ActiveX di Windows Media Player 7 o versione successiva fornisce il supporto per l'utilizzo delle playlist della libreria, nonché delle playlist contenute nei file di Windows Media con estensione asx.

> [!Note]  
> Per motivi di sicurezza, l'utente deve concedere i diritti di accesso alla libreria prima che il programma possa modificare il contenuto. I diritti di accesso possono essere richiesti e concessi solo tramite il modello a oggetti di Windows Media Player 9 o versione successiva. Per informazioni dettagliate sui diritti di accesso, vedere [accesso alla libreria](library-access.md).

 

Il modello a oggetti di Windows Media Player 7 o versione successiva include tre oggetti per la gestione delle playlist. L'oggetto **PlaylistCollection** fornisce funzionalità per l'organizzazione delle playlist; rappresenta l'intera raccolta di playlist nella libreria dell'utente. L'oggetto **PlaylistArray** fornisce un modo per recuperare una playlist specifica dall'oggetto **PlaylistCollection** usando un numero di indice; due dei metodi dell'oggetto **PlaylistCollection** recuperano un oggetto **PlaylistArray** . L'oggetto **playlist** fornisce le proprietà e i metodi necessari per modificare gli elementi multimediali contenuti in una singola playlist.

Ad esempio, poiché ogni playlist nella libreria ha un nome univoco, è possibile recuperare una playlist dalla libreria usando *PlaylistCollection*. metodo **GetByName** :


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



Si vuole usare più spesso la playlist corrente. Sebbene sia possibile usare diversi oggetti playlist, solo uno può essere recuperato dal *lettore*. proprietà **currentPlaylist** in un determinato momento: quello che Windows Media Player sta elaborando in quel momento.

Quando Windows Media Player 7 o versione successiva riproduce un metafile di Windows Media con estensione asx, viene innanzitutto creato un oggetto **playlist** . Quindi, riempie l'oggetto con le informazioni dalla playlist. asx, quindi rende l'oggetto **playlist** corrente la playlist corrente. Ciò significa che è possibile utilizzare le proprietà e i metodi associati all'oggetto **playlist** per modificare le playlist. asx esattamente come si gestiranno le playlist nella libreria. Ad esempio, per recuperare il numero di voci in una playlist con estensione asx usando il modello a oggetti della versione 6,4, usare *Player6*. Proprietà **EntryCount** :


```C++
var entrycount = WMP64.EntryCount;

```



Quando si usa il modello a oggetti di Windows Media Player 7 o versione successiva, si usa la *playlist*. proprietà **count** :


```C++
var entrycount = WMP9.currentPlaylist.count;

```



Quando si usa il controllo versione 6,4, è possibile usare *Player6*. Metodo **GetCurrentEntry** per recuperare l'indice della voce corrente in una playlist. asx:


```C++
var entrynum = WMP64.GetCurrentEntry();

```



È possibile ottenere lo stesso risultato usando il modello a oggetti di Windows Media Player 7 o versione successiva nello script. Nell'esempio JScript seguente viene confrontato l'oggetto multimediale corrente con ogni elemento della playlist. Quando il *supporto*.  il risultato è true. una finestra di messaggio Visualizza l'indice dell'elemento multimediale corrente.


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



Per specificare l'indice della voce corrente in una playlist. asx, usare *Player6*. **SetCurrentEntry**. Gli indici di voci della playlist nella versione 6,4 iniziano con 1, quindi per rendere la seconda voce in una playlist di metafile quella corrente, usare la sintassi seguente:


```C++
WMP6.SetCurrentEntry(2);

```



Gli indici di voci della playlist sono basati su zero in Windows Media Player 7 o versioni successive. per rendere la seconda voce in una playlist di metafile quella corrente, quando si usa il modello a oggetti di Windows Media Player 7 o versione successiva, usare la sintassi seguente:


```C++
WMP9.controls.currentItem = WMP9.currentPlaylist.item(1);

```



Nell'esempio JScript riportato di seguito viene illustrata una funzione che accetta un numero di indice come parametro e quindi rende la voce della playlist corrispondente all'indice dell'elemento multimediale corrente:


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



I metafile di Windows Media possono contenere elementi di parametri personalizzati, che è possibile specificare usando il **<PARAM>** tag. Quando si usa il modello a oggetti versione 6,4, è possibile recuperare il nome di un parametro specifico con *Player6*. Metodo **GetMediaParameterName** . Nell'esempio JScript seguente viene recuperato il nome del primo parametro nella prima voce di una playlist. asx:


```C++
var paramname = WMP6.GetMediaParameterName(1,1);

```



Analogamente, è possibile recuperare il valore associato al parametro usando *Player6*. **GetMediaParameter**:


```C++
var paramvalue = WMP6.GetMediaParameter(1, paramname);

```



Nell'esempio di codice JScript seguente viene usato il modello a oggetti di Windows Media Player 7 o versione successiva per recuperare il nome e il valore del parametro dalla prima voce di una playlist. asx:


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



È possibile usare *PlaylistCollection*. metodo **importPlaylist** per aggiungere una playlist. asx alla libreria. Una volta importato, la playlist del metafile diventa una playlist di libreria, in modo da poterla modificare usando tutte le proprietà e i metodi a sua disposizione. L'utente deve concedere diritti di accesso completi alla libreria per consentire all'applicazione di usare il metodo **importPlaylist** .

È possibile usare *PlaylistCollection*. **GetByName** per verificare se esiste una playlist. Questo metodo restituisce sempre un oggetto **PlaylistArray** valido. Se la matrice di playlist recuperata contiene esattamente una playlist, esiste una playlist con tale nome nella libreria. In caso contrario, la matrice della playlist non conterrà alcun oggetto playlist; Ciò significa che nella libreria non è presente alcuna playlist con il nome passato come argomento al metodo **GetByName** . Nell'esempio JScript seguente viene illustrato quanto segue:


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Gestione delle playlist**](managing-playlists.md)
</dt> <dt>

[**Guida alla migrazione del modello a oggetti**](object-model-migration-guide.md)
</dt> <dt>

[**Oggetto playlist**](playlist-object.md)
</dt> </dl>

 

 





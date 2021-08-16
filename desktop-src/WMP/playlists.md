---
title: Playlist
description: Playlist
ms.assetid: b1ac9208-33d1-448f-9e2e-920fad9c6add
keywords:
- Windows Media Player,playlist
- Windows Media Player a oggetti, playlist
- modello a oggetti, playlist
- Windows Media Player ActiveX, playlist
- ActiveX controllo, playlist
- Windows Media Player controllo ActiveX per dispositivi mobili,playlist
- Windows Media Player dispositivi mobili, playlist
- playlist, migrazione
- Windows playlist di metafile multimediali, migrazione
- playlist di metafile, migrazione
- guida alla migrazione, playlist
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bccdd98789de6c8d4faa06882376967298646febabd790067710dc4f460ba65b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118334474"
---
# <a name="playlists"></a>Playlist

Il Windows Media Player a oggetti del controllo ActiveX 6.4 include quattro metodi e una proprietà per l'uso Windows playlist di metafile multimediali:

-   *Player6*. **GetCurrentEntry**
-   *Player6*. **SetCurrentEntry**
-   *Player6*. **GetMediaParameter**
-   *Player6*. **GetMediaParameterName**
-   *Player6*. **EntryCount**.

Insieme, offrono funzionalità limitate per l'esplorazione di un metafile di playlist con estensione asx e il recupero di informazioni sulle voci contenute nella playlist.

Windows Media Player 7 ha introdotto "Catalogo multimediale". La libreria consente agli utenti di organizzare il contenuto multimediale digitale, nonché di creare playlist personalizzate che possono essere gestite dall'interfaccia utente grafica di Player. Il modello Windows Media Player a oggetti del controllo ActiveX Windows Media Player 7 o versioni successive fornisce il supporto per l'uso di playlist di libreria, nonché playlist contenute nei metafile di Windows Media con estensione asx.

> [!Note]  
> Per motivi di sicurezza, l'utente deve concedere diritti di accesso alla libreria prima che il programma possa modificarne il contenuto. I diritti di accesso possono essere richiesti e concessi solo tramite il modello a oggetti Windows Media Player serie 9 o versioni successive. Per informazioni dettagliate sui diritti di accesso, vedere [Accesso alla libreria.](library-access.md)

 

Il Windows Media Player a oggetti di Windows Media Player 7 o versione successiva include tre oggetti per la gestione delle playlist. **L'oggetto PlaylistCollection** fornisce funzionalità per organizzare le playlist. rappresenta l'intera raccolta di playlist nella libreria dell'utente. **L'oggetto PlaylistArray** consente di recuperare una playlist specifica dall'oggetto **PlaylistCollection** usando un numero di indice. due dei metodi **dell'oggetto PlaylistCollection** recuperano un **oggetto PlaylistArray.** **L'oggetto Playlist** fornisce le proprietà e i metodi necessari per modificare gli elementi multimediali contenuti in una singola playlist.

Ad esempio, poiché ogni playlist nella libreria ha un nome univoco, è possibile recuperare una playlist dalla libreria usando *PlaylistCollection.* **Metodo getByName:**


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



È più frequente usare la playlist corrente. Anche se è possibile usare diversi oggetti playlist, solo uno può essere recuperato da *Player.* **Proprietà currentPlaylist** in qualsiasi momento: quella che Windows Media Player elabora in quel momento.

Quando Windows Media Player 7 o versione successiva riproduce un metafile di Windows Media con estensione asx, crea prima un **oggetto Playlist.** Successivamente, inserisce nell'oggetto le informazioni della playlist asx e quindi rende tale **oggetto Playlist** la playlist corrente. Ciò significa che è possibile usare le proprietà e i metodi associati all'oggetto **Playlist** per modificare le playlist asx esattamente come si gestiscono le playlist nella libreria. Ad esempio, per recuperare il numero di voci in una playlist asx usando il modello a oggetti della versione 6.4, usare *Player6.* **Proprietà EntryCount:**


```C++
var entrycount = WMP64.EntryCount;

```



Quando si usa il modello Windows Media Player 7 o versione successiva, si usa la *playlist*. **Proprietà count:**


```C++
var entrycount = WMP9.currentPlaylist.count;

```



Quando si usa il controllo versione 6.4, è possibile usare *Player6.* **Metodo GetCurrentEntry** per recuperare l'indice della voce corrente in una playlist asx:


```C++
var entrynum = WMP64.GetCurrentEntry();

```



È possibile ottenere lo stesso risultato usando il modello a oggetti Windows Media Player 7 o versione successiva nello script. Nell'JScript seguente viene confrontato l'oggetto multimediale corrente con ogni elemento nella playlist. Quando *l'oggetto multimediale è*. **isIdentical restituisce** true. In una finestra di messaggio viene visualizzato l'indice dell'elemento multimediale corrente.


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



Per specificare l'indice della voce corrente in una playlist asx, usare *Player6.* **SetCurrentEntry**. Gli indici delle voci di playlist nella versione 6.4 iniziano con 1, quindi per impostare la seconda voce in una playlist di metafile su quella corrente, usare la sintassi seguente:


```C++
WMP6.SetCurrentEntry(2);

```



Gli indici delle voci di playlist sono in base zero in Windows Media Player 7 o versioni successive; per impostare la seconda voce in una playlist di metafile come corrente, quando si usa il modello a oggetti Windows Media Player 7 o versione successiva, usare la sintassi seguente:


```C++
WMP9.controls.currentItem = WMP9.currentPlaylist.item(1);

```



Nell'JScript seguente viene illustrata una funzione che accetta un numero di indice come parametro e quindi imposta la voce della playlist che corrisponde all'indice come elemento multimediale corrente:


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



Windows I metafile multimediali possono contenere elementi parametro personalizzati, che è possibile specificare usando il **<PARAM>** tag . Quando si usa il modello a oggetti della versione 6.4, è possibile recuperare il nome di un parametro specifico con *Player6.* **Metodo GetMediaParameterName.** Nell'JScript seguente viene recuperato il nome del primo parametro nella prima voce di una playlist asx:


```C++
var paramname = WMP6.GetMediaParameterName(1,1);

```



Analogamente, è possibile recuperare il valore associato al parametro usando *Player6.* **GetMediaParameter**:


```C++
var paramvalue = WMP6.GetMediaParameter(1, paramname);

```



Nell'JScript seguente viene utilizzato il modello a oggetti Windows Media Player 7 o versione successiva per recuperare il nome e il valore del parametro dalla prima voce di una playlist asx:


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



È possibile usare *PlaylistCollection.* **Metodo importPlaylist** per aggiungere una playlist asx alla libreria. Dopo l'importazione, la playlist del metafile diventa una playlist della libreria, quindi è possibile modificarla usando tutte le proprietà e i metodi disponibili. L'utente deve concedere diritti di accesso completi alla libreria per consentire all'applicazione di usare il **metodo importPlaylist.**

È possibile usare *PlaylistCollection.* **getByName per** verificare se esiste una playlist. Questo metodo restituisce sempre un oggetto **PlaylistArray** valido. Se la matrice di playlist recuperata contiene esattamente una playlist, esiste una playlist con tale nome nella libreria. In caso contrario, la matrice di playlist non conterrà alcun oggetto playlist. Ciò significa che non è presente alcuna playlist nella libreria con il nome passato come argomento al **metodo getByName.** Nell'esempio JScript seguente viene illustrato quanto segue:


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

[**Oggetto Playlist**](playlist-object.md)
</dt> </dl>

 

 





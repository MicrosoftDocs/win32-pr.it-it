---
title: Uso del modello a oggetti Windows Media Player 7 o versioni successive
description: Uso del modello a oggetti Windows Media Player 7 o versioni successive
ms.assetid: e2dbe2c1-23be-499b-b754-b7e87486ecd6
keywords:
- Windows Media Player, modello a oggetti
- Windows Media Player a oggetti, versione 7 o successiva
- modello a oggetti, versione 7 o successiva
- Windows Media Player ActiveX, versione 7 o successiva
- ActiveX, versione 7 o successiva
- Windows Media Player Controllo ActiveX per dispositivi mobili, versione 7 o successiva
- Windows Media Player Dispositivi mobili, modello a oggetti
- guida alla migrazione, versione 7 o successiva
- versioni di Windows Media Player, modello a oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa40dea2718c602bfae305703913b418d0f8a48b90278683aba099dfe0d703bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118117029"
---
# <a name="using-the-windows-media-player-7-or-later-object-model"></a>Uso del modello a oggetti Windows Media Player 7 o versioni successive

La maggior parte delle attività che potrebbero essere state eseguite usando il modello Windows Media Player 6.4 ActiveX a oggetti del controllo richiederà un nuovo approccio. In molti casi, i nomi delle proprietà, dei metodi e degli eventi sono cambiati nel modello a oggetti Windows Media Player 7 o versione successiva. Ad esempio, per specificare il percorso del file nel modello a oggetti della versione 6.4, impostare la proprietà **Player6.FileName:**


```C++
WMP64.FileName = "https://www.microsoft.com/somefile.wmv";

```



Quando si usa il modello Windows Media Player 7 o versione successiva, è necessario impostare la **proprietà Player.URL:**


```C++
WMP9.URL = "https://www.microsoft.com/somefile.wmv";

```



In alternativa, usando il modello a oggetti 10, è possibile ottenere un oggetto **Media** dalla libreria e quindi impostare la **proprietà Player.currentMedia:**


```C++
// Get the first media object in the media collection.
var MyMediaItem = WMP9.mediaCollection.getAll().item(0)

// Make the MyMediaItem object the current media.
WMP9.currentMedia = MyMediaItem;

```



Gran parte delle funzionalità del modello a oggetti Windows Media Player 7 o versione successiva è accessibile tramite la gerarchia di oggetti. Come illustrato nell'esempio precedente, è possibile ottenere un oggetto **Playlist** usando il **metodo getAll** dell'oggetto **mediaCollection,** a cui si accede tramite l'oggetto **Player** radice. È quindi possibile ottenere un particolare **oggetto Media** dall'oggetto **Playlist** usando il **metodo item** dell'oggetto **Playlist.** Sono disponibili cinque metodi aggiuntivi accessibili tramite **l'oggetto mediaCollection** che restituiscono un **oggetto Playlist.** ogni metodo consente di recuperare l'oggetto in base a criteri specifici, ad esempio genere o album.

La struttura gerarchica del modello a oggetti del controllo Windows Media Player 7 o versione successiva ActiveX offre un approccio più logico per organizzare le proprietà, i metodi e gli eventi disponibili per l'uso. Tutte le funzionalità per i controlli Player sono contenute nell'oggetto **Controls,** tutte le funzionalità per la connessione di rete del lettore sono contenute nell'oggetto **Network** e così via. Ad esempio, per avviare la riproduzione del contenuto usando il modello a oggetti della versione 6.4, usare il **metodo Player6.Play:**


```C++
WMP64.Play();

```



Quando si usa il Windows Media Player a oggetti di Windows Media Player 7 o versione successiva, è necessario accedere al metodo **Play** usando l'oggetto **Controls:**


```C++
WMP9.controls.play();

```



La profondità del modello a oggetti, tuttavia, può causare istruzioni script molto lunghe:


```C++
WMP9.currentPlaylist.appendItem(WMP9.mediaCollection.getByName("MySong").item(0));

```



Istruzioni come quella precedente possono essere rese molto più semplici e leggibili usando singoli oggetti denominati. L'esempio seguente sostituisce l'istruzione di codice precedente con la sintassi usando variabili oggetto separate:


```C++
// Store the current playlist object.
var pl = WMP9.currentPlaylist;

// Get a playlist from the media collection that contains
// one media item named "MySong".
var temp = WMP9.mediaCollection.getByName("MySong");

// Get the individual media item from the temp playlist.
var song = temp.item(0);

// Append the media item to the current playlist.
pl.appendItem(song);

```



Questo stile di codifica richiede più righe di script, ma è molto più semplice da seguire, soprattutto con i commenti aggiunti. Esiste un altro vantaggio: **l'oggetto currentPlaylist** è facile da riutilizzare perché è archiviato nella variabile pl.

Molte delle proprietà, dei metodi e degli eventi nel modello a oggetti di Windows Media Player 7 o versioni successive impostano o recuperano valori diversi oppure restituiscono valori di un tipo o un numero diverso rispetto alle funzionalità corrispondenti nel modello a oggetti della versione 6.4. Ad esempio, quando **Player6.openState** recupera 2, tale valore corrisponde alla costante **Visual Basic nsLoadingNSC,** ovvero il lettore sta caricando un file di stazione con estensione nsc. Tuttavia, quando la proprietà **player.openState** del modello a oggetti di Windows Media Player 7 o versioni successive recupera 2, tale valore corrisponde allo stato PlaylistLocating, vale a dire che Windows Media Player sta tentando di individuare una playlist. Inoltre, la **proprietà Player6.openState** può recuperare sette valori diversi, mentre la proprietà Windows Media Player 7 o versioni successive **Player.openState** può recuperare 22 valori diversi. Assicurarsi di fare riferimento alla sezione Object Model Reference for Scripting (Riferimento al modello a oggetti per script) di Windows Media Player SDK quando si rivede il codice per usare una versione diversa del modello a oggetti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sul modello a oggetti del lettore**](about-the-player-object-model.md)
</dt> <dt>

[**Informazioni di riferimento sul modello a oggetti per lo scripting**](object-model-reference-for-scripting.md)
</dt> <dt>

[**Guida alla migrazione del modello a oggetti**](object-model-migration-guide.md)
</dt> </dl>

 

 





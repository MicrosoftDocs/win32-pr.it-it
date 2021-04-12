---
title: Uso del modello a oggetti di Windows Media Player 7 o versione successiva
description: Uso del modello a oggetti di Windows Media Player 7 o versione successiva
ms.assetid: e2dbe2c1-23be-499b-b754-b7e87486ecd6
keywords:
- Windows Media Player, modello a oggetti
- Modello a oggetti di Windows Media Player, versione 7 o successiva
- modello a oggetti, versione 7 o successiva
- Controllo ActiveX di Windows Media Player versione 7 o successiva
- Controllo ActiveX, versione 7 o successiva
- Controllo ActiveX Windows Media Player Mobile versione 7 o successiva
- Windows Media Player Mobile, modello a oggetti
- Guida alla migrazione, 7 o versione successiva
- versioni di Windows Media Player, modello a oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8eb4d3d09b38e381d0cddeb25ee7cb5d7de3cb2b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330708"
---
# <a name="using-the-windows-media-player-7-or-later-object-model"></a>Uso del modello a oggetti di Windows Media Player 7 o versione successiva

La maggior parte delle attività che potrebbero essere state eseguite utilizzando il modello a oggetti del controllo ActiveX di Windows Media Player 6,4 richiederà un nuovo approccio. In molti casi, i nomi delle proprietà, dei metodi e degli eventi sono stati modificati nel modello a oggetti di Windows Media Player 7 o versioni successive. Ad esempio, per specificare il percorso del file nel modello a oggetti della versione 6,4, impostare la proprietà **Player6. FileName** :


```C++
WMP64.FileName = "https://www.microsoft.com/somefile.wmv";

```



Quando si usa il modello a oggetti di Windows Media Player 7 o versione successiva, è necessario impostare la proprietà **Player. URL** :


```C++
WMP9.URL = "https://www.microsoft.com/somefile.wmv";

```



In alternativa, usando il modello a oggetti 10, è possibile ottenere un oggetto **multimediale** dalla libreria, quindi impostare la proprietà **Player. currentMedia** :


```C++
// Get the first media object in the media collection.
var MyMediaItem = WMP9.mediaCollection.getAll().item(0)

// Make the MyMediaItem object the current media.
WMP9.currentMedia = MyMediaItem;

```



Gran parte delle funzionalità del modello a oggetti di Windows Media Player 7 o versione successiva è accessibile tramite la gerarchia di oggetti. Come illustrato nell'esempio precedente, è possibile ottenere un oggetto **playlist** usando il metodo **GetAll** dell'oggetto **mediacollection** , a cui si accede tramite l'oggetto **Player** radice. È quindi possibile ottenere un oggetto **multimediale** particolare dall'oggetto **playlist** usando il metodo **Item** dell'oggetto **playlist** . Esistono cinque metodi aggiuntivi accessibili tramite l'oggetto **mediacollection** che restituiscono un oggetto **playlist** ; ogni metodo consente di recuperare l'oggetto in base a criteri specifici, ad esempio genere o album.

La struttura gerarchica del modello a oggetti del controllo ActiveX Windows Media Player 7 o versioni successive offre un approccio più logico per organizzare le proprietà, i metodi e gli eventi disponibili per l'uso. Tutte le funzionalità per i controlli Player sono contenute nell'oggetto **Controls** , tutte le funzionalità della connessione di rete Player sono contenute nell'oggetto di **rete** e così via. Ad esempio, per avviare la riproduzione del contenuto utilizzando il modello a oggetti della versione 6,4, utilizzare il metodo **Player6. Play** :


```C++
WMP64.Play();

```



Quando si usa il modello a oggetti di Windows Media Player 7 o versione successiva, è necessario accedere al metodo **Play** usando l'oggetto **Controls** :


```C++
WMP9.controls.play();

```



La profondità del modello a oggetti, tuttavia, può causare istruzioni script molto lunghe:


```C++
WMP9.currentPlaylist.appendItem(WMP9.mediaCollection.getByName("MySong").item(0));

```



Le istruzioni come la precedente possono essere rese molto più semplici e più leggibili tramite l'utilizzo di singoli oggetti denominati. Nell'esempio seguente l'istruzione del codice precedente viene sostituita con la sintassi utilizzando variabili oggetto separate:


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



Questo stile di codifica richiede più righe di script, ma è molto più semplice da seguire, soprattutto con i commenti aggiunti. Un altro vantaggio: l'oggetto **currentPlaylist** è facile da riutilizzare perché è archiviato nella variabile pl.

Molte proprietà, metodi ed eventi nel modello a oggetti di Windows Media Player 7 o versione successiva impostano o recuperano valori diversi oppure restituiscono valori di un tipo o di un numero diverso rispetto alla funzionalità corrispondente nel modello a oggetti della versione 6,4. Ad esempio, quando **Player6. openState** recupera 2, tale valore corrisponde alla costante Visual Basic **nsLoadingNSC**, vale a dire che il lettore sta caricando un file di stazione con estensione NSC. Tuttavia, quando **la proprietà del** modello a oggetti di Windows Media Player 7 o versione successiva restituisce 2, tale valore corrisponde allo stato PlaylistLocating, ovvero Windows Media Player sta tentando di individuare una playlist. Inoltre, la proprietà **Player6. openState** può recuperare sette valori diversi, mentre la proprietà **Player. openState** di Windows Media Player 7 o versione successiva può recuperare 22 valori diversi. Assicurarsi di fare riferimento al riferimento del modello a oggetti per la sezione scripting di Windows Media Player SDK durante la revisione del codice per l'utilizzo di una versione diversa del modello a oggetti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sul modello a oggetti del lettore**](about-the-player-object-model.md)
</dt> <dt>

[**Riferimento del modello a oggetti per lo scripting**](object-model-reference-for-scripting.md)
</dt> <dt>

[**Guida alla migrazione del modello a oggetti**](object-model-migration-guide.md)
</dt> </dl>

 

 





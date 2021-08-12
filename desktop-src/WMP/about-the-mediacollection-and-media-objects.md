---
title: Informazioni sugli oggetti MediaCollection e Media
description: Informazioni sugli oggetti MediaCollection e Media
ms.assetid: e3260efd-44cc-4b4e-9f48-3441631bfa4f
keywords:
- Windows Media Player,Oggetto MediaCollection
- Windows Media Player a oggetti, oggetto MediaCollection
- modello a oggetti, oggetto MediaCollection
- Windows Media Player ActiveX, oggetto MediaCollection
- ActiveX, oggetto MediaCollection
- Windows Media Player Mobile ActiveX control,MediaCollection object
- Windows Media Player Mobile, oggetto MediaCollection
- Oggetto MediaCollection
- Windows Media Player,Oggetto Media
- Windows Media Player a oggetti, oggetto Media
- modello a oggetti, oggetto multimediale
- Windows Media Player ActiveX, oggetto Media
- ActiveX, oggetto Media
- Windows Media Player Mobile ActiveX control,Media object
- Windows Media Player Mobile, oggetto Media
- Oggetto multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 082bea6eb3707915422a0bfa5cba63a2a999ac8df27ffa13876e74ffcfc6a882
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583683"
---
# <a name="about-the-mediacollection-and-media-objects"></a>Informazioni sugli oggetti MediaCollection e Media

Gli **oggetti MediaCollection** **e Media** regolano la raccolta multimediale, che definisce le posizioni dei file multimediali digitali a cui Windows Media Player possibile accedere. Ottieni **l'oggetto MediaCollection** dalla **proprietà mediaCollection** dell'oggetto **Player.** La **proprietà mediaCollection** restituisce l'oggetto **MediaCollection.** È possibile accedere alle proprietà **dell'oggetto MediaCollection** solo dopo che è stato creato. Ad esempio, per aggiungere un **oggetto Media** (brano), usare il codice seguente:


```C++
player.mediacollection.add('laure.wma');

```



Il file laure.wma è stato aggiunto alla raccolta di supporti.

È possibile ottenere **l'oggetto Multimediale** corrente usando la **proprietà currentMedia** di **Player.** Ad esempio, questo codice ottiene la **proprietà duration** dell'oggetto **Media** corrente:


```C++
myduration = player.currentmedia.duration;

```



Esistono diversi modi per ottenere un oggetto **Media** in modo da poter accedere alle relative proprietà. Ad esempio, se si vuole accedere alla proprietà **duration** del supporto corrente, è possibile usare ognuna delle righe di codice seguenti.

Per ottenere la durata del contenuto multimediale attualmente in riproduzione:


```C++
player.currentMedia.duration;

```



Per ottenere la durata del supporto corrente in una playlist:


```C++
player.controls.currentItem.duration;

```



Per ottenere la durata del terzo elemento multimediale in una playlist:


```C++
player.currentPlaylist.item(2).duration;

```



Per ottenere la durata del terzo elemento multimediale in un genere "Jazz":


```C++
player.mediaCollection.getByGenre("jazz").item(2).duration;

```



Per ottenere la durata del terzo elemento multimediale nella seconda playlist:


```C++
player.playlistCollection.getAll.item(1).item(2).duration; 
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> <dt>

[**Oggetto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Modello a oggetti del lettore per linguaggi di scripting**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 





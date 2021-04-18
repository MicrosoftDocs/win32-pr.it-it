---
title: Informazioni sugli oggetti Mediacollection e media
description: Informazioni sugli oggetti Mediacollection e media
ms.assetid: e3260efd-44cc-4b4e-9f48-3441631bfa4f
keywords:
- Windows Media Player, oggetto Mediacollection
- Modello a oggetti di Windows Media Player, oggetto Mediacollection
- modello a oggetti, oggetto Mediacollection
- Controllo ActiveX Windows Media Player, oggetto Mediacollection
- Controllo ActiveX, oggetto Mediacollection
- Controllo ActiveX Windows Media Player Mobile, oggetto Mediacollection
- Windows Media Player Mobile, oggetto Mediacollection
- Mediacollection (oggetto)
- Windows Media Player, oggetto multimediale
- Modello a oggetti di Windows Media Player, oggetto multimediale
- modello a oggetti, oggetto multimediale
- Controllo ActiveX Windows Media Player, oggetto multimediale
- Controllo ActiveX, oggetto multimediale
- Controllo ActiveX Windows Media Player Mobile, oggetto multimediale
- Windows Media Player Mobile, oggetto multimediale
- Oggetto multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe902fd9ed046e0197fb5c8c2d995d26befafe29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298590"
---
# <a name="about-the-mediacollection-and-media-objects"></a>Informazioni sugli oggetti Mediacollection e media

**Mediacollection** e gli oggetti **multimediali** regolano la raccolta di supporti, che definisce le posizioni dei file multimediali digitali a cui può accedere Windows Media Player. Si ottiene l'oggetto **mediacollection** dalla proprietà **mediacollection** dell'oggetto **Player** . La proprietà **mediacollection** restituisce l'oggetto **mediacollection** . È possibile accedere alle proprietà dell'oggetto **mediacollection** solo dopo averlo creato. Ad esempio, per aggiungere un oggetto **multimediale** (un brano), usare il codice seguente:


```C++
player.mediacollection.add('laure.wma');

```



Il file Laure. WMA è stato aggiunto alla raccolta di supporti.

È possibile ottenere l'oggetto **multimediale** corrente usando la proprietà **currentMedia** del **lettore**. Questo codice, ad esempio, ottiene la proprietà **Duration** dell'oggetto **multimediale** corrente:


```C++
myduration = player.currentmedia.duration;

```



Esistono diversi modi per ottenere un oggetto **multimediale** per poter accedere alle relative proprietà. Se ad esempio si vuole accedere alla proprietà **Duration** del supporto corrente, è possibile usare ognuna delle righe di codice seguenti.

Per ottenere la durata del supporto attualmente in riproduzione:


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

[**Mediacollection (oggetto)**](mediacollection-object.md)
</dt> <dt>

[**Modello a oggetti del lettore per i linguaggi di scripting**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 





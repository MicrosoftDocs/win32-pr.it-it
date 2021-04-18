---
title: Corrispondenza dei colori di Windows Media Player
description: Corrispondenza dei colori di Windows Media Player
ms.assetid: b4d1da08-a4cf-46dd-82a5-40562bb3c049
keywords:
- Windows Media Player Online Stores, corrispondenti colori di Windows Media Player
- negozi online, corrispondenti colori di Windows Media Player
- digitare 1 negozi online, corrispondenti colori di Windows Media Player
- digitare 2 archivi online, corrispondenti colori di Windows Media Player
- Windows Media Player Online Stores, Windows Media Player color matching
- archivi online, corrispondenza colori Windows Media Player
- digitare 1 archivi online, corrispondenza colori Windows Media Player
- digitare 2 archivi online, corrispondenza colori Windows Media Player
- Windows Media Player Online Stores, corrispondenza colori per Windows Media Player
- negozi online, corrispondenza dei colori per Windows Media Player
- digitare 1 negozi online, corrispondenza dei colori per Windows Media Player
- digitare 2 negozi online, corrispondenza dei colori per Windows Media Player
- corrispondenza dei colori per Windows Media Player
- colori corrispondenti di Windows Media Player
- Windows Media Player, colori corrispondenti
- Windows Media Player, corrispondenza colori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eedf3e5df7c02f498c0dc21aeeed16c99452003c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298715"
---
# <a name="matching-the-windows-media-player-colors"></a>Corrispondenza dei colori di Windows Media Player

La creazione di una pagina Web di archivio online corrisponde alla combinazione di colori di Windows Media Player. È sufficiente gestire l'evento **External. OnColorChange** . Per specificare una funzione per gestire l'evento, usare codice simile al seguente quando viene caricata la pagina Web:


```C++
// Set up the color change event.
external.OnColorChange = OnAppColor;
```



Ogni volta che l'utente modifica la combinazione di colori di Windows Media Player, il lettore chiamerà la funzione. Nell'esempio seguente viene illustrata una funzione semplice che imposta lo sfondo della pagina Web in modo che corrisponda alla proprietà **External. appColorLight** :


```C++
// Match the current color.
function OnAppColor()
{
    window.document.bgColor = external.appColorLight;
}
```



Sono disponibili anche altre proprietà di colore per l'uso. Vedere [oggetto esterno per gli archivi online di tipo 2](external-object-for-type-2-online-stores.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**External. appColorLight**](external-appcolorlight.md)
</dt> <dt>

[**Evento External. OnColorChange**](external-oncolorchange-event.md)
</dt> <dt>

[**Informazioni comuni ai negozi online di tipo 1 e di tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 





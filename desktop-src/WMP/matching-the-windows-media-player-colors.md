---
title: Corrispondenza dei Windows Media Player colori
description: Corrispondenza dei Windows Media Player colori
ms.assetid: b4d1da08-a4cf-46dd-82a5-40562bb3c049
keywords:
- Windows Media Player online, corrispondenza con Windows Media Player colori
- online store, corrispondenza con Windows Media Player colori
- type 1 online stores,matching Windows Media Player colors
- tipo 2 negozi online, corrispondenza con Windows Media Player colori
- Windows Media Player punti vendita online, Windows Media Player colori corrispondenti
- online store, corrispondenza Windows Media Player colori
- type 1 online stores,Windows Media Player color matching
- Store online di tipo 2, corrispondenza Windows Media Player colori
- Windows Media Player online, corrispondenza colori per Windows Media Player
- negozi online, corrispondenza dei colori per Windows Media Player
- type 1 online stores,color matching for Windows Media Player
- type 2 online stores,color matching for Windows Media Player
- corrispondenza dei colori per Windows Media Player
- colori Windows Media Player corrispondenti
- Windows Media Player, colori corrispondenti
- Windows Media Player,corrispondenza colori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3dbb7ed8b73973d35bc8ad884109c569d1c4738d038cf48f657068c5bde51bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135184"
---
# <a name="matching-the-windows-media-player-colors"></a>Corrispondenza dei Windows Media Player colori

Fare in modo che la pagina Web dello store online corrisponda Windows Media Player combinazione di colori è semplice. È sufficiente gestire **l'evento External.OnColorChange.** Per specificare una funzione per gestire l'evento, usare codice simile al seguente quando viene caricata la pagina Web:


```C++
// Set up the color change event.
external.OnColorChange = OnAppColor;
```



Ogni volta che l'utente modifica la combinazione di colori Windows Media Player, il lettore chiamerà la funzione . L'esempio seguente illustra una semplice funzione che imposta lo sfondo della pagina Web in modo che corrisponda alla **proprietà External.appColorLight:**


```C++
// Match the current color.
function OnAppColor()
{
    window.document.bgColor = external.appColorLight;
}
```



Sono disponibili anche altre proprietà di colore per l'uso. Vedere [Oggetto esterno per i negozi online di tipo 2.](external-object-for-type-2-online-stores.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**External.appColorLight**](external-appcolorlight.md)
</dt> <dt>

[**Evento External.OnColorChange**](external-oncolorchange-event.md)
</dt> <dt>

[**Informazioni comuni ai negozi online di tipo 1 e di tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 





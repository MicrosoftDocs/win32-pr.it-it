---
title: Album artistico
description: Album artistico
ms.assetid: a5996232-e1ee-41ae-a6ca-f841321644fe
keywords:
- Windows Media Player Mobile Skins, album Art
- Skin, album Art
- informazioni di riferimento per Skins, album Art
- file di immagine per Skins, album Art
- Album Art in Skins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0974f8683da98469e75a4472d086dcb1a244c75
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298028"
---
# <a name="album-art"></a>Album artistico

Quando si crea un'interfaccia per Windows Media Player 10 mobile o versione successiva, è possibile che si desideri visualizzare gli album grafici che fanno riferimento all'elemento multimediale attualmente in riproduzione. Quando si progetta l'interfaccia, è consigliabile riservare spazio nell'immagine di sfondo per contenere l'immagine dell'album.

La sezione album art del file di definizione dell'interfaccia deve iniziare con la riga seguente:


```C++
[ Album Art ]

```



È quindi necessario aggiungere le informazioni che specificano la posizione e le dimensioni dell'immagine dell'album nell'interfaccia. È necessario immettere quattro numeri interi positivi, separati da virgole che definiscono la sinistra, la parte superiore, la larghezza e l'altezza dell'arte dell'album, in pixel, rispetto all'immagine di sfondo. Nell'esempio seguente viene illustrato come specificare le dimensioni:


```C++
//  <Location>
//  ----------
   5,37,230,155

```



Se si prevede di includere una sezione video nell'interfaccia utente, è possibile usare le stesse dimensioni e la stessa posizione per l'arte degli album per conservare spazio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Riferimento all'interfaccia**](skin-reference.md)
</dt> </dl>

 

 





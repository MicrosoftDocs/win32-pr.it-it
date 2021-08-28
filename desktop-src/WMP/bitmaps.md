---
title: Bitmap (Windows Media Player SDK)
description: Bitmap
ms.assetid: cd10bc7d-1167-485e-8acf-13c021bc608b
keywords:
- Windows Media Player Interfaccia per dispositivi mobili, bitmap
- interfaccia, bitmap
- informazioni di riferimento per le interfaccia, bitmap
- bitmap nelle interfaccia, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33ff4689c052162d8addfb9a66aeb6b227916f0e22e21de3e3572ea265380664
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123861"
---
# <a name="bitmaps-windows-media-player-sdk"></a>Bitmap (Windows Media Player SDK)

È necessario usare una o più immagini nell'interfaccia e ogni immagine deve essere definita nel file di definizione dell'interfaccia. Se non si definisce un'immagine in questa sezione, l'interfaccia non sarà in grado di usarla.

Il termine "bitmap" viene usato in tutto il riferimento in senso generico e fa riferimento alle immagini bitmap con estensione .bmp, alle immagini GIF con estensione .gif, alle immagini JPEG con estensione .jpg e alle immagini PNG con estensione .png.

La sezione Bitmaps del file di definizione dell'interfaccia inizia con questa riga:


```C++
[ Bitmaps ]

```



È quindi necessario aggiungere una o più righe contenenti informazioni su ognuna delle immagini nell'interfaccia.

Una linea tipica potrebbe essere:


```C++
    Background  Background.bmp  0,0

```



È possibile usare il modello seguente per la sezione Bitmaps del file di definizione dell'interfaccia:


```C++
//  <Type>      <Filename>      <X,Y>
//  ------      -----------     -----

```



È necessario usare l'ordine seguente per le informazioni bitmap per ogni riga nella sezione Bitmap. Ogni parte della riga è obbligatoria.

1.  [Tipo bitmap](bitmap-type.md)
2.  [Nome file](file-name.md)
3.  [Coordinate](coordinates.md)

Per un esempio di codice bitmap, vedere [sezione Bitmap di esempio.](sample-bitmap-section.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni di riferimento per l'interfaccia**](skin-reference.md)
</dt> </dl>

 

 





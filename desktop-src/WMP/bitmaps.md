---
title: Bitmap (Windows Media Player SDK)
description: Bitmap
ms.assetid: cd10bc7d-1167-485e-8acf-13c021bc608b
keywords:
- Interfacce di Windows Media Player per dispositivi mobili, bitmap
- interfacce, bitmap
- informazioni di riferimento per interfacce, bitmap
- bitmap nelle interfacce, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ad690b691c22154bad4db0981e2b5ab760400b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474764"
---
# <a name="bitmaps-windows-media-player-sdk"></a>Bitmap (Windows Media Player SDK)

È necessario usare una o più immagini nell'interfaccia personalizzata e ogni immagine deve essere definita nel file di definizione dell'interfaccia. Se non si definisce un'immagine in questa sezione, l'interfaccia non sarà in grado di utilizzarla.

Il termine "bitmap" viene usato in tutto il riferimento in senso generico e fa riferimento alle immagini bitmap con estensione bmp, immagini GIF con estensione gif, immagini JPEG con estensione jpg e immagini PNG con estensione png.

La sezione bitmap del file di definizione dell'interfaccia personalizzata inizia con questa riga:


```C++
[ Bitmaps ]

```



È quindi necessario aggiungere una o più righe contenenti informazioni su ognuna delle immagini nell'interfaccia.

Una linea tipica potrebbe essere:


```C++
    Background  Background.bmp  0,0

```



È possibile usare il modello seguente per la sezione bitmap del file di definizione dell'interfaccia personalizzata:


```C++
//  <Type>      <Filename>      <X,Y>
//  ------      -----------     -----

```



Per le informazioni bitmap per ogni riga della sezione bitmap, è necessario utilizzare l'ordine seguente. Ogni parte della riga è obbligatoria.

1.  [Tipo di bitmap](bitmap-type.md)
2.  [Nome file](file-name.md)
3.  [Coordinate](coordinates.md)

Per un esempio di codice bitmap, vedere la [sezione relativa alla bitmap di esempio](sample-bitmap-section.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Riferimento all'interfaccia**](skin-reference.md)
</dt> </dl>

 

 





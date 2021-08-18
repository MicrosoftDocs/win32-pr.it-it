---
title: Sezione bitmap di esempio
description: Sezione bitmap di esempio
ms.assetid: 51b84b34-3cbb-4863-b7dc-e33e80d6ba23
keywords:
- Windows Media Player Interfaccia per dispositivi mobili, bitmap
- interfaccia, bitmap
- informazioni di riferimento per le interfaccia, bitmap
- bitmap nelle interfaccia, sezione Bitmap
- file di definizione dell'interfaccia utente, sezione Bitmaps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de401906896abcdda4728ff0984871ef4a399d3e223b36afd9d585eb0e4fce76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118833395"
---
# <a name="sample-bitmap-section"></a>Sezione bitmap di esempio

Le righe seguenti mostrano una tipica sezione Bitmaps di un file di definizione dell'interfaccia:


```C++
[ Bitmaps ]

//  <Type>      <File name>     <X,Y>
//  ------      -----------     -----
    Background  Background.bmp  0,0
    Disabled    Disabled.bmp    0,0
    Pushed      Pushed.bmp      0,0
    Region      Region.bmp      0,0
    Super       Super.bmp       0,0
    

```



In questo modo vengono definite cinque bitmap usate per creare un'immagine di sfondo, immagini per i pulsanti Disabilitato e Premuto, un'immagine region per i pulsanti dell'area e un'immagine Super per i trackbar.

> [!Note]  
> Le bitmap Region e Super sono deprecate nelle interfaccia per Windows Media Player 10 Mobile o versioni successive.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Bitmap**](bitmaps.md)
</dt> </dl>

 

 





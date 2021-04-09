---
title: Sezione bitmap di esempio
description: Sezione bitmap di esempio
ms.assetid: 51b84b34-3cbb-4863-b7dc-e33e80d6ba23
keywords:
- Interfacce di Windows Media Player per dispositivi mobili, bitmap
- interfacce, bitmap
- informazioni di riferimento per interfacce, bitmap
- bitmap in interfacce, sezione bitmap
- file di definizione dell'interfaccia, sezione bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00b05183be7ba56ed5b00a6bfd26ee6162e008cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856569"
---
# <a name="sample-bitmap-section"></a>Sezione bitmap di esempio

Le righe seguenti mostrano una tipica sezione bitmap di un file di definizione dell'interfaccia personalizzata:


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



Definisce cinque bitmap che vengono usate per creare un'immagine di sfondo, immagini per i pulsanti disabilitati e di cui è stato eseguito il push, un'immagine di area per i pulsanti di area e un'immagine con privilegi avanzati per trackbars.

> [!Note]  
> L'area e le bitmap con privilegi avanzati sono deprecate nelle interfacce per Windows Media Player 10 mobile o versioni successive.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Bitmap**](bitmaps.md)
</dt> </dl>

 

 





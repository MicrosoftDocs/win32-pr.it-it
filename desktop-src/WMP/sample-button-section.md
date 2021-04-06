---
title: Sezione pulsante di esempio
description: Sezione pulsante di esempio
ms.assetid: 52358f83-8c74-4957-87c4-ca1ed7f667fc
keywords:
- Windows Media Player Mobile Skins, sezione Button
- interfacce, sezione Button
- riferimento per Skin, sezione Button
- pulsanti in Skin, sezione Button
- file di definizione dell'interfaccia, sezione Button
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c35a4efd0e52dd7f5fd0cf87fc269eb4a9f4c27
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044957"
---
# <a name="sample-button-section"></a>Sezione pulsante di esempio

Le righe seguenti mostrano una sezione dei pulsanti tipici di un file di definizione dell'interfaccia personalizzata:


```C++
[ Buttons ]

//  <Function> <Type>     <Location>     <Push Image Src>  <Dis Image Src>    <Hit R,G,B>  <Norm 2 Image Src>  <Push 2 Image Src>
//  ---------- ------     ----------     ----------------  ---------------    -----------  ------------------  ------------------
    PlayPause  2PushHit   84,99,67,67   Pushed @ 44,50    Disabled @ 44,50     0,255,255  Pushed @ 160,5      Pushed @ 160,98
    Info       PushHit    97,49,43,43    Pushed @ 57,0     Disabled @ 57,0      0,  0,  0
    Stop       PushHit    97,173,43,43   Pushed @ 57,124   Disabled @ 57,124  255,255,  0
    Prev       PushHit    40,83,43,43    Pushed @ 0,34     Disabled @ 0,34      0,  0,255
    Next       PushHit    153,83,43,43   Pushed @ 113,34   Disabled @ 113,34  255,  0,  0
    Shuffle    ToggleHit  40,136,43,43   Pushed @ 0,87     Disabled @ 0,87      0,255,  0
    Repeat     ToggleHit  153,136,43,43  Pushed @ 113,87   Disabled @ 113,87  255,  0,255
    Mute       Toggle     5,220,24,23    Super @ 247,29    Super @ 4,28         0,  0,  0

```



Questo codice definisce otto pulsanti usati per fornire tutte le funzioni seguenti in un'interfaccia personalizzata:

-   Riprodurre, sospendere e arrestare elementi multimediali.
-   Riproduzione casuale, ripetizione e spostamento nella playlist.
-   Disattivare il volume.

Tutti i pulsanti eccetto il pulsante di silenziamento sono pulsanti dell'area. Il pulsante di silenziamento ottiene le immagini inserite e disabilitate dalla bitmap con privilegi avanzati per praticità.

> [!Note]  
> I tipi di pulsanti sono deprecati nelle interfacce per Windows Media Player 10 mobile o versioni successive. Invece di un tipo di pulsante dichiarato nel file skin, immettere "NA" per ogni tipo.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Pulsanti**](buttons.md)
</dt> </dl>

 

 





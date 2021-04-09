---
description: I sistemi di coordinate per Direct3D 10 sono definiti per pixel e Texel.
ms.assetid: c8c269e7-6e2a-4b5d-847c-6779e276b9af
title: Sistemi di coordinate (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba84cd7d807474a1ff41f873d16cbd7eee07224
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748970"
---
# <a name="coordinate-systems-direct3d-10"></a>Sistemi di coordinate (Direct3D 10)

I sistemi di coordinate per Direct3D 10 sono definiti per pixel e Texel.



|                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Differenze tra Direct3D 9 e Direct3D 10:<br/> Direct3D 10 definisce l'angolo superiore sinistro del pixel superiore sinistro come origine di una destinazione di rendering.<br/> Direct3D 9 definisce il centro del pixel superiore sinistro come origine di una destinazione di rendering.<br/> |



 

-   [Sistema di coordinate pixel](#pixel-coordinate-system)
    -   [Sistema di coordinate pixel per Direct3D 9](#pixel-coordinate-system-for-direct3d-9)
-   [Sistema di coordinate Texel](#texel-coordinate-system)
    -   [Sistema di coordinate Texel](#texel-coordinate-system)
-   [Argomenti correlati](#related-topics)

## <a name="pixel-coordinate-system"></a>Sistema di coordinate pixel

Il sistema di coordinate pixel in Direct3D 10 definisce l'origine di una destinazione di rendering nell'angolo superiore sinistro. come illustrato nel diagramma seguente. I centri pixel sono offset di (0,5 f, 0,5 f) dalle posizioni intere.

![diagramma del sistema di coordinate pixel in Direct3D 10](images/d3d10-coordspix10.png)

### <a name="pixel-coordinate-system-for-direct3d-9"></a>Sistema di coordinate pixel per Direct3D 9

Come riferimento, di seguito è riportato il sistema di coordinate pixel per Direct3D 9, che ha definito l'origine o una destinazione di rendering come centro del pixel superiore sinistro, (0,5, 0,5) dall'angolo superiore sinistro, come illustrato nel diagramma seguente. In Direct3D 9 i pixel Center si trovano in posizioni di tipo Integer.

![diagramma del sistema di coordinate pixel in Direct3D 9](images/d3d10-coordspix9.png)

## <a name="texel-coordinate-system"></a>Sistema di coordinate Texel

Il sistema di coordinate Texel ha origine nell'angolo superiore sinistro della trama, come illustrato nella figura seguente. In questo modo si rende semplice il rendering delle trame allineate allo schermo (in Direct3D 10), perché il sistema di coordinate pixel è allineato con il sistema di coordinate Texel.

![diagramma del sistema di coordinate Texel](images/d3d10-coordstex10.png)

### <a name="texel-coordinate-system"></a>Sistema di coordinate Texel

Le coordinate di trama sono rappresentate con un numero normalizzato o ridimensionato; ogni coordinata di trama viene mappata a un Texel specifico, come indicato di seguito:

Per una coordinata normalizzata:

-   Campionamento di punti: Texel \# = Floor (U \* Width)
-   Campionamento lineare: a sinistra Texel \# = Floor (U \* Width), right Texel \# = Left Texel \# + 1

Per una coordinata ridimensionata:

-   Campionamento di punti: Texel \# = Floor (U)
-   Campionamento lineare: a sinistra Texel \# = Floor (U-0,5), right Texel \# = Left Texel \# + 1

Dove Width è la larghezza della trama (in Texels).

Il wrapping degli indirizzi di trama si verifica dopo il calcolo della posizione di Texel.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 





---
description: I sistemi di coordinate per Direct3D 10 sono definiti per pixel e texel.
ms.assetid: c8c269e7-6e2a-4b5d-847c-6779e276b9af
title: Sistemi di coordinate (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e3da846ae4b989f6d8cb4741f9df8f7228e8970
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335465"
---
# <a name="coordinate-systems-direct3d-10"></a>Sistemi di coordinate (Direct3D 10)

I sistemi di coordinate per Direct3D 10 sono definiti per pixel e texel.



Differenze tra Direct3D 9 e Direct3D 10:

- Direct3D 10 definisce l'angolo superiore sinistro del pixel superiore sinistro come origine di una destinazione di rendering.
- Direct3D 9 definisce il centro del pixel superiore sinistro come origine di una destinazione di rendering.



 

[Sistema di coordinate pixel](#pixel-coordinate-system)
- [Sistema di coordinate pixel per Direct3D 9](#pixel-coordinate-system-for-direct3d-9)

[Sistema di coordinate Texel](#texel-coordinate-system)
- [Sistema di coordinate Texel](#texel-coordinate-system)

[Argomenti correlati](#related-topics)

## <a name="pixel-coordinate-system"></a>Sistema di coordinate pixel

Il sistema di coordinate pixel in Direct3D 10 definisce l'origine di una destinazione di rendering nell'angolo superiore sinistro. come illustrato nel diagramma seguente. I centri pixel vengono offset da (0,5f,0,5f) dalle posizioni di numeri interi.

![diagramma del sistema di coordinate pixel in direct3d 10](images/d3d10-coordspix10.png)

### <a name="pixel-coordinate-system-for-direct3d-9"></a>Sistema di coordinate pixel per Direct3D 9

Come riferimento, di seguito è riportato il sistema di coordinate pixel per Direct3D 9, che ha definito l'origine o una destinazione di rendering come centro del pixel superiore sinistro,(0,5,0.5) lontano dall'angolo superiore sinistro, come illustrato nel diagramma seguente. In Direct3D 9 i pixel center sono in posizioni intere.

![diagramma del sistema di coordinate pixel in direct3d 9](images/d3d10-coordspix9.png)

## <a name="texel-coordinate-system"></a>Sistema di coordinate texel

Il sistema di coordinate texel ha l'origine nell'angolo superiore sinistro della trama, come illustrato nel diagramma seguente. In questo modo, il rendering delle trame allineate sullo schermo è semplice (in Direct3D 10), perché il sistema di coordinate pixel è allineato al sistema di coordinate texel.

![diagramma del sistema di coordinate texel](images/d3d10-coordstex10.png)

### <a name="texel-coordinate-system"></a>Sistema di coordinate texel

Le coordinate della trama sono rappresentate con un numero normalizzato o ridimensionato. Ogni coordinata di trama viene mappata a un texel specifico come segue:

Per una coordinata normalizzata:

-   Campionamento dei punti: Texel \# = floor(U \* Width)
-   Campionamento lineare: Left Texel \# = floor(U \* Width), Right Texel \# = Left Texel \# + 1

Per una coordinata ridimensionata:

-   Campionamento dei punti: Texel \# = floor(U)
-   Campionamento lineare: Left Texel \# = floor(U - 0.5), Right Texel \# = Left Texel \# + 1

Dove larghezza, è la larghezza della trama (in texel).

La disposizione degli indirizzi di trama si verifica dopo il calcolo della posizione del texel.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 





---
description: D3DX è una libreria di utilità che fornisce servizi di supporto. Si tratta di un livello sopra il componente Direct3D.
ms.assetid: 84815851-ca96-47ab-9f84-56ecaeb4a6d9
title: Supporto della trama in D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd9c8d6da498a47d14fe57ca770ba96a6852ae41
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303672"
---
# <a name="texture-support-in-d3dx-direct3d-9"></a>Supporto della trama in D3DX (Direct3D 9)

D3DX è una libreria di utilità che fornisce servizi di supporto. Si tratta di un livello sopra il componente Direct3D.

## <a name="textures"></a>Trame

Negli argomenti seguenti sono supportate molte trame diverse.

-   Supporto della trama mipmap standard. Vedere [generazione automatica di mipmap (Direct3D 9)](automatic-generation-of-mipmaps.md).
-   Supporto della mappa cubo. Vedere [mapping di ambienti cubici (Direct3D 9)](cubic-environment-mapping.md).
-   Supporto della trama del volume. Vedere [risorse di trama volume (Direct3D 9)](volume-texture-resources.md).
-   Supporto del mapping dell'ambiente. Vedere [mapping dell'ambiente (Direct3D 9)](environment-mapping.md).
-   Supporto del mapping di Bump. Vedere [bump mapping (Direct3D 9)](bump-mapping.md).

### <a name="texture-color-conversion"></a>Conversione colori trama

Quando si usa una delle funzioni D3DXLoadSurfacexxx, D3DXLoadVolumexxx, D3DXCreateTexturexxx, D3DXCreateCubeTexturexxx o D3DXCreateVolumeTexturexxx, potrebbe essere necessario eseguire la conversione dei colori. Ad esempio, una superficie può essere di tipo RGBA e l'altra potrebbe essere UVWQ. Per i casi di formati diversi, la sequenza di conversione è la seguente:

### <a name="mapping-rgba-to-uvwq"></a>Mapping di RGBA a UVWQ

-   R <-> U, il canale R è mappato al canale U o viceversa.
-   G <-> V, il canale G viene mappato al canale V o viceversa.
-   B <-> W, il canale B è mappato al canale W o viceversa.
-   Un <-> Q/L, viene eseguito il mapping di un canale al canale Q o L (a seconda di quale è disponibile nel formato di destinazione) o viceversa.


```
R->U
G->V
B->W
A->Q or A->L
```



### <a name="mapping-uv-to-rgba"></a>Mapping di UV a RGBA

-   U <-> R, U Channel è mappato al canale R o viceversa.
-   V <-> G, V Channel è mappato al canale G o viceversa.
-   1 <-> B, 1 viene mappato al canale B o viceversa.
-   1 <-> A, 1 viene mappato a un canale o viceversa.

Se un canale non esiste nell'origine, si presuppone che sia 1 (ad eccezione di A8, dove R, G, B si presuppone che sia 0). Ad esempio:


```
U -> R
V -> G
1 -> B
1 -> A
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[D3DX](d3dx.md)
</dt> </dl>

 

 




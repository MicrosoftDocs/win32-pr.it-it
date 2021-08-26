---
description: Informazioni sul supporto delle trame in D3DX. D3DX è una libreria di utilità che fornisce servizi helper. Si tratta di un livello sopra il componente Direct3D.
ms.assetid: 84815851-ca96-47ab-9f84-56ecaeb4a6d9
title: Supporto delle trame in D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ba518a5e9158c0337d45485852675d4ab91ef3585f027bd78fc51164c40466
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026021"
---
# <a name="texture-support-in-d3dx-direct3d-9"></a>Supporto delle trame in D3DX (Direct3D 9)

D3DX è una libreria di utilità che fornisce servizi helper. Si tratta di un livello sopra il componente Direct3D.

## <a name="textures"></a>Trame

Negli argomenti seguenti sono supportate molte trame diverse.

-   Supporto standard per le trame mipmapped. Vedere [Generazione automatica di mipmap (Direct3D 9).](automatic-generation-of-mipmaps.md)
-   Supporto delle mappe cubi. Vedere [Cubic Environment Mapping (Direct3D 9) ( Mapping dell'ambiente cubico - Direct3D 9).](cubic-environment-mapping.md)
-   Supporto della trama del volume. Vedere [Risorse trama del volume (Direct3D 9).](volume-texture-resources.md)
-   Supporto del mapping dell'ambiente. Vedere [Environment Mapping (Direct3D 9) (Mapping dell'ambiente - Direct3D 9).](environment-mapping.md)
-   Supporto del mapping di urti. Vedere [Bump Mapping (Direct3D 9)](bump-mapping.md).

### <a name="texture-color-conversion"></a>Conversione del colore della trama

Quando si usa una delle funzioni D3DXLoadSurfacexxx, D3DXLoadVolumexxx, D3DXCreateTexturexxx, D3DXCreateCubeTexturexxx o D3DXCreateVolumeTexturexxx, potrebbe essere necessario eseguire la conversione dei colori. Ad esempio, una superficie potrebbe essere di tipo RGBA e l'altra potrebbe essere UVWQ. Per i casi di formati diversi, la sequenza di conversione è la seguente:

### <a name="mapping-rgba-to-uvwq"></a>Mapping di RGBA a UVWQ

-   R <-> U, il canale R viene mappato al canale U o viceversa.
-   G <-> V, il canale G viene mappato al canale V o viceversa.
-   B <-> W, il canale B viene mappato al canale W o viceversa.
-   Un < di >, un canale A viene mappato al canale Q o L (a seconda di quale è disponibile nel formato di destinazione) o viceversa.


```
R->U
G->V
B->W
A->Q or A->L
```



### <a name="mapping-uv-to-rgba"></a>Mapping UV a RGBA

-   U <-> R, il canale U è mappato al canale R o viceversa.
-   V <-> G, il canale V viene mappato al canale G o viceversa.
-   1 <-> B, 1 è mappato al canale B o viceversa.
-   1 <-> A, 1 viene mappato al canale A o viceversa.

Se non esiste un canale nell'origine, si presuppone che sia 1 (ad eccezione di A8, dove si presuppone che R,G,B sia 0). Esempio:


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

 

 




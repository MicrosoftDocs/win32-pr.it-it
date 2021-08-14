---
description: Il frullatore del buffer dei fotogrammi può ora unire i canali alfa indipendentemente dalla fusione dei canali di colore nelle destinazioni di rendering. Questo controllo è abilitato con un nuovo stato di rendering, D3DRS \_ SEPARATEALPHABLENDENABLE.
ms.assetid: 6d30b13e-f4c6-4bc4-8735-15c398c099f1
title: Alfa di destinazione di rendering (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf5d4701b2d09334d605cf2c90ef0e03b06ea7886ea875ce8ec8ff9cbc428ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118797936"
---
# <a name="render-target-alpha-direct3d-9"></a>Alfa di destinazione di rendering (Direct3D 9)

Il frullatore del buffer dei fotogrammi può ora unire i canali alfa indipendentemente dalla fusione dei canali di colore nelle destinazioni di rendering. Questo controllo è abilitato con un nuovo stato di rendering, D3DRS \_ SEPARATEALPHABLENDENABLE.

Quando D3DRS \_ SEPARATEALPHABLENDENABLE è impostato su **FALSE** (condizione predefinita), i fattori di fusione della destinazione di rendering e le operazioni applicate al valore alfa sono gli stessi definiti per la fusione dei canali di colore. Un driver deve impostare il limite D3DPMISCCAPS SEPARATEALPHABLEND per indicare che può supportare la fusione alfa della destinazione \_ di rendering. Assicurarsi di abilitare D3DRS ALPHABLEND per indicare alla pipeline che è necessaria \_ la fusione alfa.

Per controllare i fattori nel canale alfa dei blender di destinazione di rendering, due nuovi stati di rendering sono definiti come segue:


```
D3DRS_SRCBLENDALPHA 
D3DRS_DESTBLENDALPHA 
```



Come D3DRS SRCBLEND e D3DRS DESTBLEND, questi valori possono essere impostati su uno dei valori \_ \_ nell'enumerazione [**D3DBLEND.**](./d3dblend.md) Le impostazioni di blend di origine e di destinazione possono essere combinate in diversi modi, a seconda delle impostazioni nei membri SrcBlendCaps e DestBlendCaps [**di D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

La fusione alfa viene eseguita nel modo seguente:

renderTargetAlpha = (alpha<sub>in</sub> \* srcBlendOp) BlendOp (alpha<sub>rt</sub> \* destBlendOp)

Dove:

-   alpha<sub>in è</sub> il valore alfa di input.
-   srcBlendOp è uno dei fattori di fusione in [**D3DBLEND**](./d3dblend.md).
-   BlendOp è uno dei fattori di fusione in [**D3DBLENDOP.**](./d3dblendop.md)
-   alpha<sub>rt è</sub> il valore alfa della destinazione di rendering.
-   destBlendOp è uno dei fattori di fusione in [**D3DBLEND.**](./d3dblend.md)
-   renderTargetAlpha è il valore alfa blended finale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Fusione alfa](alpha-blending.md)
</dt> </dl>

 

 

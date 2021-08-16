---
description: Il blender del buffer di frame può ora unire canali alfa indipendenti dalla fusione dei canali di colore nelle destinazioni di rendering. Questo controllo è abilitato con un nuovo stato di rendering, D3DRS \_ SEPARATEALPHABLENDENABLE.
ms.assetid: 6d30b13e-f4c6-4bc4-8735-15c398c099f1
title: Eseguire il rendering del valore alfa di destinazione (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf5d4701b2d09334d605cf2c90ef0e03b06ea7886ea875ce8ec8ff9cbc428ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118797936"
---
# <a name="render-target-alpha-direct3d-9"></a>Eseguire il rendering del valore alfa di destinazione (Direct3D 9)

Il blender del buffer di frame può ora unire canali alfa indipendenti dalla fusione dei canali di colore nelle destinazioni di rendering. Questo controllo è abilitato con un nuovo stato di rendering, D3DRS \_ SEPARATEALPHABLENDENABLE.

Quando L'opzione D3DRS \_ SEPARATEALPHABLENDENABLE è impostata su **FALSE** (condizione predefinita), i fattori di fusione della destinazione di rendering e le operazioni applicate ai valori alfa sono gli stessi definiti per la fusione dei canali di colori. Un driver deve impostare il limite D3DPMISCCAPS SEPARATEALPHABLEND per indicare che può supportare la fusione alfa di destinazione \_ del rendering. Assicurarsi di abilitare D3DRS ALPHABLEND per indicare alla pipeline che \_ è necessaria la fusione alfa.

Per controllare i fattori nel canale alfa dei blender di destinazione di rendering, vengono definiti due nuovi stati di rendering nel modo seguente:


```
D3DRS_SRCBLENDALPHA 
D3DRS_DESTBLENDALPHA 
```



Come D3DRS SRCBLEND e D3DRS DESTBLEND, questi possono essere impostati su uno dei valori \_ \_ nell'enumerazione [**D3DBLEND.**](./d3dblend.md) Le impostazioni di blend di origine e di destinazione possono essere combinate in diversi modi, a seconda delle impostazioni nei membri SrcBlendCaps e DestBlendCaps di [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

La fusione alfa viene eseguita come segue:

renderTargetAlpha = (alpha<sub>in</sub> \* srcBlendOp) BlendOp (alpha<sub>rt</sub> \* destBlendOp)

Dove:

-   alpha<sub>in</sub> è il valore alfa di input.
-   srcBlendOp è uno dei fattori di blend in [**D3DBLEND.**](./d3dblend.md)
-   BlendOp è uno dei fattori di blend in [**D3DBLENDOP.**](./d3dblendop.md)
-   alpha<sub>rt è</sub> il valore alfa della destinazione di rendering.
-   destBlendOp è uno dei fattori di blend in [**D3DBLEND.**](./d3dblend.md)
-   renderTargetAlpha è il valore alfa misto finale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Fusione alfa](alpha-blending.md)
</dt> </dl>

 

 

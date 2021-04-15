---
description: Il Blend buffer frame è ora in grado di fondere i canali alfa indipendentemente dalla combinazione del canale dei colori nelle destinazioni di rendering. Questo controllo è abilitato con un nuovo stato di rendering, D3DRS \_ SEPARATEALPHABLENDENABLE.
ms.assetid: 6d30b13e-f4c6-4bc4-8735-15c398c099f1
title: Alfa destinazione rendering (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b70f395406559782172448b5555daff056ffd54c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520474"
---
# <a name="render-target-alpha-direct3d-9"></a>Alfa destinazione rendering (Direct3D 9)

Il Blend buffer frame è ora in grado di fondere i canali alfa indipendentemente dalla combinazione del canale dei colori nelle destinazioni di rendering. Questo controllo è abilitato con un nuovo stato di rendering, D3DRS \_ SEPARATEALPHABLENDENABLE.

Quando D3DRS \_ SEPARATEALPHABLENDENABLE è impostato su **false** (condizione predefinita), le operazioni e i fattori di combinazione della destinazione di rendering applicati ad Alpha corrispondono a quelli definiti per la fusione dei canali dei colori. Un driver deve impostare D3DPMISCCAPS \_ SEPARATEALPHABLEND Cap per indicare che può supportare la fusione alfa di destinazione di rendering. Assicurarsi di abilitare D3DRS \_ AlphaBlend per indicare alla pipeline che è necessaria la fusione alfa.

Per controllare i fattori nel canale alfa dei Blender di destinazione di rendering, due nuovi Stati di rendering vengono definiti come segue:


```
D3DRS_SRCBLENDALPHA 
D3DRS_DESTBLENDALPHA 
```



Come D3DRS \_ SRCBLEND e D3DRS \_ DESTBLEND, questi possono essere impostati su uno dei valori nell'enumerazione [**D3DBLEND**](./d3dblend.md) . Le impostazioni di Blend di origine e di destinazione possono essere combinate in diversi modi, a seconda delle impostazioni nei membri SrcBlendCaps e DestBlendCaps di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

La fusione alfa viene eseguita come indicato di seguito:

renderTargetAlpha = (Alpha<sub>in</sub> \* srcBlendOp) BlendOp (Alpha<sub>RT</sub> \* destBlendOp)

Dove:

-   alfa<sub>in</sub> è il valore alfa di input.
-   srcBlendOp è uno dei fattori di Blend in [**D3DBLEND**](./d3dblend.md).
-   BlendOp è uno dei fattori di Blend in [**D3DBLENDOP**](./d3dblendop.md).
-   alfa<sub>RT</sub> è il valore alfa della destinazione di rendering.
-   destBlendOp è uno dei fattori di Blend in [**D3DBLEND**](./d3dblend.md).
-   renderTargetAlpha è il valore alfa blend finale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Fusione alfa](alpha-blending.md)
</dt> </dl>

 

 

---
description: Il motore di illuminazione Direct3D può usare dati di colore per vertice quando si esegue l'illuminazione se si indica al runtime che i dati sono presenti.
ms.assetid: acb43921-f0d4-4151-9371-1b99e5d30c0e
title: Per-Vertex colore (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6efd227c64785f7399ae3ba56d4623342c0910d901c3cfc404fc4a37f0d233
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117727987"
---
# <a name="per-vertex-color-state-direct3d-9"></a>Per-Vertex colore (Direct3D 9)

Il motore di illuminazione Direct3D può usare dati di colore per vertice quando si esegue l'illuminazione se si indica al runtime che i dati sono presenti. Questa operazione viene eseguita attivando lo stato di rendering seguente:


```
// disable per-vertex color
SetRenderState(D3DRS_COLORVERTEX, FALSE);

// enable per-vertex color
SetRenderState(D3DRS_COLORVERTEX, TRUE);
```



Se il colore per vertice è abilitato, le applicazioni possono configurare l'origine da cui il sistema recupera le informazioni sul colore per un vertice. Gli stati di \_ rendering D3DRS AMBIENTMATERIALSOURCE, D3DRS \_ DIFFUSEMATERIALSOURCE, D3DRS EMISSIVEMATERIALSOURCE e D3DRS SPECULARMATERIALSOURCE controllano rispettivamente le origini del componente colore \_ \_ ambiente, diffuso, emissivo e speculare. Ogni stato può essere impostato su membri del tipo enumerato [**D3DMATERIALCOLORSOURCE,**](./d3dmaterialcolorsource.md) che definisce costanti che indicano al sistema di usare il materiale corrente, il colore diffuso o il colore speculare come origine per il componente colore specificato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Stati di rendering](render-states.md)
</dt> </dl>

 

 

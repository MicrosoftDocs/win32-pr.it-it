---
description: Il motore di illuminazione Direct3D può usare i dati relativi al colore per ogni vertice durante l'illuminazione se si indica al runtime che i dati sono presenti.
ms.assetid: acb43921-f0d4-4151-9371-1b99e5d30c0e
title: Stato del colore Per-Vertex (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0104b427753fa3d7b7cf5a0a5a10cfeb5d10f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401059"
---
# <a name="per-vertex-color-state-direct3d-9"></a>Stato del colore Per-Vertex (Direct3D 9)

Il motore di illuminazione Direct3D può usare i dati relativi al colore per ogni vertice durante l'illuminazione se si indica al runtime che i dati sono presenti. Questa operazione viene eseguita attivando lo stato di rendering seguente:


```
// disable per-vertex color
SetRenderState(D3DRS_COLORVERTEX, FALSE);

// enable per-vertex color
SetRenderState(D3DRS_COLORVERTEX, TRUE);
```



Se il colore per vertice è abilitato, le applicazioni possono configurare l'origine da cui il sistema recupera le informazioni sui colori per un vertice. Gli \_ Stati di rendering D3DRS AMBIENTMATERIALSOURCE, D3DRS \_ DIFFUSEMATERIALSOURCE, D3DRS EMISSIVEMATERIALSOURCE \_ e D3DRS \_ SPECULARMATERIALSOURCE controllano rispettivamente le origini dei componenti di ambiente, diffuse, emissivo e speculare. Ogni stato può essere impostato sui membri del tipo enumerato [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) , che definisce le costanti che indicano al sistema di usare il materiale corrente, il colore diffuso o il colore speculare come origine per il componente colore specificato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Stati di rendering](render-states.md)
</dt> </dl>

 

 

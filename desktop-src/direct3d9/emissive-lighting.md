---
description: L'illuminazione emissivo è descritta da un singolo termine.
ms.assetid: b6ccf274-a6c5-4b26-8c43-c857c2c24e0f
title: Illuminazione emissivo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19cb0566d2409fb68e5fbbdca1cc609c31120e95
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303680"
---
# <a name="emissive-lighting-direct3d-9"></a>Illuminazione emissivo (Direct3D 9)

L'illuminazione emissivo è descritta da un singolo termine.

Illuminazione emissivo = C ₑ

Dove:



| Parametro | Valore predefinito | Tipo          | Descrizione     |
|-----------|---------------|---------------|-----------------|
| C ₑ        | (0, 0, 0, 0)     | D3DCOLORVALUE | Colore emissivo. |



 

Il valore per C ₑ è:

-   Vertex color1, se EMISSIVEMATERIALSOURCE = D3DMCS \_ color1 e il primo colore del vertice viene specificato nella dichiarazione del vertice.
-   Vertex color2, se EMISSIVEMATERIALSOURCE = D3DMCS \_ color2, e il secondo colore del vertice viene specificato nella dichiarazione del vertice.
-   colore emissivo materiale

> [!Note]  
> Se viene usata l'opzione EMISSIVEMATERIALSOURCE e il colore del vertice non viene specificato, viene usato il colore emissivo del materiale.

 

## <a name="example"></a>Esempio

In questo esempio, l'oggetto è colorato usando la luce ambientale della scena e un colore di ambiente di materiale. Il codice è illustrato di seguito.


```
// create material
D3DMATERIAL9 mtrl;
ZeroMemory( &mtrl, sizeof(mtrl) );
mtrl.Emissive.r = 0.0f;
mtrl.Emissive.g = 0.75f;
mtrl.Emissive.b = 0.0f;
mtrl.Emissive.a = 0.0f;
m_pd3dDevice->SetMaterial( &mtrl );
m_pd3dDevice->SetRenderState(D3DRS_EMISSIVEMATERIALSOURCE, D3DMCS_MATERIAL);
```



In base all'equazione, il colore risultante per i vertici dell'oggetto è il colore del materiale.

Nella figura seguente viene illustrato il colore del materiale, che è verde. Emissivo illumina tutti i vertici degli oggetti con lo stesso colore. Non dipende dal vertice normale o dalla direzione della luce. Di conseguenza, la sfera appare come un cerchio 2D perché non esiste alcuna differenza nell'ombreggiatura intorno alla superficie dell'oggetto.

![illustrazione di una sfera verde](images/lighte.jpg)

Nell'illustrazione seguente viene illustrato il modo in cui emissivo Light si integra con gli altri tre tipi di luci, dagli esempi precedenti. Sul lato destro della sfera è presente una Blend della emissivo verde e della luce di ambiente rossa. Sul lato sinistro della sfera, il verde emissivo chiaro si fonde con l'ambiente rosso e la luce diffusa che produce una sfumatura rossa. L'evidenziazione speculare è bianca al centro e crea un anello giallo, perché il valore della luce speculare cade in modo nitido lasciando inalterati i valori dell'ambiente, della diffusione e della luce emissivo che si fondono per essere gialli.

![illustrazione di una sfera verde con emissivo Light](images/lightadse.jpg)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Matematica dell'illuminazione](mathematics-of-lighting.md)
</dt> </dl>

 

 




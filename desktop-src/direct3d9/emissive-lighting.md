---
description: L'illuminazione emissiva è descritta da un singolo termine.
ms.assetid: b6ccf274-a6c5-4b26-8c43-c857c2c24e0f
title: Illuminazione emissiva (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da3200486118e6b44efc3be31f01b3a10e62c876d673c687619a4e6c8445f0cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118802933"
---
# <a name="emissive-lighting-direct3d-9"></a>Illuminazione emissiva (Direct3D 9)

L'illuminazione emissiva è descritta da un singolo termine.

Illuminazione emissiva = Cₑ

Dove:



| Parametro | Valore predefinito | Tipo          | Descrizione     |
|-----------|---------------|---------------|-----------------|
| Cₑ        | (0,0,0,0)     | D3DCOLORVALUE | Colore emissivo. |



 

Il valore per Cₑ è uno dei seguenti:

-   vertex color1, se EMISSIVEMATERIALSOURCE = D3DMCS COLOR1 e il primo colore del vertice viene \_ fornito nella dichiarazione del vertice.
-   vertex color2, se EMISSIVEMATERIALSOURCE = D3DMCS COLOR2 e il secondo colore del vertice viene \_ specificato nella dichiarazione del vertice.
-   colore emissivo materiale

> [!Note]  
> Se si usa l'opzione EMISSIVEMATERIALSOURCE e non viene specificato il colore del vertice, viene usato il colore emissivo del materiale.

 

## <a name="example"></a>Esempio

In questo esempio l'oggetto viene colorato usando la luce ambientale della scena e un colore di ambiente materiale. Il codice è illustrato di seguito.


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

La figura seguente mostra il colore del materiale, che è verde. Luci emissive di tutti i vertici degli oggetti con lo stesso colore. Non dipende dalla normale del vertice o dalla direzione della luce. Di conseguenza, la sfera è simile a un cerchio 2D perché non esiste alcuna differenza nell'ombreggiatura intorno alla superficie dell'oggetto.

![illustrazione di una sfera verde](images/lighte.jpg)

Nella figura seguente viene illustrato come la luce emissiva si integra con gli altri tre tipi di luci degli esempi precedenti. Sul lato destro della sfera è presente una combinazione dell'emissivo verde e della luce ambientale rossa. Sul lato sinistro della sfera, la luce verde emissiva si combina con una luce ambientale rossa e una luce diffusa che produce una sfumatura rossa. L'evidenziazione speculare è bianca al centro e crea un anello giallo quando il valore della luce speculare cade in modo nitido lasciando i valori di luce ambientale, diffusa ed emissiva che si fondono per ottenere il giallo.

![illustrazione di una sfera verde con luce emissiva](images/lightadse.jpg)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Matematica dell'illuminazione](mathematics-of-lighting.md)
</dt> </dl>

 

 




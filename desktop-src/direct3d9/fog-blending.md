---
description: La fusione dello sfumamento si riferisce all'applicazione del fattore di riempimento ai colori dell'oggetto e dell'oggetto per produrre il colore finale visualizzato in una scena, come descritto in Formule dei colori (Direct3D 9).
ms.assetid: b5b43f12-bbed-4464-aebc-02ad6dab1951
title: Blending Di Blending (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f60f3402daf71a3fce14af936334c3d96e928d3469452eafb94d139594bb0b19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894021"
---
# <a name="fog-blending-direct3d-9"></a>Blending Di Blending (Direct3D 9)

La fusione degli elementi si riferisce all'applicazione del fattore di colore dei colori degli oggetti e degli oggetti per produrre il colore finale visualizzato in una scena, come descritto in Formula dei concis [(Direct3D 9).](fog-formulas.md) Lo stato di rendering di D3DRS \_ FOGENABLE controlla la fusione delle sfumature. Impostare questo stato di rendering su **TRUE per** abilitare la fusione delle sfumature, come illustrato nel codice di esempio seguente. Il valore predefinito è **FALSE.**


```
// For this example, g_pDevice is a valid pointer
// to an IDirect3DDevice9 interface.
HRESULT hr;
hr = g_pDevice->SetRenderState(
                    D3DRS_FOGENABLE,
                    TRUE);
if FAILED(hr)
    return hr;
```



È necessario abilitare la fusione delle sfumature sia per pixel pixel che per vertice. Per informazioni sull'uso di questi tipi di ami, vedere [Pixel Coordinate (Direct3D 9)](pixel-fog.md) e [Vertex Risoluzione (Direct3D 9).](vertex-fog.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi Disami](fog-types.md)
</dt> </dl>

 

 




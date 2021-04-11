---
description: La fusione di nebbia si riferisce all'applicazione del fattore di nebbia ai colori dell'oggetto e della nebbia per produrre il colore finale visualizzato in una scena, come descritto in formule di nebbia (Direct3D 9).
ms.assetid: b5b43f12-bbed-4464-aebc-02ad6dab1951
title: Blending di nebbia (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa918715a7bbe37b200568a0a9098135c5558b0d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123351"
---
# <a name="fog-blending-direct3d-9"></a>Blending di nebbia (Direct3D 9)

La fusione di nebbia si riferisce all'applicazione del fattore di nebbia ai colori dell'oggetto e della nebbia per produrre il colore finale visualizzato in una scena, come descritto in [formule di nebbia (Direct3D 9)](fog-formulas.md). Lo \_ stato di rendering FOGENABLE di D3DRS controlla la fusione di nebbia. Impostare questo stato di rendering su **true** per abilitare la fusione di nebbia, come illustrato nel codice di esempio seguente. Il valore predefinito è **false**.


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



È necessario abilitare la fusione di nebbia sia per la nebbia dei pixel che per il vertice. Per informazioni sull'uso di questi tipi di nebbia, vedere [pixel Fog (Direct3D 9)](pixel-fog.md) e [Vertex Fog (Direct3D 9)](vertex-fog.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di nebbia](fog-types.md)
</dt> </dl>

 

 




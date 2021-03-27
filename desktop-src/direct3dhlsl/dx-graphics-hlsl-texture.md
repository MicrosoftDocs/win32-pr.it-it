---
title: Tipo di trama
description: Per dichiarare una variabile di trama, usare la sintassi seguente.
ms.assetid: 54db5432-dab8-4a4d-a4de-93c6fa640535
keywords:
- Tipo di trama HLSL
topic_type:
- apiref
api_name:
- Texture type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89568dc5cf24af38f916375795eea052c8b39200
ms.sourcegitcommit: 6f905c836d3fd04934fb3e5f1a56b4a421f7596f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/07/2020
ms.locfileid: "103723983"
---
# <a name="texture-type"></a>Tipo di trama

Per dichiarare una variabile di trama, usare la sintassi seguente.

|                |
|----------------|
| **Nome tipo;** |

## <a name="parameters"></a>Parametri
| Elemento                                                                                     | Descrizione                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Tipo**<br/> | Uno dei tipi seguenti: texture (non tipizzata, per compatibilità con le versioni precedenti), Texture1D, Texture1DArray, Texture2D, Texture2DArray, Texture3D, TextureCube. Le dimensioni dell'elemento devono essere incluse in quantità a 4 32 bit.<br/> |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nome**<br/> | Stringa ASCII che identifica in modo univoco il nome della variabile.<br/>                                                                                                                                                   |
## <a name="remarks"></a>Commenti

È possibile utilizzare una trama in tre parti.

1.  Dichiarazione di una variabile di trama. Questa operazione viene eseguita con la sintassi illustrata in precedenza. Ad esempio, si tratta di dichiarazioni valide.

    ```
    texture g_MeshTexture;
    ```

    \- - oppure -

    ```
    Texture2D g_MeshTexture;
    ```

2.  Dichiarazione e inizializzazione di un oggetto Sampler. Questa operazione viene eseguita con sintassi leggermente diversa in Direct3D 9 e Direct3D 10. Per informazioni dettagliate sulla sintassi degli oggetti Sampler, vedere [Sampler Type (DirectX HLSL)](dx-graphics-hlsl-sampler.md).
3.  Richiamo di una funzione di trama in uno shader.

Differenze tra Direct3D 9 e Direct3D 10:

Direct3D 9 utilizza [funzioni di trama intrinseche](dx-graphics-hlsl-intrinsic-functions.md) per eseguire operazioni di trama. Questo esempio è relativo all' [esempio BasicHLSL](/previous-versions/windows/desktop/bb153287(v%3Dvs.85)) e USA [tex2D (s, t) (DirectX HLSL)](dx-graphics-hlsl-tex2d.md) per eseguire il campionamento della trama.

<code>Output.RGBColor = tex2D(MeshTextureSampler, In.TextureUV) * In.Diffuse;</code>

Direct3D 10 usa invece [oggetti trama basati su modelli](dx-graphics-hlsl-to-type.md) . Di seguito è riportato un esempio dell'operazione di trama equivalente.

<code>Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) * In.Diffuse;</code>

## <a name="see-also"></a>Vedi anche

[Tipi di dati (DirectX HLSL)](dx-graphics-hlsl-data-types.md)

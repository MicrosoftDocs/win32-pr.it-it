---
title: SampleCmp (oggetto trama di DirectX HLSL)
description: Esegue il campionamento di una trama e confronta un singolo componente con il valore di confronto specificato.
ms.assetid: e21894c4-e8c5-4c3d-92c1-727964f8fd94
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6991bead4bfc42451c26fe5476b4c114626eb7e8
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/17/2020
ms.locfileid: "104993653"
---
# <a name="samplecmp-directx-hlsl-texture-object"></a>SampleCmp (oggetto trama di DirectX HLSL)

Esegue il campionamento di una trama e confronta un singolo componente con il valore di confronto specificato.

<table>
<tbody>
<tr class="odd">
<td>float Object. SampleCmp ( <dl> SamplerComparisonState S,<br />
Percorso float,<br />
float CompareValue,<br />
[offset int]<br />
</dl>);</td>
</tr>
</tbody>
</table>
 

Il confronto è un confronto a componente singolo tra il primo componente archiviato nella trama e il valore di confronto passato nel metodo.

Questo metodo può essere richiamato solo da un pixel shader; non è supportato in un vertex o in un geometry shader.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Oggetto*
</dt> <dd>

Qualsiasi tipo [di oggetto trama](dx-graphics-hlsl-to-type.md) (ad eccezione di Texture2DMS, Texture2DMSArray o Texture3D).

</dd> <dt>

<span id="S"></span><span id="s"></span>*S*
</dt> <dd>

\[in \] uno stato di confronto del campionatore, ovvero lo stato del campionatore più uno stato di confronto (una funzione di confronto e un filtro di confronto). Per informazioni dettagliate e un esempio, vedere il [tipo di campionatore](dx-graphics-hlsl-sampler.md) .

</dd> <dt>

<span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Percorso*
</dt> <dd>

\[nelle \] coordinate di trama. Il tipo di argomento dipende dal tipo di oggetto trama.

| Tipo di Texture-Object          | Tipo di parametro |
|------------------------------|----------------|
| Texture1D                    | float          |
| Texture1DArray, Texture2D    | float2         |
| Texture2DArray ¹, TextureCube | float3         |
| TextureCubeArray ¹            | float4         |

</dd> <dt>

<span id="CompareValue"></span><span id="comparevalue"></span><span id="COMPAREVALUE"></span>*CompareValue*
</dt> <dd>

Valore a virgola mobile da utilizzare come valore di confronto.

</dd> <dt>

<span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*Offset*
</dt> <dd>

\[in \] un offset della coordinata di trama facoltativo che può essere usato per qualsiasi tipo di oggetto trama. l'offset viene applicato al percorso prima del campionamento. Gli offset della trama devono essere statici. Il tipo di argomento dipende dal tipo di oggetto trama. Per altre informazioni, vedere [applicazione degli offset delle coordinate di trama](dx-graphics-hlsl-to-sample.md).

| Tipo di Texture-Object            | Tipo di parametro |
|--------------------------------|----------------|
| Texture1D, Texture1DArray      | INT            |
| Texture2D, Texture2DArray ¹     | int2           |
| TextureCube, TextureCubeArray ¹ | Non supportato  |

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore a virgola mobile nell'intervallo compreso tra \[ 0 e 1 \] .

Per ogni Texel recuperato (in base alla configurazione campionatore della modalità filtro), **SampleCmp** esegue un confronto del valore z (terzo componente di input) dallo shader rispetto al valore Texel (1 se il confronto passa; in caso contrario 0). **SampleCmp** combina quindi i risultati 0 e 1 per ogni Texel insieme al normale filtro della trama (non una media) e restituisce il \[ valore 0.. 1 risultante \] allo shader.

## <a name="remarks"></a>Commenti

Il filtro di confronto fornisce un'operazione di filtro di base che risulta utile per l'applicazione di filtri con profondità più stretta.

Quando si usa questo metodo su una risorsa a virgola mobile (invece di un formato normalizzato o senza segno), il valore di confronto non viene automaticamente premuto tra 0,0 e 1,0. Pertanto, può essere necessario un morsetto manuale del valore di confronto per le tecniche di ombreggiatura comuni.

Usare un offset solo in un miplevel Integer; in caso contrario, è possibile ottenere risultati diversi a seconda dell'implementazione dell'hardware o delle impostazioni del driver.

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.

| vs \_ 4 \_ 0 | vs \_ 4 \_ 1 ² | PS \_ 4 \_ 0 | PS \_ 4 \_ 1 ² | GS \_ 4 \_ 0 | GS \_ 4 \_ 1 ² |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | x ¹       | x         |          |           |

1.  Texture2DArray e TextureCubeArray sono disponibili nel modello Shader 4,1 o versione successiva.
2.  Il modello di Shader 4,1 è disponibile in Direct3D 10,1 o versione successiva.

> [!NOTE]  
> **SampleCmp** è disponibile anche in PS 4 \_ 0 \_ level \_ 9 \_ 1 e 4 \_ 0 \_ level \_ 9 \_ 3 quando si usano le tecniche descritte in implementazione di [buffer shadow per il livello di funzionalità Direct3D 9](/previous-versions/windows/apps/jj262110(v=win.10)).

## <a name="related-topics"></a>Argomenti correlati

[Texture-oggetto](dx-graphics-hlsl-to-type.md)

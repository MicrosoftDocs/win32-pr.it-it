---
title: SampleCmp (oggetto trama DirectX HLSL)
description: Consente di eseguire il campionamento di una trama e di confrontare un singolo componente con il valore di confronto specificato.
ms.assetid: e21894c4-e8c5-4c3d-92c1-727964f8fd94
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a606ad9081f1ca1fdc4261d862ea6edfef4460989bb6d51d839d85f5797c1466
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854641"
---
# <a name="samplecmp-directx-hlsl-texture-object"></a>SampleCmp (oggetto trama DirectX HLSL)

Consente di eseguire il campionamento di una trama e di confrontare un singolo componente con il valore di confronto specificato.

<table>
<tbody>
<tr class="odd">
<td>float Object.SampleCmp( <dl> SamplerComparisonState S,<br />
float Location,<br />
float CompareValue,<br />
[int Offset]<br />
</dl>);</td>
</tr>
</tbody>
</table>
 

Il confronto è un confronto a componente singolo tra il primo componente archiviato nella trama e il valore di confronto passato nel metodo .

Questo metodo può essere richiamato solo da un pixel shader; non è supportato in un vertex shader o geometry shader.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Oggetto*
</dt> <dd>

Qualsiasi [tipo di oggetto](dx-graphics-hlsl-to-type.md) trama (ad eccezione di Texture2DMS, Texture2DMSArray o Texture3D).

</dd> <dt>

<span id="S"></span><span id="s"></span>*S*
</dt> <dd>

\[in Uno stato sampler-comparison, ovvero lo stato del campionatore più uno stato di confronto (una funzione di confronto \] e un filtro di confronto). Per informazioni [dettagliate e un esempio,](dx-graphics-hlsl-sampler.md) vedere il tipo di campionatore.

</dd> <dt>

<span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Posizione*
</dt> <dd>

\[in \] Coordinate della trama. Il tipo di argomento dipende dal tipo texture-object.

| Texture-Object tipo          | Tipo di parametro |
|------------------------------|----------------|
| Texture1D                    | float          |
| Texture1DArray, Texture2D    | float2         |
| Texture2DArray¹, TextureCube | float3         |
| TextureCubeArray¹            | float4         |

</dd> <dt>

<span id="CompareValue"></span><span id="comparevalue"></span><span id="COMPAREVALUE"></span>*CompareValue*
</dt> <dd>

Valore a virgola mobile da utilizzare come valore di confronto.

</dd> <dt>

<span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*compensare*
</dt> <dd>

\[in Offset delle coordinate di trama facoltativo, che può essere usato per qualsiasi tipo di oggetto trama. L'offset viene applicato alla posizione \] prima del campionamento. Gli offset di trama devono essere statici. Il tipo di argomento dipende dal tipo texture-object. Per altre informazioni, vedere [Applicazione degli offset delle coordinate di trama.](dx-graphics-hlsl-to-sample.md)

| Texture-Object tipo            | Tipo di parametro |
|--------------------------------|----------------|
| Texture1D, Texture1DArray      | int            |
| Texture2D, Texture2DArray¹     | int2           |
| TextureCube, TextureCubeArray¹ | Non supportato  |

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore a virgola mobile compreso nell'intervallo \[ 0..1. \]

Per ogni texel recuperato (in base alla configurazione del campionatore della modalità filtro), **SampleCmp** esegue un confronto tra il valore z (terzo componente di input) dello shader e il valore texel (1 se il confronto passa; in caso contrario, 0). **SampleCmp** unisce quindi questi risultati 0 e 1 per ogni texel come nel normale filtro trame (non una media) e restituisce il valore \[ 0..1 risultante allo \] shader.

## <a name="remarks"></a>Commenti

Il filtro di confronto offre un'operazione di filtro di base utile per il filtro con più profondità percentuale.

Quando si usa questo metodo in una risorsa a virgola mobile (anziché in un formato normalizzato con segno o senza segno), il valore di confronto non viene impostato automaticamente tra 0.0 e 1.0. Pertanto, potrebbe essere necessaria una chiusura manuale del valore di confronto per le tecniche di ombreggiatura comuni.

Usare un offset solo in corrispondenza di un valore integer miplevel. In caso contrario, è possibile ottenere risultati diversi a seconda dell'implementazione dell'hardware o delle impostazioni del driver.

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli shader seguenti.

| vs \_ 4 \_ 0 | vs \_ 4 \_ 1² | ps \_ 4 \_ 0 | ps \_ 4 \_ 1² | gs \_ 4 \_ 0 | gs \_ 4 \_ 1² |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | x¹       | x         |          |           |

1.  Texture2DArray e TextureCubeArray sono disponibili in Shader Model 4.1 o versione successiva.
2.  Shader Model 4.1 è disponibile in Direct3D 10.1 o versione successiva.

> [!NOTE]  
> **SampleCmp** è disponibile anche in ps 4 \_ 0 \_ level 9 1 e 4 0 level 9 3 quando si usano le tecniche descritte \_ \_ in \_ \_ \_ \_ [Implementing shadow buffers for Direct3D feature level 9](/previous-versions/windows/apps/jj262110(v=win.10)).

## <a name="related-topics"></a>Argomenti correlati

[Oggetto texture](dx-graphics-hlsl-to-type.md)

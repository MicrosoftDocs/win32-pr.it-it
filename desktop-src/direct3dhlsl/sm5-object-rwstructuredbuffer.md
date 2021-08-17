---
title: RWStructuredBuffer
description: Buffer di lettura/scrittura che può assumere un tipo T che è una struttura .
ms.assetid: 8dd93b81-135d-4f28-898f-38510dc39af1
keywords:
- RWStructuredBuffer HLSL
topic_type:
- apiref
api_name:
- RWStructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 58eacc277eac2d55aca0e6068698d11110768cfbe3ab6b564b97a0607715a7ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095151"
---
# <a name="rwstructuredbuffer"></a>RWStructuredBuffer

Buffer di lettura/scrittura che può assumere un tipo T che è una struttura .



| Metodo                                                                     | Descrizione                             |
|----------------------------------------------------------------------------|-----------------------------------------|
| [**DecrementCounter**](sm5-object-rwstructuredbuffer-decrementcounter.md) | Decrementa il contatore nascosto dell'oggetto. |
| [**GetDimensions**](sm5-object-rwstructuredbuffer-getdimensions.md)       | Ottiene le dimensioni della risorsa.           |
| [**IncrementCounter**](sm5-object-rwstructuredbuffer-incrementcounter.md) | Incrementa il contatore nascosto dell'oggetto. |
| [**Caricamento**](rwstructuredbuffer-load.md)                                    | Legge i dati del buffer.                      |
| [**Operatore\[\]**](sm5-object-rwstructuredbuffer-operatorindex.md)        | Restituisce una variabile di risorsa.            |



 

Una variabile di risorsa può anche essere passata a qualsiasi operazione non ordinata o interlocked.

Gli oggetti RWStructuredBuffer possono essere preceduti dalla classe di archiviazione **globalmentecoherente**. Questa classe di archiviazione causa barriere di memoria e sincronizzazioni per scaricare i dati nell'intera GPU in modo che altri gruppi possano visualizzare le scritture. Senza questo identificatore, una barriera di memoria o una sincronizzazione scarica solo un UAV all'interno del gruppo corrente.

Il formato UAV associato a questa risorsa deve essere creato con il formato DXGI \_ FORMAT \_ UNKNOWN.

Per altre informazioni sui [buffer strutturati,](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources)vedere il materiale di panoramica.

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questo oggetto è supportato nei modelli di shader seguenti.



| Modello di shader                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Supportato |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models [Shader Model 4](dx-graphics-hlsl-sm4.md) (Disponibile tramite l'API Direct3D 11 usando il livello di funzionalità 10.0 o 10.1 ([**D3D \_ FEATURE \_ LEVEL**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) \_ 10 X) nei dispositivi che supportano \_ compute shader. Per altre informazioni sul supporto di compute shader su hardware di livello inferiore, vedere [Compute Shaders on Downlevel Hardware (Compute Shader su hardware di livello inferiore).](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders)<br/> | sì       |



 

Questo oggetto è supportato per i tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti modello shader 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 


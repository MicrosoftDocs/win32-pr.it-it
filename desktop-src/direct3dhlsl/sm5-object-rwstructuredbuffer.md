---
title: RWStructuredBuffer
description: Un buffer di lettura/scrittura che può assumere un tipo T che è una struttura.
ms.assetid: 8dd93b81-135d-4f28-898f-38510dc39af1
keywords:
- HLSL RWStructuredBuffer
topic_type:
- apiref
api_name:
- RWStructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f921ca795e761522828de14ede61894defe44f6e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399205"
---
# <a name="rwstructuredbuffer"></a>RWStructuredBuffer

Un buffer di lettura/scrittura che può assumere un tipo T che è una struttura.



| Metodo                                                                     | Descrizione                             |
|----------------------------------------------------------------------------|-----------------------------------------|
| [**DecrementCounter**](sm5-object-rwstructuredbuffer-decrementcounter.md) | Decrementa il contatore nascosto dell'oggetto. |
| [**GetDimensions**](sm5-object-rwstructuredbuffer-getdimensions.md)       | Ottiene le dimensioni della risorsa.           |
| [**IncrementCounter**](sm5-object-rwstructuredbuffer-incrementcounter.md) | Incrementa il contatore nascosto dell'oggetto. |
| [**Caricamento**](rwstructuredbuffer-load.md)                                    | Legge i dati del buffer.                      |
| [**Operatore\[\]**](sm5-object-rwstructuredbuffer-operatorindex.md)        | Restituisce una variabile di risorsa.            |



 

Una variabile di risorsa può essere passata anche in qualsiasi operazione non ordinata o Interlocked.

Gli oggetti RWStructuredBuffer possono essere preceduti dalla classe di archiviazione **globallycoherent**. Questa classe di archiviazione causa barriere e sincronizzazioni di memoria per scaricare i dati nell'intera GPU, in modo che altri gruppi possano visualizzare le Scritture. Senza questo identificatore, una barriera di memoria o una sincronizzazione Scarica solo un UAV all'interno del gruppo corrente.

Il formato UAV associato a questa risorsa deve essere creato con il formato DXGI \_ formato \_ sconosciuto.

Per ulteriori informazioni sui [buffer strutturati](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources), vedere il materiale di panoramica.

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questo oggetto è supportato nei modelli shader seguenti.



| Modello di shader                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Supportato |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md) e High shader Models Shader Model [4](dx-graphics-hlsl-sm4.md) (disponibile tramite l'API Direct3D 11 usando il livello di funzionalità 10,0 o 10,1 ([**D3D \_ feature \_ Level**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) \_ 10 \_ X) sui dispositivi che supportano compute shader. Per ulteriori informazioni sul supporto di compute shader nell'hardware di livello inferiore, vedere [Compute Shaders su hardware di livello inferiore](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).<br/> | sì       |



 

Questo oggetto è supportato per i tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti Shader Model 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 


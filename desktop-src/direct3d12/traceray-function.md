---
description: Invia un raggio in una ricerca di riscontri in una struttura di accelerazione.
ms.assetid: ''
title: TraceRay (funzione)
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TraceRay
api_type:
- NA
ms.openlocfilehash: faeed928b25acb4dac95e47a46a103daf87124e0
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "106320821"
---
# <a name="traceray-function"></a>TraceRay (funzione)

Invia un raggio in una ricerca di riscontri in una struttura di accelerazione.

## <a name="syntax"></a>Sintassi
Questa definizione di funzione intrinseca è equivalente al modello di funzione seguente:

```
Template<payload_t>
void TraceRay(RaytracingAccelerationStructure AccelerationStructure,
              uint RayFlags,
              uint InstanceInclusionMask,
              uint RayContributionToHitGroupIndex,
              uint MultiplierForGeometryContributionToHitGroupIndex,
              uint MissShaderIndex,
              RayDesc Ray,
              inout payload_t Payload);

```



## <a name="parameters"></a>Parametri

`AccelerationStructure`

Struttura di accelerazione di primo livello da usare. La definizione di una struttura di accelerazione NULL impone un mancato riscontro.

`RayFlags`

Combinazione valida di valori di [ray_flag](ray_flag.md) . Solo i flag raggio definiti vengono propagati dal sistema, ovvero sono visibili alla funzione intrinseca shader [RayFlags](rayflags.md) .

`InstanceInclusionMask`

Un Unsigned Integer, gli 8 bit ultimi, usati per includere o rifiutare istanze geometry basate su InstanceMask in ogni istanza. Ad esempio:
```
if(!((InstanceInclusionMask & InstanceMask) & 0xff)) { //ignore intersection }
```

`RayContributionToHitGroupIndex`

Unsigned Integer che specifica l'offset da aggiungere ai calcoli di indirizzamento nelle tabelle dello shader per l'indicizzazione del gruppo di hit.  Vengono utilizzati solo i 4 bit inferiori di questo valore.

`MultiplierForGeometryContributionToHitGroupIndex`

Un Unsigned Integer che specifica lo stride da moltiplicare per *GeometryContributionToHitGroupIndex*, che è solo l'indice in base 0, che la geometria è stata fornita dall'app nella struttura di accelerazione di livello inferiore. Vengono utilizzati solo i 16 bit inferiori del valore del moltiplicatore.

`MissShaderIndex`

Unsigned Integer che specifica l'indice dello shader di mancato utilizzo in una tabella shader.

`Ray`

Oggetto [**RayDesc**](raydesc.md) che rappresenta il raggio da tracciare.

`Payload`

Payload con raggio definito dall'utente a cui si accede sia per l'input che per l'output da shader richiamati durante raytracing.  Al termine dell'esecuzione di [**TraceRay**](traceray-function.md) , il chiamante può accedere anche al payload.

## <a name="return-value"></a>Valore restituito

**void**

## <a name="remarks"></a>Commenti

Questa funzione può essere chiamata dai seguenti tipi di shader raytracing:

* [**Hit shader più vicino**](closest-hit-shader.md)
* [**Lo shader manca**](miss-shader.md)
* [**Shader di generazione del Ray**](ray-generation-shader.md)



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Guida di riferimento a Direct3D 12 raytracing HLSL](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 





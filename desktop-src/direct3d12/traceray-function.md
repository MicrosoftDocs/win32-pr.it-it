---
description: Invia un raggio a una ricerca di riscontri in una struttura di accelerazione.
ms.assetid: ''
title: Funzione TraceRay
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
ms.openlocfilehash: 4e22a26d7bd2fd91029c106133667bce98c163d90d99f0700dac7f2bdf0796fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027981"
---
# <a name="traceray-function"></a>Funzione TraceRay

Invia un raggio a una ricerca di riscontri in una struttura di accelerazione.

## <a name="syntax"></a>Sintassi
Questa definizione di funzione intrinseca equivale al modello di funzione seguente:

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

Struttura di accelerazione di primo livello da utilizzare. Se si specifica una struttura di accelerazione NULL, viene forzata una mancata esecuzione.

`RayFlags`

Combinazione valida [di ray_flag](ray_flag.md) valori. Solo i flag di raggio definiti vengono propagati dal sistema, ad esempio sono visibili alla funzione intrinseca dello shader [RayFlags.](rayflags.md)

`InstanceInclusionMask`

Intero senza segno, i cui ultimi 8 bit vengono usati per includere o rifiutare istanze geometry in base a InstanceMask in ogni istanza. Esempio:
```
if(!((InstanceInclusionMask & InstanceMask) & 0xff)) { //ignore intersection }
```

`RayContributionToHitGroupIndex`

Intero senza segno che specifica l'offset da aggiungere ai calcoli di indirizzamento all'interno delle tabelle shader per l'indicizzazione dei gruppi di hit.  Vengono usati solo i 4 bit più in basso di questo valore.

`MultiplierForGeometryContributionToHitGroupIndex`

Intero senza segno che specifica lo stride da moltiplicare per *GeometryContributionToHitGroupIndex,* che è solo l'indice in base 0 fornito dall'app nella struttura di accelerazione di livello inferiore. Vengono usati solo i 16 bit più in basso di questo valore del moltiplicatore.

`MissShaderIndex`

Intero senza segno che specifica l'indice del miss shader all'interno di una tabella shader.

`Ray`

Oggetto [**RayDesc**](raydesc.md) che rappresenta il raggio da tracciare.

`Payload`

Un payload di raggi definito dall'utente accede sia per l'input che per l'output dagli shader richiamati durante il raytracing.  Al [**termine di TraceRay,**](traceray-function.md) il chiamante può accedere anche al payload.

## <a name="return-value"></a>Valore restituito

**void**

## <a name="remarks"></a>Commenti

Questa funzione può essere chiamata dai tipi di shader raytracing seguenti:

* [**Hit Shader più vicino**](closest-hit-shader.md)
* [**Miss Shader**](miss-shader.md)
* [**Shader di generazione di raggi**](ray-generation-shader.md)



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni di riferimento su Direct3D 12 Raytracing HLSL](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 





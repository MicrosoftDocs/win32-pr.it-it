---
title: SV_GroupIndex
description: "\\ 0034; flatd \\ 0034; Indice di un thread compute shader all'interno di un gruppo di thread, che converte l'oggetto SV GroupThreadID multidimensionale \\_ in un valore 1D. SV \\_ groupIndex varia da 0 a (numthreadsX \\ numthreadsY \\ numThreadsZ) \\ 8211; 1."
ms.assetid: e793be10-7c83-478c-859a-4b0a2c537570
keywords:
- SV_GroupIndex HLSL
topic_type:
- apiref
api_name:
- SV_GroupIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 952a94378a0570d5bb7bc4f08959074bc8a4da4d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728178"
---
# <a name="sv_groupindex"></a>\_GROUPINDEX SV

Indice "flat" di un thread compute shader all'interno di un gruppo di thread, che trasforma l'oggetto SV \_ GroupThreadID multidimensionali in un valore 1D. SV \_ groupIndex varia da 0 a (numthreadsX \* numthreadsY \* numThreadsZ) – 1.

## <a name="type"></a>Tipo



| Tipo |
|------|
| uint |



 

## <a name="remarks"></a>Commenti


```
SV_GroupIndex = SV_GroupThreadID.z*dimx*dimy + 
                      SV_GroupThreadID.y*dimx + 
                      SV_GroupThreadID.x
```



dove dimx e Dimy sono le dimensioni specificate nell'attributo [numThreads](sm5-attributes-numthreads.md) per il punto di ingresso.

Questo valore di sistema è facoltativo. Tuttavia, il suo utilizzo garantisce che un thread scriva solo nell'area di memoria assegnata nella variabile groupshared.

Nella figura seguente viene illustrata la relazione tra i parametri passati a [**sul ID3D11DeviceContext::D di patch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), dispatch (5, 3, 2), i valori specificati nell'attributo [numThreads](sm5-attributes-numthreads.md) , numThreads (10, 8, 3) e i valori che vengono passati al compute shader per i valori di sistema correlati al thread (SV \_ groupIndex,[SV \_ DispatchThreadID](sv-dispatchthreadid.md),[SV \_ GroupThreadID](sv-groupthreadid.md),[SV \_ GroupID](sv-groupid.md)).

![illustrazione della relazione tra dispatch, i gruppi di thread e i thread](images/threadgroupids.png)

Questa funzione è supportata nei tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Semantica](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
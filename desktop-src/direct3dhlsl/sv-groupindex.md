---
title: SV_GroupIndex
description: "\\ 0034;flattened \\ 0034; indice di un thread compute shader all'interno di un gruppo di thread, che trasforma groupThreadID SV multidimensionale \\_ in un valore 1D. SV \\_ GroupIndex varia da 0 a (numthreadsX \\ numthreadsY \\ numThreadsZ) \\ 8211; 1."
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
ms.openlocfilehash: fd8c10212a2dd91e4ecbe7fd48a427e4019b2cd79b3d56457635ab9ef9d9262a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118508251"
---
# <a name="sv_groupindex"></a>SV \_ GroupIndex

Indice "flat" di un thread compute shader all'interno di un gruppo di thread, che trasforma groupThreadID SV multidimensionale \_ in un valore 1D. SV \_ GroupIndex varia da 0 a (numthreadsX \* numthreadsY \* numThreadsZ) - 1.

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



dove dimx e dimy sono le dimensioni specificate [nell'attributo numthreads](sm5-attributes-numthreads.md) per il punto di ingresso.

Questo valore di sistema è facoltativo. Tuttavia, il relativo utilizzo garantisce che un thread scrive solo nell'area di memoria assegnata nella variabile groupshared.

La figura seguente illustra la relazione tra i parametri passati [**a ID3D11DeviceContext::D ispatch,**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)Dispatch(5,3,2), i valori specificati nell'attributo [numthreads,](sm5-attributes-numthreads.md) numthreads(10,8,3) e i valori che verranno passati allo shader di calcolo per i valori di sistema correlati ai thread (SV \_ GroupIndex,[SV \_ DispatchThreadID,](sv-dispatchthreadid.md)[SV \_ GroupThreadID,](sv-groupthreadid.md)[SV \_ GroupID).](sv-groupid.md)

![Illustrazione della relazione tra dispatch, gruppi di thread e thread](images/threadgroupids.png)

Questa funzione è supportata nei tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Semantica](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
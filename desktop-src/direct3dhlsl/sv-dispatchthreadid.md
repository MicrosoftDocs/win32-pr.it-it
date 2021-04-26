---
title: SV_DispatchThreadID
description: Indici per i quali è in esecuzione un compute shader combinato di thread e thread.
ms.assetid: bad697f6-26d9-47cd-93e5-127621a161e8
keywords:
- SV_DispatchThreadID HLSL
topic_type:
- apiref
api_name:
- SV_DispatchThreadID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e9653d98ebbfef6dd25bb137af3358a14d177f3e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996518"
---
# <a name="sv_dispatchthreadid"></a>SV \_ DispatchThreadID

Indici per i quali è in esecuzione un compute shader combinato di thread e thread. SV \_ DispatchThreadID è la somma di SV \_ GroupID \* numthreads e GroupThreadID. Varia nell'intervallo specificato in [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) e [numthreads](sm5-attributes-numthreads.md). Ad esempio, se Dispatch(2,2,2) viene chiamato su un compute shader con numthreads(3,3,3) SV DispatchThreadID avrà un intervallo \_ di 0,.5 per ogni dimensione.

## <a name="type"></a>Tipo



|       |
|-------|
| Tipo  |
| uint3 |



 

## <a name="remarks"></a>Commenti

Questo valore di sistema è facoltativo.

La figura seguente illustra la relazione tra i parametri passati a [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), i valori specificati nell'attributo [numthreads,](sm5-attributes-numthreads.md) numthreads(10,8,3) e i valori che verranno passati al compute shader per i valori di sistema correlati al thread ([SV \_ GroupIndex](sv-groupindex.md), SV \_ DispatchThreadID,[SV \_ GroupThreadID](sv-groupthreadid.md),[SV \_ GroupID](sv-groupid.md)).

![illustrazione della relazione tra dispatch, gruppi di thread e thread](images/threadgroupids.png)

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

 

 

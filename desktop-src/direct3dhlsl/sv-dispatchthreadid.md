---
title: SV_DispatchThreadID
description: Indici per i quali un thread e un gruppo di thread combinati eseguono uno shader di calcolo.
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
ms.openlocfilehash: 8e2713aaa50206660f7672688a43e644873b1c13
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827060"
---
# <a name="sv_dispatchthreadid"></a>SV \_ DispatchThreadID

Indici per i quali un thread e un gruppo di thread combinati eseguono uno shader di calcolo. SV \_ DispatchThreadID è la somma di \_ SV GroupID \* numthreads e GroupThreadID. Varia in base all'intervallo specificato in [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) e [numthreads](sm5-attributes-numthreads.md). Ad esempio, se Dispatch(2,2,2) viene chiamato in un compute shader con numthreads(3,3,3) SV \_ DispatchThreadID avrà un intervallo di 0,.5 per ogni dimensione.

## <a name="type"></a>Tipo



| Tipo      |
|-------|
| uint3 |



 

## <a name="remarks"></a>Commenti

Questo valore di sistema è facoltativo.

La figura seguente illustra la relazione tra i parametri passati a [**Dispatch,**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)Dispatch(5,3,2), i valori specificati nell'attributo [numthreads,](sm5-attributes-numthreads.md) numthreads(10,8,3) e i valori che verranno passati allo shader di calcolo per i valori di sistema correlati al thread ([SV \_ GroupIndex](sv-groupindex.md), SV \_ DispatchThreadID,[SV \_ GroupThreadID](sv-groupthreadid.md),[SV \_ GroupID](sv-groupid.md)).

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

 

 

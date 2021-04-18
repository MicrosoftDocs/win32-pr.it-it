---
title: SV_DispatchThreadID
description: Indici per i quali viene eseguito un compute shader in un gruppo di thread e thread combinato.
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
ms.openlocfilehash: d55fcf7e291c561ecb51dd32dfac135c563974c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104560326"
---
# <a name="sv_dispatchthreadid"></a>\_DISPATCHTHREADID SV

Indici per i quali viene eseguito un compute shader in un gruppo di thread e thread combinato. SV \_ DispatchThreadID è la somma di SV \_ GroupID \* numThreads e GroupThreadID. Varia in base all'intervallo specificato in [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) e [numThreads](sm5-attributes-numthreads.md). Ad esempio, se dispatch (2, 2, 2) viene chiamato in un compute shader con numThreads (3, 3, 3) SV \_ DispatchThreadID avrà un intervallo di 0.5 per ogni dimensione.

## <a name="type"></a>Tipo



|       |
|-------|
| Tipo  |
| uint3 |



 

## <a name="remarks"></a>Commenti

Questo valore di sistema è facoltativo.

Nella figura seguente viene illustrata la relazione tra i parametri passati a [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), dispatch (5, 3, 2), i valori specificati nell'attributo [numThreads](sm5-attributes-numthreads.md) , numThreads (10, 8, 3) e i valori che vengono passati al compute shader per i valori di sistema correlati ai thread ([SV \_ groupIndex](sv-groupindex.md), SV \_ DispatchThreadID,[SV \_ GroupThreadID](sv-groupthreadid.md),[SV \_ GroupID](sv-groupid.md)).

![illustrazione della relazione tra dispatch, i gruppi di thread e i thread](images/threadgroupids.png)

Questa funzione è supportata nei tipi di shader seguenti:



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Semantica](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
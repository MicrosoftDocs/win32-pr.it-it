---
title: SV_GroupThreadID
description: Indici per i quali viene eseguito un compute shader in un singolo thread all'interno di un gruppo di thread.
ms.assetid: be944592-c4ea-43c9-88bc-98a9a190a437
keywords:
- SV_GroupThreadID HLSL
topic_type:
- apiref
api_name:
- SV_GroupThreadID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2d36e5639b017dfa94e0f3c9f84d6725f6b6a283
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996988"
---
# <a name="sv_groupthreadid"></a>SV \_ GroupThreadID

Indici per i quali viene eseguito un compute shader in un singolo thread all'interno di un gruppo di thread. SV \_ GroupThreadID varia nell'intervallo specificato per il compute shader [nell'attributo numthreads.](sm5-attributes-numthreads.md) Ad esempio, se numthreads(3,2,1) è stato specificato, i valori possibili per il valore di input SV GroupThreadID hanno questo intervallo di valori \_ (0-2,0-1,0).

## <a name="type"></a>Tipo



|       |
|-------|
| Tipo  |
| uint3 |



 

## <a name="remarks"></a>Commenti

Questo valore di sistema è facoltativo ed è sempre compreso nei limiti dei valori passati [nell'attributo numthreads.](sm5-attributes-numthreads.md)

La figura seguente illustra la relazione tra i parametri passati a [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), i valori specificati nell'attributo [numthreads,](sm5-attributes-numthreads.md) numthreads(10,8,3) e i valori che verranno passati al compute shader per i valori di sistema correlati al thread ([SV \_ GroupIndex](sv-groupindex.md),[SV \_ DispatchThreadID](sv-dispatchthreadid.md), SV \_ GroupThreadID,[SV \_ GroupID](sv-groupid.md)).

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

 

 

---
title: SV_GroupThreadID
description: Indici per cui è in esecuzione un singolo thread in un gruppo di thread in cui è in esecuzione compute shader.
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
ms.openlocfilehash: 3d4d35766bdbdc2d69c98983a85f336ab784d24d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338983"
---
# <a name="sv_groupthreadid"></a>\_GROUPTHREADID SV

Indici per cui è in esecuzione un singolo thread in un gruppo di thread in cui è in esecuzione compute shader. SV \_ GroupThreadID varia in base all'intervallo specificato per compute shader nell'attributo [numThreads](sm5-attributes-numthreads.md) . Se, ad esempio, numThreads (3, 2, 1) è stato specificato, i valori possibili per il \_ valore di input SV GroupThreadID includono questo intervallo di valori (0-2, 0-1, 0).

## <a name="type"></a>Tipo



|       |
|-------|
| Tipo  |
| uint3 |



 

## <a name="remarks"></a>Commenti

Questo valore di sistema è facoltativo ed è sempre compreso tra i limiti dei valori passati nell'attributo [numThreads](sm5-attributes-numthreads.md) .

Nella figura seguente viene illustrata la relazione tra i parametri passati a [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), dispatch (5, 3, 2), i valori specificati nell'attributo [numThreads](sm5-attributes-numthreads.md) , numThreads (10, 8, 3) e i valori che vengono passati al compute shader per i valori di sistema correlati ai thread ([SV \_ groupIndex](sv-groupindex.md),[SV \_ DispatchThreadID](sv-dispatchthreadid.md), SV \_ GroupThreadID,[SV \_ GroupID](sv-groupid.md)).

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

 

 
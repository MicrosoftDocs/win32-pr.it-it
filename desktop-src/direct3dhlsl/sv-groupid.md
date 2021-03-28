---
title: SV_GroupID
description: Indici per il gruppo di thread in cui è in esecuzione compute shader.
ms.assetid: 1b90ca74-a2b6-4a5f-aa4a-1ec879360593
keywords:
- SV_GroupID HLSL
topic_type:
- apiref
api_name:
- SV_GroupID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a2588474a4c6f2cfc6d616cdb70940277389fd1f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117898"
---
# <a name="sv_groupid"></a>\_GROUPID SV

Indici per il gruppo di thread in cui è in esecuzione compute shader. Gli indici sono per l'intero gruppo e non per un singolo thread. I valori possibili variano nell'intervallo passato come parametri da [**inviare**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch). Se ad esempio si chiama dispatch (2, 1, 1), i valori possibili sono 0, 0, 0 e 1, 0, 0.

Definisce l'offset di gruppo all'interno di una chiamata di [**invio**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) , per dimensione della chiamata di invio.

## <a name="type"></a>Tipo



|       |
|-------|
| Tipo  |
| uint3 |



 

## <a name="remarks"></a>Commenti

Questo valore di sistema è facoltativo.

Nella figura seguente viene illustrata la relazione tra i parametri passati a [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), dispatch (5, 3, 2), i valori specificati nell'attributo [numThreads](sm5-attributes-numthreads.md) , numThreads (10, 8, 3) e i valori che vengono passati al compute shader per i valori di sistema correlati ai thread ([SV \_ groupIndex](sv-groupindex.md),[SV \_ DispatchThreadID](sv-dispatchthreadid.md),[SV \_ GroupThreadID](sv-groupthreadid.md), SV \_ GroupID).

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

 

 
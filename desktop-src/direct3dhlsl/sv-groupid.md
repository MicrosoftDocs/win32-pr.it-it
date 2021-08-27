---
title: SV_GroupID
description: Indici per il quale il gruppo di thread raggruppa uno shader di calcolo in cui è in esecuzione.
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
ms.openlocfilehash: bce2623141329b4d750ab5add7957a7674662d7c21de9ff03e1165d341f98576
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118161"
---
# <a name="sv_groupid"></a>SV \_ GroupID

Indici per il quale il gruppo di thread raggruppa uno shader di calcolo in cui è in esecuzione. Gli indici sono relativi all'intero gruppo e non a un singolo thread. I valori possibili variano in base all'intervallo passato come parametri a [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch). Ad esempio, chiamando Dispatch(2,1,1) si possono ottenere valori possibili di 0,0,0 e 1,0,0.

Definisce l'offset del gruppo all'interno [**di una chiamata Dispatch,**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) per dimensione della chiamata dispatch.

## <a name="type"></a>Tipo



| Tipo      |
|-------|
| uint3 |



 

## <a name="remarks"></a>Commenti

Questo valore di sistema è facoltativo.

La figura seguente illustra la relazione tra i parametri passati a [**Dispatch,**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)Dispatch(5,3,2), i valori specificati nell'attributo [numthreads,](sm5-attributes-numthreads.md) numthreads(10,8,3) e i valori che verranno passati allo shader di calcolo per i valori di sistema correlati ai thread ([SV \_ GroupIndex,](sv-groupindex.md)[SV \_ DispatchThreadID,](sv-dispatchthreadid.md)[SV \_ GroupThreadID,](sv-groupthreadid.md)SV GroupID, SV \_ GroupID).

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

 

 

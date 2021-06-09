---
title: SV_GroupID
description: Indici per il gruppo di thread in cui è in esecuzione un compute shader.
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
ms.openlocfilehash: ab94cef0a9a33f23947e11b93a5487c65eee3890
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827040"
---
# <a name="sv_groupid"></a>SV \_ GroupID

Indici per il gruppo di thread in cui è in esecuzione un compute shader. Gli indici sono relativi all'intero gruppo e non a un singolo thread. I valori possibili variano nell'intervallo passato come parametri a [**Dispatch.**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) Ad esempio, se si chiama Dispatch(2,1,1), i valori possibili sono 0,0,0 e 1,0,0.

Definisce l'offset del gruppo all'interno [**di una chiamata Dispatch,**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) per dimensione della chiamata di invio.

## <a name="type"></a>Tipo



| Tipo      |
|-------|
| uint3 |



 

## <a name="remarks"></a>Commenti

Questo valore di sistema è facoltativo.

La figura seguente illustra la relazione tra i parametri passati a [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), i valori specificati nell'attributo [numthreads,](sm5-attributes-numthreads.md) numthreads(10,8,3) e i valori che verranno passati al compute shader per i valori di sistema correlati al thread [(SV \_ GroupIndex](sv-groupindex.md),[SV \_ DispatchThreadID](sv-dispatchthreadid.md),[SV \_ GroupThreadID](sv-groupthreadid.md), SV \_ GroupID).

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

 

 

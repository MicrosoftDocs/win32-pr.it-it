---
title: SV_GroupThreadID
description: Indici per cui un singolo thread all'interno di un gruppo di thread esegue uno shader di calcolo.
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
ms.openlocfilehash: d399008f1a9314ceb1fd4b1499b51340b499600b
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827030"
---
# <a name="sv_groupthreadid"></a>SV \_ GroupThreadID

Indici per cui un singolo thread all'interno di un gruppo di thread esegue uno shader di calcolo. SV \_ GroupThreadID varia in base all'intervallo specificato per lo shader di calcolo [nell'attributo numthreads.](sm5-attributes-numthreads.md) Se, ad esempio, numthreads(3,2,1) è stato specificato, i valori possibili per il valore di input SV GroupThreadID hanno questo intervallo di valori \_ (0-2,0-1,0).

## <a name="type"></a>Tipo



| Tipo      |
|-------|
| uint3 |



 

## <a name="remarks"></a>Commenti

Questo valore di sistema è facoltativo ed è sempre compreso nei limiti dei valori passati [nell'attributo numthreads.](sm5-attributes-numthreads.md)

La figura seguente illustra la relazione tra i parametri passati a [**Dispatch,**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)Dispatch(5,3,2), i valori specificati nell'attributo [numthreads,](sm5-attributes-numthreads.md) numthreads(10,8,3) e i valori che verranno passati allo shader di calcolo per i valori di sistema correlati al thread ([SV \_ GroupIndex,](sv-groupindex.md)[SV \_ DispatchThreadID,](sv-dispatchthreadid.md)SV \_ GroupThreadID,[SV \_ GroupID).](sv-groupid.md)

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

 

 

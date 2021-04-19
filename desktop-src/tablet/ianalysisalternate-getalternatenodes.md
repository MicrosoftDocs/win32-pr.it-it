---
description: Ottiene gli oggetti IContextNode associati a questa alternativa.
ms.assetid: 6dfae9cc-d9d2-44de-b6cf-80bbcd296390
title: 'Metodo IAnalysisAlternate:: GetAlternateNodes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetAlternateNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: dd24581774c2115c9f7ccb6857d0cd4d9e1bfd2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307478"
---
# <a name="ianalysisalternategetalternatenodes-method"></a>Metodo IAnalysisAlternate:: GetAlternateNodes

Ottiene gli oggetti [**IContextNode**](icontextnode.md) associati a questa alternativa.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetAlternateNodes(
  [out] IContextNodes **ppAlternateNodes
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppAlternateNodes* \[ out\]
</dt> <dd>

Puntatore alla raccolta [**IContextNodes**](icontextnodes.md) che contiene gli oggetti [**IContextNode**](icontextnode.md) associati a questa alternativa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su \* *ppAlternateNodes* quando non è più necessario usare la raccolta di nodi di contesto.

 

Questo metodo restituisce i nodi di contesto foglia associati a questa alternativa. Esempi di nodi foglia sono i nodi di contesto InkWord, TextWord, image, InkDrawing e InkBullet. Per altre informazioni, vedere [**IContextNode:: GetType**](icontextnode-gettype.md) e [tipi di nodo di contesto](context-node-types.md).

Poiché corrispondono a alternative, questi oggetti [**IContextNode**](icontextnode.md) non sono discendenti del **IContextNode** radice dell'oggetto [**IInkAnalyzer**](iinkanalyzer.md) (vedere il [**Metodo IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md)), a meno che non siano l'alternativa superiore, ovvero il primo elemento di una raccolta [**IAnalysisAlternates**](ianalysisalternates.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNodes**](icontextnodes.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> <dt>

[System. Windows. Ink. AnalysisCore. AnalysisAlternateBase. AlternateNodes](ianalysisalternate-getalternatenodes.md)
</dt> </dl>

 


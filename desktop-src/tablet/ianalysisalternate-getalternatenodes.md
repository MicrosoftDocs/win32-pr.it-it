---
description: Ottiene gli oggetti IContextNode associati a questo oggetto alternativo.
ms.assetid: 6dfae9cc-d9d2-44de-b6cf-80bbcd296390
title: Metodo IAnalysisAlternate::GetAlternateNodes (IACom.h)
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
ms.openlocfilehash: fbaff3cea515c9636127ce2267b9f05e0c0a0006b96046a7f2474661b3b76f77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935521"
---
# <a name="ianalysisalternategetalternatenodes-method"></a>Metodo IAnalysisAlternate::GetAlternateNodes

Ottiene gli [**oggetti IContextNode**](icontextnode.md) associati a questo oggetto alternativo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetAlternateNodes(
  [out] IContextNodes **ppAlternateNodes
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppAlternateNodes* \[ Cambio\]
</dt> <dd>

Puntatore alla [**raccolta IContextNodes**](icontextnodes.md) che contiene gli [**oggetti IContextNode**](icontextnode.md) associati a questa alternativa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su \* *ppAlternateNodes* quando non è più necessario usare la raccolta di nodi di contesto.

 

Questo metodo restituisce i nodi del contesto foglia associati a questa alternativa. Esempi di nodi foglia sono i nodi di contesto InkWord, TextWord, Image, InkDrawing e InkBullet. Per altre informazioni, vedere [**IContextNode::GetType**](icontextnode-gettype.md) e [Tipi di nodo di contesto.](context-node-types.md)

Poiché corrispondono a alternative, questi oggetti [**IContextNode**](icontextnode.md) non sono discendenti del nodo **IContextNode** radice dell'oggetto [**IInkAnalyzer**](iinkanalyzer.md) (vedere il metodo [**IInkAnalyzer::GetRootNode**](iinkanalyzer-getrootnode.md)), a meno che non siano il primo elemento di una raccolta [**IAnalysisAlternates.**](ianalysisalternates.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNodes**](icontextnodes.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> <dt>

[Sistema. Windows. Ink.AnalysisCore.AnalysisAlternateBase.AlternateNodes](ianalysisalternate-getalternatenodes.md)
</dt> </dl>

 


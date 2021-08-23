---
description: Recupera i nodi foglia input penna che contengono i tratti specificati.
ms.assetid: d9ebc57d-63f5-4175-8bb6-a688b98823d4
title: Metodo IInkAnalyzer::FindInkLeafNodesForStrokes (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindInkLeafNodesForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a7424f62008e15feb538df7a6a27745dda17bf6ace4612218608f8e509e75e59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967280"
---
# <a name="iinkanalyzerfindinkleafnodesforstrokes-method"></a>Metodo IInkAnalyzer::FindInkLeafNodesForStrokes

Recupera i nodi foglia input penna che contengono i tratti specificati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT FindInkLeafNodesForStrokes(
  [in]  ULONG         ulStrokeIdsCount,
  [in]  LONG          *plStrokeIds,
  [out] IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ulStrokeIdsCount* \[ Pollici\]
</dt> <dd>

Numero di identificatori di tratto passati.

</dd> <dt>

*plStrokeIds* \[ Pollici\]
</dt> <dd>

Matrice degli identificatori dei tratti.

</dd> <dt>

*ppContextNodesFound* \[ Cambio\]
</dt> <dd>

Raccolta di [**oggetti IContextNode**](icontextnode.md) che contengono tutti i nodi foglia input penna che contengono i tratti con identificatori nella matrice *plStrokeIds.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppContextNodesFound* quando non è più necessario usare l'oggetto .

 

I nodi foglia non contengono nodi figlio. I nodi input penna contengono i dati del tratto. Esempi di nodi foglia di input penna sono gli oggetti InkWord, InkDrawing e [**IContextNode**](icontextnode.md) IInkBullet. Per altre informazioni, vedere [Tipi di nodo di contesto](context-node-types.md).

Se nessun nodo contiene i tratti specificati, viene restituita una raccolta [**IContextNodes**](icontextnodes.md) vuota. Analogamente, se *ulStrokeIdsCount* è zero, viene restituita una raccolta **IContextNodes** vuota.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Metodo IInkAnalyzer::FindInkLeafNodes**](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[**Metodo IInkAnalyzer::FindLeafNodes**](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[**Metodo IInkAnalyzer::FindNode**](iinkanalyzer-findnode.md)
</dt> <dt>

[**Metodo IInkAnalyzer::FindNodesOfType**](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[**Metodo IInkAnalyzer::FindNodesOfTypeForStrokes**](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[**Metodo IInkAnalyzer::FindNodesOfTypeInSubTree**](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[**Metodo IInkAnalyzer::FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[**Metodo IInkAnalyzer::FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 


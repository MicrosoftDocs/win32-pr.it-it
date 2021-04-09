---
description: Recupera i nodi foglia dell'input penna che contengono i tratti specificati.
ms.assetid: d9ebc57d-63f5-4175-8bb6-a688b98823d4
title: 'Metodo IInkAnalyzer:: FindInkLeafNodesForStrokes (IACom. h)'
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
ms.openlocfilehash: d19bed823f5385533dfc938eb9f6013b4a5640c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879337"
---
# <a name="iinkanalyzerfindinkleafnodesforstrokes-method"></a>Metodo IInkAnalyzer:: FindInkLeafNodesForStrokes

Recupera i nodi foglia dell'input penna che contengono i tratti specificati.

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

*ulStrokeIdsCount* \[ in\]
</dt> <dd>

Numero di identificatori di tratto passati.

</dd> <dt>

*plStrokeIds* \[ in\]
</dt> <dd>

Matrice degli identificatori del tratto.

</dd> <dt>

*ppContextNodesFound* \[ out\]
</dt> <dd>

Raccolta di oggetti [**IContextNode**](icontextnode.md) che contengono tutti i nodi foglia dell'input penna che contengono i tratti con identificatori nella matrice *plStrokeIds* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppContextNodesFound* quando non è più necessario utilizzare l'oggetto.

 

I nodi foglia non contengono nodi figlio. I nodi Ink contengono dati Stroke. Esempi di nodi foglia input penna sono oggetti InkWord, InkDrawing, andInkBullet [**IContextNode**](icontextnode.md) . Per altre informazioni, vedere [tipi di nodo di contesto](context-node-types.md).

Se nessun nodo contiene i tratti specificati, viene restituita una raccolta [**IContextNodes**](icontextnodes.md) vuota. Analogamente, se *ulStrokeIdsCount* è zero, viene restituita una raccolta **IContextNodes** vuota.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: FindInkLeafNodes**](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: FindLeafNodes**](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: FindNode**](iinkanalyzer-findnode.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: FindNodesOfType**](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: FindNodesOfTypeForStrokes**](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: FindNodesOfTypeInSubTree**](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 


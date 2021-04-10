---
description: Recupera tutti i nodi foglia dell'input penna.
ms.assetid: 988ae9f9-8fca-4757-8eb0-ae161e5690c9
title: 'Metodo IInkAnalyzer:: FindInkLeafNodes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindInkLeafNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d5ebcfe542ab03f2e3d3a24c29142e41433c9eed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879341"
---
# <a name="iinkanalyzerfindinkleafnodes-method"></a>Metodo IInkAnalyzer:: FindInkLeafNodes

Recupera tutti i nodi foglia dell'input penna.

## <a name="syntax"></a>Sintassi


```C++
HRESULT FindInkLeafNodes(
  [out] IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppContextNodesFound* \[ out\]
</dt> <dd>

Puntatore alla raccolta [**IContextNodes**](icontextnodes.md) contenente tutti i nodi foglia dell'input penna.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppContextNodesFound* quando non è più necessario utilizzare l'oggetto.

 

I nodi foglia non contengono nodi figlio. I nodi Ink contengono dati Stroke. Esempi di nodi foglia input penna sono oggetti InkWord, InkDrawing e InkBullet [**IContextNode**](icontextnode.md) . Per altre informazioni, vedere [tipi di nodo di contesto](context-node-types.md).

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

[**Metodo IInkAnalyzer:: FindInkLeafNodesForStrokes**](iinkanalyzer-findinkleafnodesforstrokes.md)
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

 


---
description: Recupera tutti gli oggetti IContextNode del tipo specificato che contengono i tratti specificati.
ms.assetid: c674a03b-841c-4a9c-8268-302bc4038934
title: 'Metodo IInkAnalyzer:: FindNodesOfTypeForStrokes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesOfTypeForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2dd98c72007a69521506e2be21ad10edeb46df27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307390"
---
# <a name="iinkanalyzerfindnodesoftypeforstrokes-method"></a>Metodo IInkAnalyzer:: FindNodesOfTypeForStrokes

Recupera tutti gli oggetti [**IContextNode**](icontextnode.md) del tipo specificato che contengono i tratti specificati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT FindNodesOfTypeForStrokes(
  [in]  const GUID          *pNodeType,
  [in]        ULONG         ulStrokeIdsCount,
  [in]        LONG          *plStrokeIds,
  [out]       IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pNodeType* \[ in\]
</dt> <dd>

Identificatore univoco globale (GUID) che specifica il tipo di nodo.

</dd> <dt>

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

Raccolta di oggetti [**IContextNode**](icontextnode.md) che contengono tutti i nodi di tipo *pNodeType* che contengono i tratti con identificatori nella matrice *plStrokeIds* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su \* *ppContextNodesFound* quando non è più necessario utilizzare l'oggetto.

 

La proprietà *pNodeType* deve contenere un GUID dalle costanti dei [tipi di nodo di contesto](context-node-types.md) .

Se il tipo di nodo specificato non è un nodo foglia, ma uno dei discendenti del nodo fa riferimento a un tratto nella raccolta Strokes, tale nodo viene aggiunto alla raccolta restituita.

Se [**IInkAnalyzer**](iinkanalyzer.md) non contiene alcun [**IContextNode**](icontextnode.md), viene restituita una raccolta [**IContextNodes**](icontextnodes.md) vuota.

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

[**Metodo IInkAnalyzer:: FindInkLeafNodesForStrokes**](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: FindLeafNodes**](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: FindNode**](iinkanalyzer-findnode.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: FindNodesOfType**](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: FindNodesOfTypeInSubTree**](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 


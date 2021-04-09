---
description: Recupera tutti gli oggetti IContextNode del tipo specificato.
ms.assetid: e6e68d78-9697-40e6-a4ae-a187ef01a769
title: 'Metodo IInkAnalyzer:: FindNodesOfType (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesOfType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 51611fd4b3c77b43f2ea0d967f81dcc9547edb24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879334"
---
# <a name="iinkanalyzerfindnodesoftype-method"></a>Metodo IInkAnalyzer:: FindNodesOfType

Recupera tutti gli oggetti [**IContextNode**](icontextnode.md) del tipo specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT FindNodesOfType(
  [in]  const GUID          *pNodeType,
  [out]       IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pNodeType* \[ in\]
</dt> <dd>

**GUID** che specifica il tipo di nodo.

</dd> <dt>

*ppContextNodesFound* \[ out\]
</dt> <dd>

Puntatore a [**IContextNodes**](icontextnodes.md) contenente tutti i nodi di tipo *pNodeType*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppContextNodesFound* quando non è più necessario utilizzare l'oggetto.

 

La proprietà *pNodeType* deve contenere un GUID dalle costanti dei [tipi di nodo di contesto](context-node-types.md) .

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

 


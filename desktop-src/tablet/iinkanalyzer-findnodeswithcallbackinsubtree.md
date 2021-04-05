---
description: Recupera tutti gli oggetti IContextNode che corrispondono ai criteri specificati e sono discendenti dell'oggetto IContextNode specificato.
ms.assetid: 48d0ae97-c4a5-458d-b4c0-fa82f5aed4e5
title: 'Metodo IInkAnalyzer:: FindNodesWithCallBackInSubTree (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesWithCallBackInSubTree
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6b4ba64cd9271158d49ddd72270d4e6f25538672
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751826"
---
# <a name="iinkanalyzerfindnodeswithcallbackinsubtree-method"></a>Metodo IInkAnalyzer:: FindNodesWithCallBackInSubTree

Recupera tutti gli oggetti [**IContextNode**](icontextnode.md) che corrispondono ai criteri specificati e sono discendenti dell'oggetto **IContextNode** specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT FindNodesWithCallBackInSubTree(
  [in]  IMatchesCriteriaCallBack *pCriteria,
  [in]  IContextNode             *pContextNodeToSearchFrom,
  [out] IContextNodes            **ppContextNodesFound
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCriteria* \[ in\]
</dt> <dd>

Oggetto [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md) utilizzato per valutare se un oggetto [**IContextNode**](icontextnode.md) soddisfa o meno i criteri specificati.

</dd> <dt>

*pContextNodeToSearchFrom* \[ in\]
</dt> <dd>

Oggetto [**IContextNode**](icontextnode.md) di cui vengono cercati i discendenti.

</dd> <dt>

*ppContextNodesFound* \[ out\]
</dt> <dd>

Puntatore a [**IContextNodes**](icontextnodes.md) contenente tutti i nodi che soddisfano i criteri specificati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppContextNodesFound* quando non è più necessario utilizzare l'oggetto.

 

Se il [**IInkAnalyzer**](iinkanalyzer.md) non contiene il nodo *pContextNodeToSearchFrom* , questo metodo restituisce un codice di errore.

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

[**Metodo IInkAnalyzer:: FindNodesOfTypeForStrokes**](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: FindNodesOfTypeInSubTree**](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 


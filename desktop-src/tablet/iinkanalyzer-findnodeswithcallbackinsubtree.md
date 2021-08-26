---
description: Recupera tutti gli oggetti IContextNode che corrispondono ai criteri specificati e sono discendenti dell'oggetto IContextNode specificato.
ms.assetid: 48d0ae97-c4a5-458d-b4c0-fa82f5aed4e5
title: Metodo IInkAnalyzer::FindNodesWithCallBackInSubTree (IACom.h)
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
ms.openlocfilehash: d6ab8e66e75af4e31a1efacd082f79f68d5f63c546c56d59bf4ca0fedc201929
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939931"
---
# <a name="iinkanalyzerfindnodeswithcallbackinsubtree-method"></a>Metodo IInkAnalyzer::FindNodesWithCallBackInSubTree

Recupera tutti gli oggetti [**IContextNode**](icontextnode.md) che corrispondono ai criteri specificati e sono discendenti **dell'oggetto IContextNode** specificato.

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

*pCriteria* \[ Pollici\]
</dt> <dd>

Oggetto [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md) usato per valutare se un [**oggetto IContextNode**](icontextnode.md) soddisfa o non soddisfa i criteri specificati.

</dd> <dt>

*pContextNodeToSearchFrom* \[ Pollici\]
</dt> <dd>

Oggetto [**IContextNode**](icontextnode.md) i cui discendenti vengono cercati.

</dd> <dt>

*ppContextNodesFound* \[ Cambio\]
</dt> <dd>

Puntatore a [**IContextNodes**](icontextnodes.md) contenente tutti i nodi che soddisfano i criteri specificati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppContextNodesFound* quando non è più necessario usare l'oggetto .

 

Se [**IInkAnalyzer**](iinkanalyzer.md) non contiene il *nodo pContextNodeToSearchFrom,* questo metodo restituisce un codice di errore.

Se [**IInkAnalyzer**](iinkanalyzer.md) non contiene [**un IContextNode di**](icontextnode.md)questo tipo, viene restituita una raccolta [**IContextNodes**](icontextnodes.md) vuota.

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

[**Metodo IInkAnalyzer::FindInkLeafNodesForStrokes**](iinkanalyzer-findinkleafnodesforstrokes.md)
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

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 


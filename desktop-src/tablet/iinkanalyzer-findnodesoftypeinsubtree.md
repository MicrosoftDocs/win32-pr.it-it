---
description: Recupera tutti gli oggetti IContextNode del tipo specificato discendenti dell'oggetto IContextNode specificato.
ms.assetid: 7e57d6ec-fe04-44c6-904f-7a212bbfcd19
title: Metodo IInkAnalyzer::FindNodesOfTypeInSubTree (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesOfTypeInSubTree
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 16e1516a8da5b4d09b80606bad5cf5f9444d82545394543c46b06a05425befa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939947"
---
# <a name="iinkanalyzerfindnodesoftypeinsubtree-method"></a>Metodo IInkAnalyzer::FindNodesOfTypeInSubTree

Recupera tutti gli oggetti [**IContextNode**](icontextnode.md) del tipo specificato discendenti **dell'oggetto IContextNode** specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT FindNodesOfTypeInSubTree(
  [in]  const GUID          *pNodeType,
  [in]        IContextNode  *pContextNodeToSearchFrom,
  [out]       IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pNodeType* \[ Pollici\]
</dt> <dd>

**GUID che** specifica il tipo di nodo.

</dd> <dt>

*pContextNodeToSearchFrom* \[ Pollici\]
</dt> <dd>

Oggetto [**IContextNode**](icontextnode.md) i cui discendenti vengono cercati.

</dd> <dt>

*ppContextNodesFound* \[ Cambio\]
</dt> <dd>

Raccolta [**IContextNodes**](icontextnodes.md) contenente tutti i nodi di tipo *pNodeType* discendenti di *pContextNodeToSearchFrom.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppContextNodesFound* quando non è più necessario usare l'oggetto .

 

Se [**IInkAnalyzer**](iinkanalyzer.md) non contiene il nodo *pContextNodeToSearchFrom,* questo metodo restituisce un codice di errore.

La *proprietà pNodeType* deve contenere un identificatore univoco globale (GUID) dalle costanti [Context Node Types.](context-node-types.md)

Se [**IInkAnalyzer non**](iinkanalyzer.md) contiene un [**IContextNode di questo**](icontextnode.md)tipo, viene restituita una raccolta [**IContextNodes**](icontextnodes.md) vuota.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                 |
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

[**Metodo IInkAnalyzer::FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[**Metodo IInkAnalyzer::FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

 


---
description: Quando sottoposto a override in una classe derivata, valuta se un oggetto IContextNode specificato soddisfa i criteri.
ms.assetid: ade8e59c-6aeb-4a87-a95d-229f8f0b2223
title: 'Metodo IMatchesCriteriaCallBack:: EvaluateContextNode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMatchesCriteriaCallBack.EvaluateContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 554cf451396101de2238258de0a0706956f24a02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306752"
---
# <a name="imatchescriteriacallbackevaluatecontextnode-method"></a>Metodo IMatchesCriteriaCallBack:: EvaluateContextNode

Quando sottoposto a override in una classe derivata, valuta se un oggetto [**IContextNode**](icontextnode.md) specificato soddisfa i criteri.

## <a name="syntax"></a>Sintassi


```C++
HRESULT EvaluateContextNode(
  [in]  IContextNode *pContextNodeToEvaluate,
  [out] VARIANT_BOOL *pbResult
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pContextNodeToEvaluate* \[ in\]
</dt> <dd>

Oggetto [**IContextNode**](icontextnode.md) da valutare.

</dd> <dt>

*pbResult* \[ out\]
</dt> <dd>

**Variante \_ TRUE** se *pContextNodeToEvaluate* corrisponde ai criteri; in caso contrario, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Per usare il metodo [**IInkAnalyzer:: FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md) o [**IInkAnalyzer:: FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md), creare una classe che implementi [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md). Implementare **IMatchesCriteriaCallBack:: EvaluateContextNode** per restituire la **variante \_ true** se l'oggetto [**IContextNode**](icontextnode.md) corrisponde ai criteri e **Variant \_ false** in caso contrario. Per alcuni criteri, potrebbe essere necessario fornire un mezzo per inizializzare o gestire lo stato dell'oggetto **IMatchesCriteriaCallBack** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMatchesCriteriaCallBack**](imatchescriteriacallback.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





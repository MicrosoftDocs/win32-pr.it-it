---
description: Espone un metodo per valutare se un oggetto IContextNode soddisfa o meno un criterio specificato.
ms.assetid: 8b094882-e739-4088-87de-6ef4719b0b5b
title: Interfaccia IMatchesCriteriaCallBack (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMatchesCriteriaCallBack
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 960bd221bdd1f621f6ec4deb5ea167f5bf9ee4d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525320"
---
# <a name="imatchescriteriacallback-interface"></a>Interfaccia IMatchesCriteriaCallBack

Espone un metodo per valutare se un oggetto [**IContextNode**](icontextnode.md) soddisfa o meno un criterio specificato.

## <a name="members"></a>Membri

L'interfaccia **IMatchesCriteriaCallBack** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IMatchesCriteriaCallBack** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IMatchesCriteriaCallBack** dispone di questi metodi.



| Metodo                                                                      | Descrizione                                                                                                                                  |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**EvaluateContextNode**](imatchescriteriacallback-evaluatecontextnode.md) | Quando sottoposto a override in una classe derivata, valuta se un oggetto [**IContextNode**](icontextnode.md) specificato soddisfa i criteri.<br/> |



 

## <a name="remarks"></a>Commenti

Per usare il metodo [**IInkAnalyzer:: FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md) o [**IInkAnalyzer:: FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md), creare una classe che implementi **IMatchesCriteriaCallBack**. Implementare [**IMatchesCriteriaCallBack:: EvaluateContextNode**](imatchescriteriacallback-evaluatecontextnode.md) per restituire la **variante \_ true** se l'oggetto [**IContextNode**](icontextnode.md) corrisponde ai criteri e **Variant \_ false** in caso contrario. Per alcuni criteri, potrebbe essere necessario fornire un mezzo per inizializzare o gestire lo stato dell'oggetto **IMatchesCriteriaCallBack** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Metodo IInkAnalyzer:: FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 


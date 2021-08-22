---
description: Espone un metodo per valutare se un oggetto IContextNode soddisfa o meno un criterio specificato.
ms.assetid: 8b094882-e739-4088-87de-6ef4719b0b5b
title: Interfaccia IMatchesCriteriaCallBack (IACom.h)
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
ms.openlocfilehash: bc661f47c77d615df95f63e58beccbbf125b93078392a63f86ed50f52cc5636d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718970"
---
# <a name="imatchescriteriacallback-interface"></a>Interfaccia IMatchesCriteriaCallBack

Espone un metodo per valutare se un [**oggetto IContextNode**](icontextnode.md) soddisfa o meno un criterio specificato.

## <a name="members"></a>Membri

**L'interfaccia IMatchesCriteriaCallBack** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IMatchesCriteriaCallBack** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **IMatchesCriteriaCallBack.**



| Metodo                                                                      | Descrizione                                                                                                                                  |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**EvaluateContextNode**](imatchescriteriacallback-evaluatecontextnode.md) | In caso di override in una classe derivata, valuta se un oggetto [**IContextNode**](icontextnode.md) specificato soddisfa i criteri.<br/> |



 

## <a name="remarks"></a>Commenti

Per usare il metodo [**IInkAnalyzer::FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md) o [**IInkAnalyzer::FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md), creare una classe che implementa **IMatchesCriteriaCallBack.** Implementare [**IMatchesCriteriaCallBack::EvaluateContextNode**](imatchescriteriacallback-evaluatecontextnode.md) per restituire **VARIANT \_ TRUE** se l'oggetto [**IContextNode**](icontextnode.md) corrisponde ai criteri e **VARIANT \_ FALSE** in caso contrario. Per alcuni criteri, potrebbe essere necessario fornire un modo per inizializzare o gestire lo stato **dell'oggetto IMatchesCriteriaCallBack.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Metodo IInkAnalyzer::FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[**Metodo IInkAnalyzer::FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 


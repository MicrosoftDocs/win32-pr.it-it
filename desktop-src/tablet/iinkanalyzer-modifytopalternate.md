---
description: Modifica l'alternanza principale corrente nell'alternativa specificata e cancella il tipo di conferma per tutti gli oggetti IContextNode associati all'alternativa.
ms.assetid: a4ff7e82-623f-4501-9641-5235c3083757
title: 'Metodo IInkAnalyzer:: ModifyTopAlternate (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.ModifyTopAlternate
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: da2fcde7015e993e13e47673b271c560b6c3d72a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307379"
---
# <a name="iinkanalyzermodifytopalternate-method"></a>Metodo IInkAnalyzer:: ModifyTopAlternate

Modifica l'alternanza principale corrente nell'alternativa specificata e cancella il tipo di conferma per tutti gli oggetti [**IContextNode**](icontextnode.md) associati all'alternativa.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ModifyTopAlternate(
  [in] IAnalysisAlternate *pAlternate
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pAlternate* \[ in\]
</dt> <dd>

Oggetto [**IAnalysisAlternate**](ianalysisalternate.md) contenente la nuova alternativa principale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Per ottenere le alternative di analisi, usare il metodo [**IInkAnalyzer:: Getalternas**](iinkanalyzer-getalternates.md), il metodo [**IInkAnalyzer:: GetAlternatesForContextNodes**](iinkanalyzer-getalternatesforcontextnodes.md)o il metodo [**IInkAnalyzer:: GetAlternatesForStrokes**](iinkanalyzer-getalternatesforstrokes.md). Per ottenere gli oggetti [**IContextNode**](icontextnode.md) associati a un'alternativa di analisi, usare il [**Metodo IAnalysisAlternate:: GetAlternateNodes**](ianalysisalternate-getalternatenodes.md).

Per modificare il tipo di conferma per un nodo di contesto, utilizzare [**IContextNode:: Confirm**](icontextnode-confirm.md).

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

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**ConfirmationType**](confirmationtype.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





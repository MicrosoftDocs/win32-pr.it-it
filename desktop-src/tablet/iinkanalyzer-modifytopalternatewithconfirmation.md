---
description: Modifica l'alternanza principale corrente nel IAnalysisAlternate specificato.
ms.assetid: 0867a662-d172-4ca2-a41f-49c0ea454768
title: 'Metodo IInkAnalyzer:: ModifyTopAlternateWithConfirmation (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.ModifyTopAlternateWithConfirmation
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 60b0221e7d27cfd5d601dcf77e80a297045d39a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343691"
---
# <a name="iinkanalyzermodifytopalternatewithconfirmation-method"></a>Metodo IInkAnalyzer:: ModifyTopAlternateWithConfirmation

Modifica l'alternanza principale corrente nel [**IAnalysisAlternate**](ianalysisalternate.md)specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ModifyTopAlternateWithConfirmation(
  [in] IAnalysisAlternate *alternate,
  [in] VARIANT_BOOL       fconfirmAutomatically
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*alternativa* \[ in\]
</dt> <dd>

Alternativa dell'analisi da impostare come nuova alternativa principale.

</dd> <dt>

*fconfirmAutomatically* \[ in\]
</dt> <dd>

**Variante \_ TRUE** per impostare tutti i nodi di contesto foglia dell'input penna che corrispondono all'alternativa di analisi a un tipo di conferma **ConfirmationType \_ NodeTypeAndProperties** (vedere [**IContextNode::**](icontextnode-isconfirmed.md) istrued and [**ConfirmationType**](confirmationtype.md)); **Variante \_ FALSE** per impostare tutti i nodi di contesto foglia dell'input penna che corrispondono all'analisi alternativa a un tipo di conferma **ConfirmationType \_ None**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Per ottenere le alternative di analisi, usare il metodo [**IInkAnalyzer:: Getalternas**](iinkanalyzer-getalternates.md), il metodo [**IInkAnalyzer:: GetAlternatesForContextNodes**](iinkanalyzer-getalternatesforcontextnodes.md)o il metodo [**IInkAnalyzer:: GetAlternatesForStrokes**](iinkanalyzer-getalternatesforstrokes.md). Per ottenere gli oggetti nodo di contesto associati a un'alternativa di analisi, usare il [**Metodo IAnalysisAlternate:: GetAlternateNodes**](ianalysisalternate-getalternatenodes.md).

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

[**ConfirmationType di analisi dell'input penna**](confirmationtype.md)
</dt> <dt>

[Riferimento](ink-analysis-reference.md)
</dt> </dl>

 

 





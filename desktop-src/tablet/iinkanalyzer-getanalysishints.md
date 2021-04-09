---
description: Ottiene tutti gli oggetti IContextNode hint di analisi collegati a IInkAnalyzer.
ms.assetid: 97cff025-3d9e-4137-b1ac-635153804744
title: 'Metodo IInkAnalyzer:: GetAnalysisHints (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAnalysisHints
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c5ce66eeb6362ed74f1df1a38f220603d3a30117
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129455"
---
# <a name="iinkanalyzergetanalysishints-method"></a>Metodo IInkAnalyzer:: GetAnalysisHints

Ottiene tutti gli oggetti [**IContextNode**](icontextnode.md) hint di analisi collegati a [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetAnalysisHints(
  [out] IContextNodes **ppAnalysisHints
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppAnalysisHints* \[ out\]
</dt> <dd>

Puntatore a tutti gli oggetti [**IContextNode**](icontextnode.md) hint di analisi in [**IInkAnalyzer**](iinkanalyzer.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppAnalysisHints* quando non è più necessario utilizzare l'oggetto.

 

Questo metodo restituisce una raccolta vuota se nessun nodo hint di analisi è associato a [**IInkAnalyzer**](iinkanalyzer.md).

Un nodo di hint di analisi è un [**IContextNode**](icontextnode.md) con un tipo di nodo di contesto di AnalysisHint (vedere tipi di [nodo](context-node-types.md) [**IContextNode:: GetType**](icontextnode-gettype.md) e context).

Per aggiungere informazioni di contesto all'hint, utilizzare [**IContextNode:: AddPropertyData**](icontextnode-addpropertydata.md) con il parametro *pPropertyDataId* impostato su uno degli identificatori univoci globali (Guid) nelle costanti delle [proprietà dell'hint di analisi](analysis-hint-properties.md) .

Per individuare i valori delle proprietà impostati in un nodo di contesto, utilizzare [**IContextNode:: GetPropertyDataIds**](icontextnode-getpropertydataids.md). Per trovare il valore di una proprietà, usare [**IContextNode:: GetPropertyData**](icontextnode-getpropertydata.md).

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

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: CreateAnalysisHint**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**IInkAnalyzer::D Metodo eleteAnalysisHint**](iinkanalyzer-deleteanalysishint.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: GetAnalysisHintsByName**](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 


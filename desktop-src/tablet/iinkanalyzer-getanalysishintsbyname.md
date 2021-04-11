---
description: Recupera tutti gli oggetti IContextNode hint di analisi collegati a IInkAnalyzer e con il nome specificato.
ms.assetid: 15269ee0-055c-424e-be49-945f47e8a77e
title: 'Metodo IInkAnalyzer:: GetAnalysisHintsByName (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAnalysisHintsByName
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d86b18bfb8cf17097a36e35fc638dd9bd763d243
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226156"
---
# <a name="iinkanalyzergetanalysishintsbyname-method"></a>Metodo IInkAnalyzer:: GetAnalysisHintsByName

Recupera tutti gli oggetti [**IContextNode**](icontextnode.md) hint di analisi collegati a [**IInkAnalyzer**](iinkanalyzer.md) e con il nome specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetAnalysisHintsByName(
  [in]  BSTR          hintName,
  [out] IContextNodes **ppAnalysisHints
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hintName* \[ in\]
</dt> <dd>

Nome del suggerimento per il quale eseguire la ricerca.

</dd> <dt>

*ppAnalysisHints* \[ out\]
</dt> <dd>

Hint di analisi [**IContextNode**](icontextnode.md) gli oggetti in [**IInkAnalyzer**](iinkanalyzer.md) con il nome specificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md) i valori restituiti.

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppAnalysisHints* quando non è più necessario utilizzare l'oggetto.

 

Questo metodo restituisce una raccolta vuota se nessun nodo di hint di analisi di questo tipo è associato a [**IInkAnalyzer**](iinkanalyzer.md).

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

[**Metodo IInkAnalyzer:: GetAnalysisHints**](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 


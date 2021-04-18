---
description: Annulla l'operazione di analisi corrente.
ms.assetid: 909bfa66-b6df-4730-95b7-809fc2170e85
title: 'Metodo IInkAnalyzer:: Abort (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Abort
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eac96809bfbe41e7d6a070782da3ffd0f6407c60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307403"
---
# <a name="iinkanalyzerabort-method"></a>Metodo IInkAnalyzer:: Abort

Annulla l'operazione di analisi corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Abort(
  [out] IAnalysisRegion **ppAbortedRegion
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppAbortedRegion* \[ out\]
</dt> <dd>

Puntatore a un [**IAnalysisRegion**](ianalysisregion.md) che rappresenta l'area dirty (vedere il [**Metodo IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)) dell'operazione di analisi corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppAbortedRegion* quando non è più necessario usare l'oggetto.

Questo metodo annulla l'operazione di analisi corrente.

Quando *ppAbortedRegion* è **null**, questo metodo esegue l'interruzione come normale, perché questo indica che il chiamante non ha alcun interesse nel valore restituito.

Il **Metodo IInkAnalyzer:: Abort** silenzia gli eventi [**\_ IAnalysisEvents:: results**](-ianalysisevents-results.md) e [**\_ IAnalysisEvents:: Activity**](-ianalysisevents-activity.md) per l'operazione di analisi corrente.

Il **Metodo IInkAnalyzer:: Abort** viene eseguito in modo asincrono finché non viene annullata l'operazione di analisi in background corrente. Poiché il processo di annullamento è asincrono, l'applicazione può eseguire altre attività mentre il opertions di analisi corrente viene annullato.

Se non sono in corso operazioni di analisi, questo metodo restituisce un'area di analisi vuota.

Se è in corso un'operazione di analisi, questo metodo annulla l'operazione.

Se sono in corso operazioni di analisi sincrone e asincrone, questo metodo annulla l'operazione sincrona.

Se questo metodo viene chiamato più di una volta per la stessa operazione di analisi, la prima chiamata restituisce l'area dirty per l'operazione e le chiamate successive restituiscono un'area vuota.

Se l'applicazione mantiene una struttura di dati personalizzata sincronizzata con quella di [**IInkAnalyzer**](iinkanalyzer.md), la chiamata al **Metodo IInkAnalyzer:: Abort** può lasciare il documento con risultati parziali. Per evitare questo problema, non chiamare il **Metodo IInkAnalyzer:: Abort** tra il momento in cui **IInkAnalyzer** riceve l'evento [**\_ IAnalysisProxyEvents:: InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) e l'ora in cui **IInkAnalyzer** riceve l'evento [**\_ IAnalysisEvents:: IntermediateResults ()**](-ianalysisevents-intermediateresults.md) o [**\_ IAnalysisEvents:: results**](-ianalysisevents-results.md) .

Per altre informazioni sulla sincronizzazione dei dati dell'applicazione con Ink Analyzer, vedere [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).

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

[**Metodo IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: SetDirtyRegion**](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 


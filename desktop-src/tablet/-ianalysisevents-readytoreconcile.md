---
description: Si verifica quando IInkAnalyzer è pronto per risolvere i risultati dell'analisi in background con lo stato corrente.
ms.assetid: 63cf48eb-9d1e-4017-a4eb-55d811f7e6cf
title: 'Evento _IAnalysisEvents:: ReadyToReconcile (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.ReadyToReconcile
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4f3144f34dc680f9bc31f51b9e6b4284a70fb9bc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104234553"
---
# <a name="_ianalysiseventsreadytoreconcile-event"></a>\_Evento IAnalysisEvents:: ReadyToReconcile

Si verifica quando [**IInkAnalyzer**](iinkanalyzer.md) è pronto per risolvere i risultati dell'analisi in background con lo stato corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ReadyToReconcile();
```



## <a name="parameters"></a>Parametri

Questo evento non contiene parametri.

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

[**IInkAnalyzer**](iinkanalyzer.md) esegue la riconciliazione automatica quando viene impostato il flag **AnalysisModes \_ AutomaticReconciliation** dell'analizzatore di input penna (vedere il [**Metodo IInkAnalyzer:: SetAnalysisModes**](iinkanalyzer-setanalysismodes.md)). Quando il flag **AnalysisModes \_ AutomaticReconciliation** non è impostato, l'applicazione deve riconciliare manualmente i risultati dell'analisi in background.

Per eseguire la riconciliazione manuale, attenersi alla seguente procedura.

1.  Cancellare il flag **\_ AutomaticReconciliation AnalysisModes** dell'analizzatore di input penna.
2.  Gestire l'evento **\_ IAnalysisEvents:: ReadyToReconcile** .
3.  Per risolvere i risultati dell'analisi, chiamare il metodo [**IInkAnalyzer:: riconcilia**](iinkanalyzer-reconcile.md) dal gestore eventi per l'evento **\_ IAnalysisEvents:: ReadyToReconcile** . Per annullare l'operazione di analisi in background corrente, chiamare il metodo [**IInkAnalyzer:: Abort**](iinkanalyzer-abort.md) dal gestore eventi per l'evento **\_ IAnalysisEvents:: ReadyToReconcile** .

Il [**IInkAnalyzer**](iinkanalyzer.md) genera questo evento prima che venga generato l'evento [**\_ IAnalysisProxyEvents:: InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) .

Per altre informazioni sulla sincronizzazione dei dati dell'applicazione con [**IInkAnalyzer**](iinkanalyzer.md), vedere [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).

[**IInkAnalyzer**](iinkanalyzer.md) genera questo evento durante l'analisi in background.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_IAnalysisEvents**](-ianalysisevents.md)
</dt> <dt>

[**AnalysisModes**](analysismodes.md)
</dt> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: riconcilia**](iinkanalyzer-reconcile.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





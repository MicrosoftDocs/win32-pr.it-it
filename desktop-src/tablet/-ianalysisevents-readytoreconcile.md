---
description: Si verifica quando IInkAnalyzer è pronto per riconciliare i risultati dell'analisi in background con lo stato corrente.
ms.assetid: 63cf48eb-9d1e-4017-a4eb-55d811f7e6cf
title: _IAnalysisEvents::ReadyToReconcile (IACom.h)
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
ms.openlocfilehash: b65606675d8ae5aed694df87f35667a71fad2576344231a4e329783be4b31426
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111271"
---
# <a name="_ianalysiseventsreadytoreconcile-event"></a>\_Evento IAnalysisEvents::ReadyToReconcile

Si verifica quando [**IInkAnalyzer**](iinkanalyzer.md) è pronto per riconciliare i risultati dell'analisi in background con lo stato corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ReadyToReconcile();
```



## <a name="parameters"></a>Parametri

Questo evento non ha parametri.

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

[**IInkAnalyzer**](iinkanalyzer.md) esegue la riconciliazione automatica quando è impostato il flag **AnalysisModes \_ AutomaticReconciliation** dell'analizzatore input penna (vedere [**Metodo IInkAnalyzer::SetAnalysisModes**](iinkanalyzer-setanalysismodes.md)). Quando il flag **AnalysisModes \_ AutomaticReconciliation** non è impostato, l'applicazione deve riconciliare manualmente i risultati dell'analisi in background.

Per eseguire la riconciliazione manuale, seguire questa procedura.

1.  Cancellare il flag **AnalysisModes \_ AutomaticReconciliation** dell'analizzatore input penna.
2.  Gestire **\_ l'evento IAnalysisEvents::ReadyToReconcile.**
3.  Per riconciliare i risultati dell'analisi, chiamare il metodo [**IInkAnalyzer::Reconcile dal**](iinkanalyzer-reconcile.md) gestore eventi per l'evento **\_ IAnalysisEvents::ReadyToReconcile.** Per annullare l'operazione di analisi in background corrente, chiamare il metodo [**IInkAnalyzer::Abort dal**](iinkanalyzer-abort.md) gestore eventi per l'evento **\_ IAnalysisEvents::ReadyToReconcile.**

[**IInkAnalyzer**](iinkanalyzer.md) genera questo evento prima di generare l'evento [**\_ IAnalysisProxyEvents::InkAnalyzerStateChanging.**](-ianalysisproxyevents-inkanalyzerstatechanging.md)

Per altre informazioni sulla sincronizzazione dei dati dell'applicazione con [**IInkAnalyzer,**](iinkanalyzer.md)vedere [Proxy dati con l'analisi dell'input penna](data-proxy-with-ink-analysis.md).

[**L'oggetto IInkAnalyzer**](iinkanalyzer.md) genera questo evento durante l'analisi in background.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_IAnalysisEvents**](-ianalysisevents.md)
</dt> <dt>

[**Analysismodes**](analysismodes.md)
</dt> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Metodo IInkAnalyzer::Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Metodo IInkAnalyzer::BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**Metodo IInkAnalyzer::Reconcile**](iinkanalyzer-reconcile.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





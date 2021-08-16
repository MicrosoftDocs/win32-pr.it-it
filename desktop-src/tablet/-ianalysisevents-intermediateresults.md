---
description: Si verifica al termine della fase di analisi intermedia corrente.
ms.assetid: 9ade61f4-bcfe-4c49-bda1-b60aaf780935
title: evento _IAnalysisEvents::IntermediateResults (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.IntermediateResults
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 9efead00094fdcd773c3ac90b0d626e2036030171bcf3be011323b6da70fb665
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857197"
---
# <a name="_ianalysiseventsintermediateresults-event"></a>\_Evento IAnalysisEvents::IntermediateResults

Si verifica al termine della fase di analisi intermedia corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IntermediateResults(
  [in] IInkAnalyzer    *pInkAnalyzer,
  [in] IAnalysisStatus *pAnalysisStatus
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pInkAnalyzer* \[ Pollici\]
</dt> <dd>

[**IInkAnalyzer che**](iinkanalyzer.md) esegue l'analisi.

</dd> <dt>

*pAnalysisStatus* \[ Pollici\]
</dt> <dd>

Oggetto [**IAnalysisStatus**](ianalysisstatus.md) che rappresenta lo stato dei risultati intermedi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Commenti

[**L'IInkAnalyzer**](iinkanalyzer.md) genera questo evento dopo aver riconciliato i risultati intermedi per la fase di analisi corrente.

Se l'applicazione mantiene la propria struttura di dati, sincronizzata con quella di [**IInkAnalyzer,**](iinkanalyzer.md)questo evento indica che **IInkAnalyzer** ha terminato di apportare modifiche ai dati interni per questa fase di analisi.

Bloccare la struttura dei dati [**quando IInkAnalyzer**](iinkanalyzer.md) genera l'evento [**\_ IAnalysisProxyEvents::InkAnalyzerStateChanging.**](-ianalysisproxyevents-inkanalyzerstatechanging.md) Le modifiche alla struttura dei dati durante questa fase di analisi possono causare errori nell'analisi e nella sincronizzazione dell'input penna. È possibile sbloccare la struttura dei dati quando **IInkAnalyzer** genera l'evento **\_ IAnalysisEvents::IntermediateResults** o [**\_ IAnalysisEvents::Results.**](-ianalysisevents-results.md)

Per altre informazioni sulla sincronizzazione dei dati dell'applicazione con [**IInkAnalyzer,**](iinkanalyzer.md)vedere [Proxy dati con analisi input penna.](data-proxy-with-ink-analysis.md)

[**IInkAnalyzer**](iinkanalyzer.md) genera risultati intermedi solo quando per le modalità di analisi è impostato il flag **\_ IntermediateResults di AnalysisModes** (vedere [**Metodo IInkAnalyzer::GetAnalysisModes).**](iinkanalyzer-getanalysismodes.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_IAnalysisEvents**](-ianalysisevents.md)
</dt> <dt>

[**Analysismodes**](analysismodes.md)
</dt> <dt>

[**\_IAnalysisEvents::Results**](-ianalysisevents-results.md)
</dt> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Metodo IInkAnalyzer::Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Metodo IInkAnalyzer::BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

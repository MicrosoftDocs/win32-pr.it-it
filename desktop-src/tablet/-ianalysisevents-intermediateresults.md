---
description: Si verifica al termine della fase di analisi intermedia corrente.
ms.assetid: 9ade61f4-bcfe-4c49-bda1-b60aaf780935
title: 'Evento _IAnalysisEvents:: IntermediateResults () (IACom. h)'
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
ms.openlocfilehash: 33430225746ddd1a4099f89112f14f99f2b6da84
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320905"
---
# <a name="_ianalysiseventsintermediateresults-event"></a>\_Evento IAnalysisEvents:: IntermediateResults ()

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

*pInkAnalyzer* \[ in\]
</dt> <dd>

[**IInkAnalyzer**](iinkanalyzer.md) che sta eseguendo l'analisi.

</dd> <dt>

*pAnalysisStatus* \[ in\]
</dt> <dd>

Oggetto [**IAnalysisStatus**](ianalysisstatus.md) che rappresenta lo stato dei risultati intermedi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

[**IInkAnalyzer**](iinkanalyzer.md) genera questo evento dopo aver riconciliato i risultati intermedi per la fase di analisi corrente.

Se l'applicazione mantiene la propria struttura di dati, sincronizzata con quella di [**IInkAnalyzer**](iinkanalyzer.md), questo evento indica che il **IInkAnalyzer** ha completato le modifiche ai dati interni per questa fase di analisi.

Bloccare la struttura dei dati quando [**IInkAnalyzer**](iinkanalyzer.md) genera l'evento [**\_ IAnalysisProxyEvents:: InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) . Le modifiche apportate alla struttura dei dati durante questa fase dell'analisi possono causare errori nell'analisi dell'input penna e nella sincronizzazione. È possibile sbloccare la struttura dei dati quando **IInkAnalyzer** genera l'evento **\_ IAnalysisEvents:: IntermediateResults ()** o [**\_ IAnalysisEvents:: results**](-ianalysisevents-results.md) .

Per altre informazioni sulla sincronizzazione dei dati dell'applicazione con [**IInkAnalyzer**](iinkanalyzer.md), vedere [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).

[**IInkAnalyzer**](iinkanalyzer.md) genera risultati intermedi solo quando le modalità di analisi hanno il flag **AnalysisModes \_ IntermediateResults ()** impostato (vedere il [**Metodo IInkAnalyzer:: GetAnalysisModes**](iinkanalyzer-getanalysismodes.md)).

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

[**\_IAnalysisEvents:: results**](-ianalysisevents-results.md)
</dt> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

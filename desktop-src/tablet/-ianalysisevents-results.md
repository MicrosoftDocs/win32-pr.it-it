---
description: Si verifica al termine della fase di analisi finale.
ms.assetid: 97318c2d-980e-436c-b97d-e064bace5bf0
title: 'Evento _IAnalysisEvents:: results (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.Results
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bd52a5ce4563827fb22a00f79113fe1e80e852b3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320918"
---
# <a name="_ianalysiseventsresults-event"></a>\_Evento IAnalysisEvents:: results

Si verifica al termine della fase di analisi finale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Results(
  [in] IInkAnalyzer    *pInkAnalyzer,
  [in] IAnalysisStatus *pAnalysisStatus
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pInkAnalyzer* \[ in\]
</dt> <dd>

[**IInkAnalyzer**](iinkanalyzer.md) che produce i risultati dell'analisi.

</dd> <dt>

*pAnalysisStatus* \[ in\]
</dt> <dd>

Oggetto [**IAnalysisStatus**](ianalysisstatus.md) che rappresenta lo stato dell'analisi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

[**IInkAnalyzer**](iinkanalyzer.md) genera questo evento dopo aver riconciliato i risultati per la fase di analisi finale.

Se l'applicazione chiama il [**Metodo IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md), questo evento segnala quando i risultati dell'analisi sono pronti.

Se l'applicazione mantiene la propria struttura di dati, sincronizzata con quella di [**IInkAnalyzer**](iinkanalyzer.md), questo evento indica che il **IInkAnalyzer** ha completato le modifiche ai dati interni per questa fase di analisi.

Bloccare la struttura dei dati quando [**IInkAnalyzer**](iinkanalyzer.md) genera l'evento [**\_ IAnalysisProxyEvents:: InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) . Le modifiche apportate alla struttura dei dati durante questa fase dell'analisi possono causare errori nell'analisi dell'input penna e nella sincronizzazione. Sbloccare la struttura dei dati quando **IInkAnalyzer** genera l'evento [**\_ IAnalysisEvents:: IntermediateResults ()**](-ianalysisevents-intermediateresults.md) o **\_ IAnalysisEvents:: results** .

Per altre informazioni sulla sincronizzazione dei dati dell'applicazione con [**IInkAnalyzer**](iinkanalyzer.md), vedere [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).

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

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**IAnalysisStatus**](ianalysisstatus.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





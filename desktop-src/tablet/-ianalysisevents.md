---
description: Specifica gli eventi associati ai passaggi di analisi di un oggetto IInkAnalyzer.
ms.assetid: 8cb75f99-aa39-44d1-a055-dc1fb3f6b292
title: _IAnalysisEvents interfaccia
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2f49455e3e6fb68b2884cda380c304d7655b70d49ff338bcfb7c36904b449019
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452166"
---
# <a name="_ianalysisevents-interface"></a>\_Interfaccia IAnalysisEvents

Specifica gli eventi associati ai passaggi di analisi di un [**oggetto IInkAnalyzer.**](iinkanalyzer.md)

-   [Eventi](/windows)

### <a name="events"></a>Eventi

**\_ L'interfaccia IAnalysisEvents** include questi eventi.



| Event                                                               | Descrizione                                                                                                                                                                                    |
|:--------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Attività**](-ianalysisevents-activity.md)                       | Si verifica durante le chiamate al [**metodo IInkAnalyzer::Analyze**](iinkanalyzer-analyze.md) o al metodo [**IInkAnalyzer::BackgroundAnalyze.**](iinkanalyzer-backgroundanalyze.md)<br/> |
| [**IntermediateResults**](-ianalysisevents-intermediateresults.md) | Si verifica al termine della fase di analisi intermedia corrente.<br/>                                                                                                                    |
| [**ReadyToReconcile**](-ianalysisevents-readytoreconcile.md)       | Si verifica quando [**IInkAnalyzer è**](iinkanalyzer.md) pronto per riconciliare i risultati dell'analisi in background con lo stato corrente.<br/>                                                  |
| [**Risultati**](-ianalysisevents-results.md)                         | Si verifica al termine della fase di analisi finale.<br/>                                                                                                                                   |
| [**UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md)   | Si verifica prima [**dell'accesso di IInkAnalyzer**](iinkanalyzer.md) ai dati del tratto.<br/>                                                                                                        |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

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

 


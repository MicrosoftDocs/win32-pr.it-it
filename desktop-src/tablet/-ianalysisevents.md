---
description: Specifica gli eventi associati ai passaggi di analisi di un oggetto IInkAnalyzer.
ms.assetid: 8cb75f99-aa39-44d1-a055-dc1fb3f6b292
title: Interfaccia _IAnalysisEvents
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
ms.openlocfilehash: 90e32669d8b542202f6166052c072f224bb2954a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314929"
---
# <a name="_ianalysisevents-interface"></a>\_Interfaccia IAnalysisEvents

Specifica gli eventi associati ai passaggi di analisi di un oggetto [**IInkAnalyzer**](iinkanalyzer.md) .

-   [Eventi](/windows)

### <a name="events"></a>Eventi

L'interfaccia **\_ IAnalysisEvents** presenta questi eventi.



| Event                                                               | Descrizione                                                                                                                                                                                    |
|:--------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Attività**](-ianalysisevents-activity.md)                       | Si verifica durante le chiamate al metodo [**IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md) o al metodo [**IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) .<br/> |
| [**IntermediateResults ()**](-ianalysisevents-intermediateresults.md) | Si verifica al termine della fase di analisi intermedia corrente.<br/>                                                                                                                    |
| [**ReadyToReconcile**](-ianalysisevents-readytoreconcile.md)       | Si verifica quando [**IInkAnalyzer**](iinkanalyzer.md) è pronto per risolvere i risultati dell'analisi in background con lo stato corrente.<br/>                                                  |
| [**Risultati**](-ianalysisevents-results.md)                         | Si verifica al termine della fase di analisi finale.<br/>                                                                                                                                   |
| [**UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md)   | Si verifica prima che [**IInkAnalyzer**](iinkanalyzer.md) acceda ai dati del tratto.<br/>                                                                                                        |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

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

 


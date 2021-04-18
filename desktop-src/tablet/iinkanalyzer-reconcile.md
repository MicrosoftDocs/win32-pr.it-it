---
description: "Applica i risultati di un'operazione di analisi dell'input penna in background all'albero del nodo di contesto per le parti dell'albero che non sono state modificate dall'applicazione dalla chiamata al metodo IInkAnalyzer:: BackgroundAnalyze."
ms.assetid: 60e15d4f-6e81-48b9-b7f3-97d2de5c0c1c
title: 'Metodo IInkAnalyzer:: riconcilia (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Reconcile
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 33229c7da47f294f317d2216d9e9bf4f6b114599
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307378"
---
# <a name="iinkanalyzerreconcile-method"></a>Metodo IInkAnalyzer:: riconcilia

Applica i risultati di un'operazione di analisi dell'input penna in background all'albero del nodo di contesto per le parti dell'albero che non sono state modificate dall'applicazione dalla chiamata al [**Metodo IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT Reconcile();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Per impostazione predefinita, [**IInkAnalyzer**](iinkanalyzer.md) esegue una fase di riconciliazione automatica immediatamente prima di generare gli eventi [**\_ IAnalysisEvents:: IntermediateResults ()**](-ianalysisevents-intermediateresults.md) e [**\_ IAnalysisEvents:: results**](-ianalysisevents-results.md) .

Per disabilitare la riconciliazione automatica, deselezionare il flag **AnalysisModes \_ AutomaticReconciliation** dalle modalità di analisi dell'analizzatore di input penna (vedere il [**Metodo IInkAnalyzer:: SetAnalysisModes**](iinkanalyzer-setanalysismodes.md) e [**AnalysisModes**](analysismodes.md)). Il metodo [**IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) restituisce un errore quando la riconciliazione automatica è disabilitata e l'applicazione non gestisce l'evento [**\_ IAnalysisEvents:: ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) . L'applicazione deve chiamare il metodo **IInkAnalyzer:: riconcilia Method** prima che [**IInkAnalyzer**](iinkanalyzer.md) possa continuare a elaborare i risultati o continuare l'analisi per la fase di analisi corrispondente.

L'applicazione può apportare modifiche, ad esempio l'aggiunta o la rimozione di tratti e la modifica dei dati del tratto, nell'albero del nodo di contesto dell'oggetto [**IInkAnalyzer**](iinkanalyzer.md) durante l'analisi in background. Tali modifiche possono invalidare parti dei risultati dell'analisi in background. Questo metodo applica i risultati dell'analisi solo all'albero del nodo di contesto dell'analizzatore per le parti della struttura ad albero che l'applicazione non è stata modificata. Questo metodo aggiunge anche aree contenenti risultati di analisi invalidati all'area dirty dell'oggetto **IInkAnalyzer** (vedere il [**Metodo IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).

Per ulteriori informazioni sull'utilizzo di per analizzare l'input penna, vedere [Cenni preliminari sull'analisi dell'input penna](ink-analysis-overview.md). [**AnalysisModes**](analysismodes.md)

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

[**Metodo IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**\_IAnalysisEvents:: ReadyToReconcile**](-ianalysisevents-readytoreconcile.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





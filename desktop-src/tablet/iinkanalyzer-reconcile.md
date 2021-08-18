---
description: Applica i risultati di un'operazione di analisi dell'input penna in background all'albero del nodo di contesto per le parti dell'albero che non sono state modificate dall'applicazione dopo la chiamata al metodo IInkAnalyzer::BackgroundAnalyze.
ms.assetid: 60e15d4f-6e81-48b9-b7f3-97d2de5c0c1c
title: Metodo IInkAnalyzer::Reconcile (IACom.h)
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
ms.openlocfilehash: 3b16497a7f7822bf1557e3e686a81497a4e3723e71f115a1a7d6aa59d8381db2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092031"
---
# <a name="iinkanalyzerreconcile-method"></a>Metodo IInkAnalyzer::Reconcile

Applica i risultati di un'operazione di analisi dell'input penna in background all'albero del nodo di contesto per le parti dell'albero che non sono state modificate dall'applicazione dopo la chiamata al metodo [**IInkAnalyzer::BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT Reconcile();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Commenti

Per impostazione predefinita, [**IInkAnalyzer**](iinkanalyzer.md) esegue una fase di riconciliazione automatica immediatamente prima di generare gli eventi [**\_ IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) e [**\_ IAnalysisEvents::Results.**](-ianalysisevents-results.md)

Per disabilitare la riconciliazione automatica, deselezionare il flag **AnalysisModes \_ AutomaticReconciliation** dalle modalità di analisi dell'analizzatore input penna (vedere [**Metodo IInkAnalyzer::SetAnalysisModes**](iinkanalyzer-setanalysismodes.md) [**e AnalysisModes).**](analysismodes.md) Il [**metodo IInkAnalyzer::BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) restituisce un errore quando la riconciliazione automatica è disabilitata e l'applicazione non gestisce l'evento [**\_ IAnalysisEvents::ReadyToReconcile.**](-ianalysisevents-readytoreconcile.md) L'applicazione deve chiamare il metodo **IInkAnalyzer::Reconcile** prima che [**IInkAnalyzer**](iinkanalyzer.md) possa continuare a elaborare i risultati o continuare l'analisi per la fase di analisi corrispondente.

L'applicazione può apportare modifiche, ad esempio l'aggiunta o la rimozione di tratti e la modifica dei dati dei tratti, nell'albero del nodo di contesto dell'oggetto [**IInkAnalyzer**](iinkanalyzer.md) durante l'analisi in background. Tali modifiche possono invalidare parti dei risultati dell'analisi in background. Questo metodo applica i risultati dell'analisi solo all'albero dei nodi di contesto dell'analizzatore per le parti dell'albero che l'applicazione non ha modificato. Questo metodo aggiunge anche aree contenenti risultati di analisi invalidati all'area dirty dell'oggetto **IInkAnalyzer** (vedere il metodo [**IInkAnalyzer::GetDirtyRegion).**](iinkanalyzer-getdirtyregion.md)

Per altre informazioni sull'uso di per analizzare l'input penna, vedere [Cenni preliminari sull'analisi dell'input penna.](ink-analysis-overview.md) [**AnalysisModes**](analysismodes.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Metodo IInkAnalyzer::BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





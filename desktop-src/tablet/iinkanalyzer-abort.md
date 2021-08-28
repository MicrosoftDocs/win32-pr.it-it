---
description: Annulla l'operazione di analisi corrente.
ms.assetid: 909bfa66-b6df-4730-95b7-809fc2170e85
title: Metodo IInkAnalyzer::Abort (IACom.h)
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
ms.openlocfilehash: 4f52b2037210e39533d1247cb338bb22a7785f354dbca6b615c6ada67eff3bb5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773601"
---
# <a name="iinkanalyzerabort-method"></a>Metodo IInkAnalyzer::Abort

Annulla l'operazione di analisi corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Abort(
  [out] IAnalysisRegion **ppAbortedRegion
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppAbortedRegion* \[ Cambio\]
</dt> <dd>

Puntatore a un [**oggetto IAnalysisRegion**](ianalysisregion.md) che rappresenta l'area dirty (vedere il metodo [**IInkAnalyzer::GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)) dell'operazione di analisi corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Chiamare [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) in *ppAbortedRegion* quando non è più necessario usare l'oggetto .

Questo metodo annulla l'operazione di analisi corrente.

Quando *ppAbortedRegion* è **NULL,** questo metodo esegue l'interruzione come di consueto, perché indica che il chiamante non ha alcun interesse per il valore restituito.

**Il metodo IInkAnalyzer::Abort** consente di disattivare gli eventi [**\_ IAnalysisEvents::Results**](-ianalysisevents-results.md) e [**\_ IAnalysisEvents::Activity**](-ianalysisevents-activity.md) per l'operazione di analisi corrente.

**Il metodo IInkAnalyzer::Abort** viene eseguito in modo asincrono fino all'annullamento dell'operazione di analisi in background corrente. Poiché il processo di annullamento è asincrono, l'applicazione può eseguire altre attività mentre le operzioni di analisi correnti vengono annullate.

Se non è in corso alcuna operazione di analisi, questo metodo restituisce un'area di analisi vuota.

Se è in corso un'operazione di analisi, questo metodo annulla l'operazione.

Se sono in corso operazioni di analisi sincrone e asincrone, questo metodo annulla l'operazione sincrona.

Se questo metodo viene chiamato più volte per la stessa operazione di analisi, la prima chiamata restituisce l'area dirty per l'operazione e le chiamate successive restituiscono un'area vuota.

Se l'applicazione mantiene la propria struttura di dati sincronizzata con quella di [**IInkAnalyzer,**](iinkanalyzer.md)la chiamata al metodo **IInkAnalyzer::Abort** può lasciare il documento con risultati parziali. Per evitare questo problema, non chiamare il metodo **IInkAnalyzer::Abort** tra il momento in cui **IInkAnalyzer** riceve l'evento [**\_ IAnalysisProxyEvents::InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) e il momento in cui **IInkAnalyzer** riceve l'evento [**\_ IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) o [**\_ IAnalysisEvents::Results.**](-ianalysisevents-results.md)

Per altre informazioni sulla sincronizzazione dei dati dell'applicazione con l'analizzatore input penna, vedere [Proxy dati con l'analisi dell'input penna](data-proxy-with-ink-analysis.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Metodo IInkAnalyzer::Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Metodo IInkAnalyzer::BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**Metodo IInkAnalyzer::GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[**Metodo IInkAnalyzer::SetDirtyRegion**](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 


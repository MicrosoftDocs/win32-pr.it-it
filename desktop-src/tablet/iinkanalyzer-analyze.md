---
description: Esegue l'analisi sincrona dell'input penna.
ms.assetid: 957845f3-96b4-4184-aaec-e266cbe47e46
title: Metodo IInkAnalyzer::Analyze (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Analyze
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 34548eed6611b8b0e867edc7ef23e1a7c7e20a796738e2750718ec91b1e5a5d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118044221"
---
# <a name="iinkanalyzeranalyze-method"></a>Metodo IInkAnalyzer::Analyze

Esegue l'analisi sincrona dell'input penna.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Analyze(
  [out] IAnalysisStatus **ppStatus
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppStatus* \[ Cambio\]
</dt> <dd>

Puntatore a un [**oggetto IAnalysisStatus**](ianalysisstatus.md) che descrive lo stato dell'operazione di analisi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppStatus* quando non è più necessario usare lo stato di analisi.

 

Questo metodo avvia un'operazione di analisi dell'input penna sincrona. L'analisi dell'input penna include l'analisi del layout, la classificazione di scrittura e disegno e il riconoscimento della grafia. Questo metodo restituisce dopo il completamento dell'operazione di analisi.

Questo metodo restituisce **E \_ POINTER** se *ppStatus* è **NULL.**

Durante una chiamata al metodo **IInkAnalyzer::Analyze** o [**IInkAnalyzer::BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md), [**IInkAnalyzer**](iinkanalyzer.md) analizza l'input penna all'interno della relativa area dirty (vedere [**Metodo IInkAnalyzer::GetDirtyRegion).**](iinkanalyzer-getdirtyregion.md) Tuttavia, **IInkAnalyzer** può espandere l'operazione di analisi per includere le aree adiacenti.

Questo metodo imposta l'area dirty [**dell'oggetto IInkAnalyzer**](iinkanalyzer.md) su un'area vuota. Se un altro thread ha aggiunto dati sui tratti che non sono stati analizzati, **IInkAnalyzer** aggiunge il rettangolo di selezione dei tratti non analizzati all'area dirty durante la fase di riconciliazione dell'analisi.

Questo metodo restituisce un errore se l'applicazione non gestisce [**\_ l'evento IAnalysisEvents::UpdateStrokesCache.**](-ianalysisevents-updatestrokescache.md)

[**IInkAnalyzer**](iinkanalyzer.md) non genera gli eventi [**\_ IAnalysisEvents::Results**](-ianalysisevents-results.md) e [**\_ IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) in risposta a questo metodo.

Per modificare il modo in cui viene eseguita l'analisi dell'input penna, usare il metodo [**IInkAnalyzer::SetAnalysisModes**](iinkanalyzer-setanalysismodes.md).

Per altre informazioni sull'analisi dell'input penna, vedere [Cenni preliminari sull'analisi dell'input penna](ink-analysis-overview.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene eseguita l'analisi dell'input penna in primo piano.


```C++
// Perform synchronous ink analysis.
IAnalysisStatus *pAnalysisStatus = NULL;
hr = this->m_spIInkAnalyzer->Analyze(&pAnalysisStatus);

if (SUCCEEDED(hr))
{
    // Insert code that processes the analysis results.
}

// Release this reference to the analysis status.
if (pAnalysisStatus != NULL)
{
    pAnalysisStatus->Release();
    pAnalysisStatus = NULL;
}
```



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

[**Analysismodes**](analysismodes.md)
</dt> <dt>

[**Metodo IInkAnalyzer::GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[**Metodo IInkAnalyzer::SetDirtyRegion**](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[**Metodo IInkAnalyzer::GetRootNode**](iinkanalyzer-getrootnode.md)
</dt> <dt>

[**Metodo IInkAnalyzer::BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> </dl>

 


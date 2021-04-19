---
description: Esegue l'analisi dell'input sincrono.
ms.assetid: 957845f3-96b4-4184-aaec-e266cbe47e46
title: 'Metodo IInkAnalyzer:: Analyze (IACom. h)'
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
ms.openlocfilehash: 2867064067b902105508a7742c6fec88fdcd58be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307395"
---
# <a name="iinkanalyzeranalyze-method"></a>Metodo IInkAnalyzer:: Analyze

Esegue l'analisi dell'input sincrono.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Analyze(
  [out] IAnalysisStatus **ppStatus
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppStatus* \[ out\]
</dt> <dd>

Puntatore a un [**IAnalysisStatus**](ianalysisstatus.md) che descrive lo stato dell'operazione di analisi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppStatus* quando non è più necessario usare lo stato di analisi.

 

Questo metodo avvia un'operazione di analisi dell'input penna sincrona. L'analisi dell'input penna include l'analisi del layout, la scrittura e la classificazione del disegno e il riconoscimento grafia. Questo metodo viene restituito al termine dell'operazione di analisi.

Questo metodo restituisce **un \_ puntatore E** se *ppStatus* è **null**.

Durante una chiamata al metodo **IInkAnalyzer:: Analyze** o [**IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md), [**IInkAnalyzer**](iinkanalyzer.md) analizza l'input penna all'interno dell'area dirty (vedere il [**Metodo IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)). Tuttavia, **IInkAnalyzer** può espandere l'operazione di analisi per includere le aree adiacenti.

Questo metodo imposta l'area dirty dell'oggetto [**IInkAnalyzer**](iinkanalyzer.md) su un'area vuota. Se un altro thread ha aggiunto dati del tratto che non sono stati analizzati, **IInkAnalyzer** aggiunge il rettangolo di delimitazione dei tratti non analizzati alla relativa area dirty durante la fase di riconciliazione dell'analisi.

Questo metodo restituisce un errore se l'applicazione non gestisce l'evento [**\_ IAnalysisEvents:: UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) .

[**IInkAnalyzer**](iinkanalyzer.md) non genera gli eventi [**\_ IAnalysisEvents:: results**](-ianalysisevents-results.md) e [**\_ IAnalysisEvents:: IntermediateResults ()**](-ianalysisevents-intermediateresults.md) in risposta a questo metodo.

Per modificare la modalità di esecuzione dell'analisi dell'input penna, usare il [**Metodo IInkAnalyzer:: SetAnalysisModes**](iinkanalyzer-setanalysismodes.md).

Per altre informazioni sull'analisi dell'input penna, vedere [Cenni preliminari sull'analisi degli input penna](ink-analysis-overview.md).

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
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**AnalysisModes**](analysismodes.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: SetDirtyRegion**](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> </dl>

 


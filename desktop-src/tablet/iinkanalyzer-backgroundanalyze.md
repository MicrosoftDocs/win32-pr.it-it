---
description: Esegue l'analisi asincrona dell'input penna.
ms.assetid: 36427b80-5e3b-4c9a-bb49-e6b7f9301cbd
title: 'Metodo IInkAnalyzer:: BackgroundAnalyze (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.BackgroundAnalyze
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 606e1444f66884564a6b9f2007adfc26b2eb2ed1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526503"
---
# <a name="iinkanalyzerbackgroundanalyze-method"></a>Metodo IInkAnalyzer:: BackgroundAnalyze

Esegue l'analisi asincrona dell'input penna.

## <a name="syntax"></a>Sintassi


```C++
HRESULT BackgroundAnalyze();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Quando viene chiamato questo metodo, [**IInkAnalyzer**](iinkanalyzer.md) esegue l'analisi dell'input penna su un thread in background.

Questo metodo restituisce **\_ false** e non avvia una nuova operazione di analisi in background nelle circostanze seguenti.

-   Il [**IInkAnalyzer**](iinkanalyzer.md) sta attualmente eseguendo l'analisi in background.
-   l'area dirty (vedere il [**Metodo IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)) rappresenta un'area vuota.

[**IInkAnalyzer**](iinkanalyzer.md) analizza l'input penna all'interno dell'area dirty durante una chiamata al metodo [**IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md) o **IInkAnalyzer:: BackgroundAnalyze**. Tuttavia, **IInkAnalyzer** può espandere l'operazione di analisi per includere le aree adiacenti.

Questo metodo imposta l'area dirty su un'area vuota.

Se i dati del tratto sono stati aggiunti a [**IInkAnalyzer**](iinkanalyzer.md) dopo la chiamata al **Metodo IInkAnalyzer:: BackgroundAnalyze**, il **IInkAnalyzer** può aggiornare l'area dirty durante la fase di riconciliazione dell'analisi dell'input penna.

L'impostazione modalità di analisi (vedere [**IInkAnalyzer:: GetAnalysisModes metodo**](iinkanalyzer-getanalysismodes.md)) specifica il modo in cui [**IInkAnalyzer**](iinkanalyzer.md) esegue l'analisi in background. Per altre informazioni sull'analisi dell'input penna, vedere [Cenni preliminari sull'analisi degli input penna](ink-analysis-overview.md).

Questo metodo restituisce un codice di errore nelle circostanze seguenti.

-   L'applicazione ha impostato il valore [**AnalysisModes**](analysismodes.md) **AnalysisModes \_ IntermediateResults ()** in [**IInkAnalyzer**](iinkanalyzer.md) (vedere il [**Metodo IInkAnalyzer:: SetAnalysisModes**](iinkanalyzer-setanalysismodes.md)) e non gestisce l'evento [**\_ IAnalysisEvents:: IntermediateResults ()**](-ianalysisevents-intermediateresults.md) .
-   L'applicazione ha cancellato il valore [**AnalysisModes**](analysismodes.md) **AnalysisModes \_ AutomaticReconciliation** in [**IInkAnalyzer**](iinkanalyzer.md) (vedere il [**Metodo IInkAnalyzer:: SetAnalysisModes**](iinkanalyzer-setanalysismodes.md)) e non gestisce l'evento [**\_ IAnalysisEvents:: ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) .
-   L'applicazione non gestisce l'evento [**\_ IAnalysisEvents:: results**](-ianalysisevents-results.md) .
-   L'applicazione non gestisce l'evento [**\_ IAnalysisEvents:: UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) .

## <a name="examples"></a>Esempio

Nell'esempio seguente viene controllata l'area dirty dell'analizzatore di input penna e viene avviata l'analisi dell'input penna in background se l'area dirty non è vuota.


```C++
// Check that the ink analyzer's dirty region is not empty.
IAnalysisRegion *pDirtyRegion;
hr = this->m_spIInkAnalyzer->GetDirtyRegion(&pDirtyRegion);

if (SUCCEEDED(hr))
{
    VARIANT_BOOL bIsEmpty;
    hr = pDirtyRegion->IsEmpty(&bIsEmpty);

    if (SUCCEEDED(hr))
    {
        if (!bIsEmpty)
        {
            // Insert code that prepares the application for background
            // ink analysis here.

            // Start background ink analysis. The _IAnalysisEvents::Results
            // event signals when background ink analysis is complete.
            hr = this->m_spIInkAnalyzer->BackgroundAnalyze();
        }
    }
}

// Free the memory for the dirty region.
if (pDirtyRegion != NULL)
{
    pDirtyRegion->Release();
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

[**Metodo IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: GetAnalysisModes**](iinkanalyzer-getanalysismodes.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: SetAnalysisModes**](iinkanalyzer-setanalysismodes.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: SetDirtyRegion**](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





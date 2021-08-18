---
description: Rappresenta lo stato dell'operazione di analisi input penna descrivendo se l'analisi è stata completata correttamente e se si sono verificati avvisi.
ms.assetid: 57910a1d-3472-4689-ba0d-a220145e77c4
title: Interfaccia IAnalysisStatus (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisStatus
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 006b042981392ecdd52508181c7a5cde270d2e0195fe9c8b971c142361ab6081
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719998"
---
# <a name="ianalysisstatus-interface"></a>Interfaccia IAnalysisStatus

Rappresenta lo stato dell'operazione di analisi input penna descrivendo se l'analisi è stata completata correttamente e se si sono verificati avvisi.

## <a name="members"></a>Membri

**L'interfaccia IAnalysisStatus** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IAnalysisStatus** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **IAnalysisStatus.**



| Metodo                                                                     | Descrizione                                                                                                                                                                                    |
|:---------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAppliedChangesRegion**](ianalysisstatus-getappliedchangesregion.md) | Recupera l'area del documento che corrisponde alle modifiche apportate nell'albero dei nodi di contesto dell'oggetto [**IInkAnalyzer**](iinkanalyzer.md) come risultato dell'analisi dell'input penna.<br/> |
| [**GetWarnings**](ianalysisstatus-getwarnings.md)                         | Recupera una raccolta [**IAnalysisWarnings**](ianalysiswarnings.md) che descrive eventuali errori e avvisi generati dall'operazione di analisi.<br/>                                  |
| [**IsSuccessful**](ianalysisstatus-issuccessful.md)                       | Recupera un riepilogo booleano dei risultati dell'operazione di analisi.<br/>                                                                                                               |



 

## <a name="examples"></a>Esempio

L'esempio seguente illustra una struttura di un gestore eventi per [**\_ l'evento IAnalysisEvents::Results.**](-ianalysisevents-results.md) Il gestore controlla [**IAnalysisStatus::IsSuccessful**](ianalysisstatus-issuccessful.md). Se l'operazione di analisi genera avvisi, il gestore scorre la raccolta di [**oggetti IAnalysisWarning.**](ianalysiswarning.md)


```C++
// _IAnalysisEvents::Results event handler.
STDMETHODIMP CMyClass::Results(
    IInkAnalyzer *pInkAnalyzer,
    IAnalysisStatus *pAnalysisStatus)
{
    // Check the status of the analysis operation.
    VARIANT_BOOL bResult = VARIANT_FALSE;
    HRESULT hr = pAnalysisStatus->IsSuccessful(&bResult);

    if( SUCCEEDED(hr) )
    {
        if( bResult )
        {
            // Insert code that handles a successful result.
        }
        else
        {
            // Get the analysis warnings.
            IAnalysisWarnings* pAnalysisWarnings = NULL;
            hr = pAnalysisStatus->GetWarnings(&pAnalysisWarnings);
            if (SUCCEEDED(hr))
            {
                // Iterate through the warning collection.
                ULONG warningCount = 0;
                hr = pAnalysisWarnings->GetCount(&warningCount);
                if (SUCCEEDED(hr))
                {
                    IAnalysisWarning *pAnalysisWarning = NULL;
                    AnalysisWarningCode analysisWarningCode;
                    for (ULONG index=0; index<warningCount; index++)
                    {
                        // Get an analysis warning.
                        hr = pAnalysisWarnings->GetAnalysisWarning(
                            index, &pAnalysisWarning);

                        if (SUCCEEDED(hr))
                        {
                            // Get the warning code for the warning.
                            hr = pAnalysisWarning->GetWarningCode(
                                &analysisWarningCode);

                            if (SUCCEEDED(hr))
                            {
                                // Insert code that handles each
                                // analysis warning.
                            }
                        }

                        // Release this reference to the analysis warning.
                        if (pAnalysisWarning != NULL)
                        {
                            pAnalysisWarning->Release();
                            pAnalysisWarning = NULL;
                        }

                        if (FAILED(hr))
                        {
                            break;
                        }
                    }
                }
            }

            // Release this reference to the analysis warnings collection.
            if (pAnalysisWarnings != NULL)
            {
                pAnalysisWarnings->Release();
                pAnalysisWarnings = NULL;
            }
        }
    }
    return hr;
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

[**Metodo IInkAnalyzer::Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Metodo IInkAnalyzer::BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 


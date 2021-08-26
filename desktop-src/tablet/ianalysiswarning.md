---
description: Rappresenta un avviso o un errore che si verifica durante un'operazione di analisi dell'input penna.
ms.assetid: a9b0564b-8a49-44bc-9dbc-60a2fd5b60f2
title: Interfaccia IAnalysisWarning (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 27e00533894560a84e73f8eb5682d1b70789ab5f2b21be5d6fe3682c543be6a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940381"
---
# <a name="ianalysiswarning-interface"></a>Interfaccia IAnalysisWarning

Rappresenta un avviso o un errore che si verifica durante un'operazione di analisi dell'input penna.

## <a name="members"></a>Membri

**L'interfaccia IAnalysisWarning** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IAnalysisWarning** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IAnalysisWarning** include questi metodi.



| Metodo                                                            | Descrizione                                                                                                                            |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**GetBackgroundError**](ianalysiswarning-getbackgrounderror.md) | Recupera il codice di errore per l'operazione di analisi dell'input penna in background se si è verificato un errore.<br/>                                    |
| [**GetHint**](ianalysiswarning-gethint.md)                       | Recupera l'hint di analisi che ha causato l'avviso<br/>                                                                        |
| [**GetNodeIds**](ianalysiswarning-getnodeids.md)                 | Recupera gli identificatori di tutti i nodi di contesto pertinenti associati a questo avviso.<br/>                              |
| [**GetWarningCode**](ianalysiswarning-getwarningcode.md)         | Recupera il tipo di avviso che si è verificato usando [**l'enumerazione AnalysisWarningCode.**](/windows/desktop/tablet/analysiswarningcode)<br/> |



 

## <a name="remarks"></a>Commenti

I tipi di avvisi che possono verificarsi sono descritti [**dall'enumerazione AnalysisWarningCode.**](/windows/desktop/tablet/analysiswarningcode) Spesso si verificano avvisi quando si tenta di usare una funzionalità non supportata da [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) usato da [**IInkAnalyzer.**](iinkanalyzer.md)

Alcuni avvisi indicano che [**IInkAnalyzer**](iinkanalyzer.md) non ha completato l'operazione di analisi. Per altre informazioni, vedere [**AnalysisWarningCode.**](/windows/desktop/tablet/analysiswarningcode)

## <a name="examples"></a>Esempio

L'esempio seguente illustra una struttura di un gestore eventi per [**\_ l'evento IAnalysisEvents::Results.**](-ianalysisevents-results.md) Il gestore controlla [**IAnalysisStatus::IsSuccessful**](ianalysisstatus-issuccessful.md). Se l'operazione di analisi genera avvisi, il gestore scorre la raccolta di **oggetti IAnalysisWarning.**


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

[**IAnalysisWarnings**](ianalysiswarnings.md)
</dt> <dt>

[**AnalysisWarningCode**](analysiswarningcode.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 


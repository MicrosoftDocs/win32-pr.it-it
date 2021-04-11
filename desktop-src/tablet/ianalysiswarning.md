---
description: Rappresenta un avviso o un errore che si verifica durante un'operazione di analisi dell'input penna.
ms.assetid: a9b0564b-8a49-44bc-9dbc-60a2fd5b60f2
title: Interfaccia IAnalysisWarning (IACom. h)
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
ms.openlocfilehash: 79e865ac909d6f9ee1862926ffab06f538661d6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129515"
---
# <a name="ianalysiswarning-interface"></a>Interfaccia IAnalysisWarning

Rappresenta un avviso o un errore che si verifica durante un'operazione di analisi dell'input penna.

## <a name="members"></a>Membri

L'interfaccia **IAnalysisWarning** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IAnalysisWarning** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IAnalysisWarning** dispone di questi metodi.



| Metodo                                                            | Descrizione                                                                                                                            |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**GetBackgroundError**](ianalysiswarning-getbackgrounderror.md) | Recupera il codice di errore per l'operazione di analisi dell'input penna in background se si è verificato un errore.<br/>                                    |
| [**GetHint**](ianalysiswarning-gethint.md)                       | Recupera l'hint di analisi che ha generato l'avviso<br/>                                                                        |
| [**GetNodeIds**](ianalysiswarning-getnodeids.md)                 | Recupera gli identificatori di qualsiasi nodo di contesto pertinente associato a questo avviso.<br/>                              |
| [**GetWarningCode**](ianalysiswarning-getwarningcode.md)         | Recupera il tipo di avviso che si è verificato utilizzando l'enumerazione [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) .<br/> |



 

## <a name="remarks"></a>Commenti

I tipi di avvisi che possono verificarsi sono descritti dall'enumerazione [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) . Spesso gli avvisi si verificano quando si tenta di usare una funzionalità non supportata dal [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) usato da [**IInkAnalyzer**](iinkanalyzer.md) .

Alcuni avvisi indicano che il [**IInkAnalyzer**](iinkanalyzer.md) non ha completato l'operazione di analisi. Per ulteriori informazioni, vedere [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrata una struttura di un gestore eventi per l'evento [**\_ IAnalysisEvents:: results**](-ianalysisevents-results.md) . Il gestore verifica [**IAnalysisStatus:: con esito positivo**](ianalysisstatus-issuccessful.md). Se l'operazione di analisi genera avvisi, il gestore scorre la raccolta di oggetti **IAnalysisWarning** .


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
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IAnalysisWarnings**](ianalysiswarnings.md)
</dt> <dt>

[**AnalysisWarningCode**](analysiswarningcode.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 


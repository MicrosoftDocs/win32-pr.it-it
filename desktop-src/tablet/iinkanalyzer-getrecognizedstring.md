---
description: Recupera la stringa di risultato migliore dell'operazione di riconoscimento per l'intero albero del nodo di contesto in IInkAnalyzer.
ms.assetid: 4aa57f41-3122-47a9-a60d-4a229e23f63c
title: 'Metodo IInkAnalyzer:: GetRecognizedString (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetRecognizedString
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 67afe9909fcabb8df880706b2b077ea602ccade6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751807"
---
# <a name="iinkanalyzergetrecognizedstring-method"></a>Metodo IInkAnalyzer:: GetRecognizedString

Recupera la stringa di risultato migliore dell'operazione di riconoscimento per l'intero albero del nodo di contesto in [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetRecognizedString(
  [out] BSTR *pbstrRecognizedString
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbstrRecognizedString* \[ out\]
</dt> <dd>

Stringa di risultato migliore dell'operazione di riconoscimento per l'intero albero del nodo di contesto in [**IInkAnalyzer**](iinkanalyzer.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per *pbstrRecognizedString* quando non è più necessario usare la stringa.

 

Questo metodo restituisce lo stesso valore dei dati della proprietà del nodo radice per la stringa riconosciuta. (Vedere il [**Metodo IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md), [**IContextNode:: GetPropertyData**](icontextnode-getpropertydata.md)e le [proprietà del nodo di contesto](context-node-properties.md)).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato un metodo che esamina l'albero dei risultati [**IContextNode**](icontextnode.md) dell'analizzatore di input penna. Se il IInkAnlyzer non sta attualmente eseguendo l'analisi dell'input penna, il metodo esegue le operazioni seguenti.

-   Ottiene la stringa di riconoscimento superiore.
-   Ottiene il nodo radice dell'analizzatore di input penna.
-   Chiama un metodo helper, `ExploreContextNode` , per esaminare il nodo radice e i relativi nodi figlio.


```C++
// Helper method that explores the current analysis results of an ink analyzer.
HRESULT CMyClass::ExploreAnalysisResults(
    IInkAnalyzer *pInkAnalyzer)
{
    // Check that the ink analyzer is not currently analyzing ink.
    VARIANT_BOOL bIsAnalyzing;
    HRESULT hr = pInkAnalyzer->IsAnalyzing(&bIsAnalyzing);

    if (SUCCEEDED(hr))
    {
        if (bIsAnalyzing)
        {
            return E_PENDING;
        }

        // Get the ink analyzer's best-result string.
        BSTR recognizedString = NULL;
        hr = pInkAnalyzer->GetRecognizedString(&recognizedString);

        if (SUCCEEDED(hr))
        {
            // Insert code that records the ink analyzer's best-result string here.

            // Get the ink analyzer's root node.
            IContextNode *pRootNode = NULL;
            hr = pInkAnalyzer->GetRootNode(&pRootNode);

            if (SUCCEEDED(hr))
            {
                // Call a helper method that recursively explores context
                // nodes and their subnodes.
                hr = this->ExploreContextNode(pRootNode);
            }

            // Release this reference to the root node.
            if (pRootNode != NULL)
            {
                pRootNode->Release();
                pRootNode = NULL;
            }
        }

        // Free the system resources for the recognized string.
        SysFreeString(recognizedString);
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

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 


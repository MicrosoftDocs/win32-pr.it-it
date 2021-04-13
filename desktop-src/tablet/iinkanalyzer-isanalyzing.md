---
description: Recupera un valore che indica se IInkAnalyzer esegue l'analisi dell'input penna.
ms.assetid: 3f3f6f29-0c90-47e1-938c-f1ce6ed8df47
title: 'Metodo IInkAnalyzer:: overanalyzing (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.IsAnalyzing
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 94275d157b2936b7ad0ae16d4d70b62475f19af9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526490"
---
# <a name="iinkanalyzerisanalyzing-method"></a>Metodo IInkAnalyzer:: overanalyzing

Recupera un valore che indica se [**IInkAnalyzer**](iinkanalyzer.md) esegue l'analisi dell'input penna.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsAnalyzing(
  [out] VARIANT_BOOL *pbAnalyzing
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbAnalyzing* \[ out\]
</dt> <dd>

**Variante \_ TRUE** se [**IInkAnalyzer**](iinkanalyzer.md) esegue l'analisi dell'input penna; in caso contrario, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Questa proprietà è una **variante \_ true** se [**IInkAnalyzer**](iinkanalyzer.md) esegue l'analisi sincrona o asincrona.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato un metodo che esamina l'albero dei risultati [**IContextNode**](icontextnode.md) dell'analizzatore di input penna. Se l'analizzatore di input penna non sta attualmente eseguendo l'analisi dell'input penna, il metodo esegue le operazioni seguenti.

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

[**Metodo IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





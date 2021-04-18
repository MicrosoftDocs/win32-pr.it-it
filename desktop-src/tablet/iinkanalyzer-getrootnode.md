---
description: Ottiene il IContextNode radice dell'albero del contesto dell'oggetto IInkAnalyzer.
ms.assetid: 6c073952-7962-4f38-89ae-f543e64e904f
title: 'Metodo IInkAnalyzer:: GetRootNode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetRootNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 280c1907558372d247f25a0f760990d7c3c53a07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307383"
---
# <a name="iinkanalyzergetrootnode-method"></a>Metodo IInkAnalyzer:: GetRootNode

Ottiene il [**IContextNode**](icontextnode.md) radice dell'albero del contesto dell'oggetto [**IInkAnalyzer**](iinkanalyzer.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetRootNode(
  [out] IContextNode **ppRootNode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppRootNode* \[ out\]
</dt> <dd>

[**IContextNode**](icontextnode.md) radice dell'albero del contesto dell'oggetto [**IInkAnalyzer**](iinkanalyzer.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppRootNode* quando non è più necessario usare il nodo radice.

 

[**IInkAnalyzer**](iinkanalyzer.md) gestisce un albero di oggetti [**IContextNode**](icontextnode.md) . Questi oggetti contengono sia l'input per l'analisi che i risultati dell'analisi. Quando i tratti vengono inizialmente aggiunti a **IInkAnalyzer**, **IInkAnalyzer** li assegna a un **IContextNode** di tipo UnclassifiedInk (vedere i tipi di [nodo](context-node-types.md) [**IContextNode:: GetType**](icontextnode-gettype.md) e context). Una volta analizzati i tratti, **IInkAnalyzer** li assegna agli oggetti **IContextNode** appropriati nell'albero. Per altre informazioni sull'uso di **IInkAnalyzer** per analizzare l'input penna, vedere [Cenni preliminari sull'analisi dell'input penna](ink-analysis-overview.md).

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

[**IContextNode**](icontextnode.md)
</dt> <dt>

[Tipi di nodo di contesto](context-node-types.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 


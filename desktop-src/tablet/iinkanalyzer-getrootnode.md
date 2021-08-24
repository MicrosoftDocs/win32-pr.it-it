---
description: Ottiene l'oggetto IContextNode radice dell'albero del contesto dell'oggetto IInkAnalyzer.
ms.assetid: 6c073952-7962-4f38-89ae-f543e64e904f
title: Metodo IInkAnalyzer::GetRootNode (IACom.h)
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
ms.openlocfilehash: 5ff2181eacd3df1d2815448a0c2d7cafce4d521fa0abbc7b26492d9c078982dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713421"
---
# <a name="iinkanalyzergetrootnode-method"></a>Metodo IInkAnalyzer::GetRootNode

Ottiene [**l'oggetto IContextNode radice**](icontextnode.md) dell'albero del contesto dell'oggetto [**IInkAnalyzer.**](iinkanalyzer.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetRootNode(
  [out] IContextNode **ppRootNode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppRootNode* \[ Cambio\]
</dt> <dd>

Oggetto [**IContextNode radice**](icontextnode.md) dell'albero del contesto dell'oggetto [**IInkAnalyzer.**](iinkanalyzer.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppRootNode* quando non è più necessario usare il nodo radice.

 

[**IInkAnalyzer**](iinkanalyzer.md) gestisce un albero di [**oggetti IContextNode.**](icontextnode.md) Questi oggetti contengono sia input per l'analisi che i risultati dell'analisi. Quando i tratti vengono aggiunti inizialmente a **IInkAnalyzer,** **IInkAnalyzer** li assegna a **un IContextNode** di tipo UnclassifiedInk (vedere [**IContextNode::GetType**](icontextnode-gettype.md) e Tipi di nodo [di contesto).](context-node-types.md) Dopo l'analisi dei tratti, **IInkAnalyzer** li assegna agli oggetti **IContextNode** appropriati nell'albero. Per altre informazioni sull'uso di **IInkAnalyzer** per analizzare l'input penna, vedere [Panoramica dell'analisi dell'input penna](ink-analysis-overview.md).

## <a name="examples"></a>Esempio

L'esempio seguente illustra un metodo che illustra l'albero dei risultati [**IContextNode**](icontextnode.md) dell'analizzatore input penna. Se IInkAnlyzer attualmente non esegue l'analisi dell'input penna, il metodo esegue le operazioni seguenti.

-   Ottiene la prima stringa di riconoscimento.
-   Ottiene il nodo radice dell'analizzatore input penna.
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
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[Tipi di nodo di contesto](context-node-types.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 


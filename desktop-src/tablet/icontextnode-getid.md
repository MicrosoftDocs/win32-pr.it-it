---
description: Recupera l'identificatore per l'oggetto IContextNode.
ms.assetid: 7578bcc1-7c69-45fc-b3c2-7350ce4df99c
title: 'Metodo IContextNode:: GetId (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ef316111c7464bac0339a4888b887bc5cf20b93f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879362"
---
# <a name="icontextnodegetid-method"></a>Metodo IContextNode:: GetId

Recupera l'identificatore per l'oggetto [**IContextNode**](icontextnode.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetId(
  [out] GUID *pId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PID* \[ out\]
</dt> <dd>

Identificatore per l'oggetto [**IContextNode**](icontextnode.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Ink Analyzer assegna un identificatore univoco a tutti i nodi di contesto creati. Durante l'analisi dell'input penna, Ink Analyzer può modificare l'identificatore per un nodo di contesto. Ad esempio, Ink Analyzer può riclassificare un nodo di Word come due nodi di Word, quindi assegnare l'identificatore originale a uno e un nuovo identificatore all'altro. In alternativa, è possibile che l'analizzatore di input penna riclassifichi due nodi di Word come un nodo di Word e assegnare uno degli identificatori originali al nuovo nodo di Word.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato un metodo helper che recupera le informazioni su un nodo specificato, il relativo parametro *pContextNode* . Questo metodo helper restituisce informazioni dai metodi seguenti.

-   **IContextNode:: GetId**
-   [**IContextNode:: GetType**](icontextnode-gettype.md)
-   [**IContextNode:: GetLocation**](icontextnode-getlocation.md)
-   [**IContextNode:: GetParentNode**](icontextnode-getparentnode.md)


```C++
// Helper method for collecting information about a context node.
HRESULT CMyClass::GetNodeInformation(
    IContextNode *pContextNode,
    GUID *pNodeIdentifier,
    GUID *pContextNodeType,
    IAnalysisRegion **ppAnalysisRegion,
    IContextNode **ppParentNode,
    IContextNodes **ppSubNodes)
{
    // Get the identifier of the context node.
    HRESULT hr = pContextNode->GetId(pNodeIdentifier);

    if (FAILED(hr))
    {
        return hr;
    }

    // Get the type identifier for the context node.
    hr = pContextNode->GetType(pContextNodeType);

    if (FAILED(hr))
    {
        return hr;
    }

    // Get the location of the context node.
    hr = pContextNode->GetLocation(ppAnalysisRegion);

    if (FAILED(hr))
    {
        return hr;
    }

    // Get the parent node of the context node.
    hr = pContextNode->GetParentNode(ppParentNode);

    if (FAILED(hr))
    {
        if ((*ppAnalysisRegion) != NULL)
        {
            (*ppAnalysisRegion)->Release();
            (*ppAnalysisRegion) = NULL;
        }
        return hr;
    }

    // Get the subnodes of the context node.
    hr = pContextNode->GetSubNodes(ppSubNodes);

    if (FAILED(hr))
    {
        if (*ppAnalysisRegion)
        {
            (*ppAnalysisRegion)->Release();
            (*ppAnalysisRegion) = NULL;
        }
        if (*ppParentNode)
        {
            (*ppParentNode)->Release();
            (*ppParentNode) = NULL;
        }
        return hr;
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

[**IContextNode**](icontextnode.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





---
description: Si verifica dopo che IInkAnalyzer crea un oggetto IContextNode.
ms.assetid: b4ba0d3b-da91-4cc7-b071-240155687b83
title: 'Evento _IAnalysisProxyEvents:: ContextNodeCreated (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeCreated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ac06a7fc45604e93408b1bb144ee7e884efd351e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "103968993"
---
# <a name="_ianalysisproxyeventscontextnodecreated-event"></a>\_Evento IAnalysisProxyEvents:: ContextNodeCreated

Si verifica dopo che [**IInkAnalyzer**](iinkanalyzer.md) crea un oggetto [**IContextNode**](icontextnode.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT ContextNodeCreated(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeCreated
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pInkAnalyzer* \[ in\]
</dt> <dd>

[**IInkAnalyzer**](iinkanalyzer.md) che crea l'oggetto [**IContextNode**](icontextnode.md) .

</dd> <dt>

*pContextNodeCreated* \[ in\]
</dt> <dd>

Nuovo oggetto [**IContextNode**](icontextnode.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Usare questo evento quando l'applicazione mantiene la propria struttura di dati, sincronizzata con quella di [**IInkAnalyzer**](iinkanalyzer.md). Questo evento si verifica durante la fase di riconciliazione dell'analisi dell'input penna o in risposta a un metodo dell'analizzatore di input penna che crea un [**IContextNode**](icontextnode.md).

Quando [**IInkAnalyzer**](iinkanalyzer.md) crea un [**IContextNode**](icontextnode.md), il nuovo **IContextNode** non contiene alcun tratto, non contiene collegamenti ad altri oggetti **IContextNode** e potrebbe non avere tutte le relative proprietà impostate. Inoltre, il nuovo **IContextNode** viene aggiunto alla fine della raccolta di nodi del nodo padre (vedere [**IContextNode:: GetParentNode**](icontextnode-getparentnode.md) e [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md)). Dopo questo evento, **IInkAnalyzer** può generare gli eventi seguenti.

-   Evento [**\_ IAnalysisProxyEvents:: StrokeReparented**](-ianalysisproxyevents-strokereparented.md) quando sposta un tratto da un nodo di contesto a un altro.
-   Evento [**\_ IAnalysisProxyEvents:: ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md) quando aggiunge un [**IContextLink**](icontextlink.md) a un [**IContextNode**](icontextnode.md).
-   Evento [**\_ IAnalysisProxyEvents:: ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md) quando modifica l'ordine di un [**IContextNode**](icontextnode.md) all'interno della relativa raccolta di nodi padre.
-   [**IInkAnalyzer**](iinkanalyzer.md) genera l'evento [**\_ IAnalysisProxyEvents:: ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) dopo che risolve lo stato di [**IContextNode**](icontextnode.md) per questa fase di analisi.

Per altre informazioni sulla sincronizzazione dei dati dell'applicazione con [**IInkAnalyzer**](iinkanalyzer.md), vedere [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





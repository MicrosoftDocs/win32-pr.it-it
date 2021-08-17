---
description: Si verifica dopo la creazione di un oggetto IContextNode da parte di IInkAnalyzer.
ms.assetid: b4ba0d3b-da91-4cc7-b071-240155687b83
title: _IAnalysisProxyEvents::ContextNodeCreated (IACom.h)
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
ms.openlocfilehash: 5938ffda54542602248c5d04da0726d932b381aaff092f1c2038dd37ae4631e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117675868"
---
# <a name="_ianalysisproxyeventscontextnodecreated-event"></a>\_Evento IAnalysisProxyEvents::ContextNodeCreated

Si verifica dopo la creazione di un oggetto [**IContextNode**](icontextnode.md) da parte di [**IInkAnalyzer.**](iinkanalyzer.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT ContextNodeCreated(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeCreated
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pInkAnalyzer* \[ Pollici\]
</dt> <dd>

Oggetto [**IInkAnalyzer che**](iinkanalyzer.md) crea [**l'oggetto IContextNode.**](icontextnode.md)

</dd> <dt>

*pContextNodeCreated* \[ Pollici\]
</dt> <dd>

Nuovo oggetto [**IContextNode.**](icontextnode.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Usare questo evento quando l'applicazione mantiene la propria struttura di dati, sincronizzata con quella di [**IInkAnalyzer.**](iinkanalyzer.md) Questo evento si verifica durante la fase di riconciliazione dell'analisi dell'input penna o in risposta a un metodo dell'analizzatore dell'input penna che crea [**un oggetto IContextNode.**](icontextnode.md)

Quando [**IInkAnalyzer**](iinkanalyzer.md) crea un [**oggetto IContextNode,**](icontextnode.md)il nuovo **IContextNode** non contiene tratti, non contiene collegamenti ad altri oggetti **IContextNode** e potrebbe non avere tutte le proprietà impostate. Inoltre, il nuovo **IContextNode** viene aggiunto alla fine della raccolta di sottonodi del nodo padre (vedere [**IContextNode::GetParentNode**](icontextnode-getparentnode.md) e [**IContextNode::GetSubNodes).**](icontextnode-getsubnodes.md) Dopo questo evento, **IInkAnalyzer** può generare gli eventi seguenti.

-   Evento [**\_ IAnalysisProxyEvents::StrokeReparented**](-ianalysisproxyevents-strokereparented.md) quando sposta un tratto da un nodo di contesto a un altro.
-   Evento [**\_ IAnalysisProxyEvents::ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md) quando aggiunge un [**oggetto IContextLink**](icontextlink.md) a [**un oggetto IContextNode**](icontextnode.md).
-   Evento [**\_ IAnalysisProxyEvents::ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md) quando cambia l'ordine di [**un oggetto IContextNode**](icontextnode.md) all'interno della raccolta di sottonodi del nodo padre.
-   [**IInkAnalyzer**](iinkanalyzer.md) genera l'evento [**\_ IAnalysisProxyEvents::ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) dopo aver risolto lo stato di [**IContextNode**](icontextnode.md) per questa fase di analisi.

Per altre informazioni sulla sincronizzazione dei dati dell'applicazione con [**IInkAnalyzer,**](iinkanalyzer.md)vedere [Proxy dati con](data-proxy-with-ink-analysis.md)Analisi input penna .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**Metodo IInkAnalyzer::Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Metodo IInkAnalyzer::BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





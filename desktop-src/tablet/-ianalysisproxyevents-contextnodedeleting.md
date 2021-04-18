---
description: Si verifica prima che IInkAnalyzer elimini un oggetto IContextNode.
ms.assetid: 9c89198e-cc64-4041-b7a3-457f94c4aeaf
title: "Evento _IAnalysisProxyEvents:: l'ContextNodeDeleting (IACom. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeDeleting
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 26488c5657b6d2765534f82b6eacae774adcf561
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320913"
---
# <a name="_ianalysisproxyeventscontextnodedeleting-event"></a>\_Evento IAnalysisProxyEvents:: l'ContextNodeDeleting

Si verifica prima che [**IInkAnalyzer**](iinkanalyzer.md) elimini un oggetto [**IContextNode**](icontextnode.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT ContextNodeDeleting(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeToBeDeleted
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pInkAnalyzer* \[ in\]
</dt> <dd>

Oggetto [**IInkAnalyzer**](iinkanalyzer.md) che elimina l'oggetto [**IContextNode**](icontextnode.md) .

</dd> <dt>

*pContextNodeToBeDeleted* \[ in\]
</dt> <dd>

Oggetto [**IContextNode**](icontextnode.md) da eliminare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Usare questo evento quando l'applicazione mantiene la propria struttura di dati, sincronizzata con quella di [**IInkAnalyzer**](iinkanalyzer.md). Questo evento si verifica durante la fase di riconciliazione dell'analisi dell'input penna o in risposta a un metodo dell'analizzatore di input penna che elimina un [**IContextNode**](icontextnode.md).

Prima che [**IInkAnalyzer**](iinkanalyzer.md) elimini un [**IContextNode**](icontextnode.md), **IInkAnalyzer** rimuove tutti i tratti dal nodo di contesto e rimuove tutti i collegamenti ad altri nodi di contesto. Prima di rimuovere il nodo di contesto, **IInkAnalyzer** può generare gli eventi seguenti.

-   Evento [**\_ IAnalysisProxyEvents:: StrokeReparented**](-ianalysisproxyevents-strokereparented.md) quando sposta un tratto da [**IContextNode**](icontextnode.md).
-   Evento [**\_ IAnalysisProxyEvents:: l'ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md) prima di rimuovere un [**IContextLink**](icontextlink.md) da [**IContextNode**](icontextnode.md).
-   Evento **\_ IAnalysisProxyEvents:: l'ContextNodeDeleting** prima di rimuovere un nodo di contesto padre che non contiene più nodi figlio.

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

 

 





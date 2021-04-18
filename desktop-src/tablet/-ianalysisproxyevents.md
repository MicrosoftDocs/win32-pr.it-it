---
description: Specifica gli eventi associati ai passaggi del proxy di dati di un oggetto IInkAnalyzer.
ms.assetid: 57fee525-02e2-4721-b6e5-28112d53db2a
title: Interfaccia _IAnalysisProxyEvents (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4b83019cafb6053b9f803c815289d9f9f64d32a5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320946"
---
# <a name="_ianalysisproxyevents-interface"></a>\_Interfaccia IAnalysisProxyEvents

Specifica gli eventi associati ai passaggi del proxy di dati di un oggetto [**IInkAnalyzer**](iinkanalyzer.md) .

-   [Eventi](/windows)

### <a name="events"></a>Eventi

L'interfaccia **\_ IAnalysisProxyEvents** presenta questi eventi.



| Event                                                                                      | Descrizione                                                                                                                                                                               |
|:-------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md)                     | Si verifica dopo che [**IInkAnalyzer**](iinkanalyzer.md) crea un oggetto [**IContextNode**](icontextnode.md) .<br/>                                                                  |
| [**L'ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md)                   | Si verifica prima che [**IInkAnalyzer**](iinkanalyzer.md) elimini un oggetto [**IContextNode**](icontextnode.md) .<br/>                                                                 |
| [**ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md)               | Si verifica prima che [**IInkAnalyzer**](iinkanalyzer.md) aggiunga un oggetto [**IContextLink**](icontextlink.md) tra due oggetti [**IContextNode**](icontextnode.md) .<br/>           |
| [**L'ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md)           | Si verifica prima che [**IInkAnalyzer**](iinkanalyzer.md) elimini un oggetto [**IContextLink**](icontextlink.md) tra due oggetti [**IContextNode**](icontextnode.md) .<br/>         |
| [**ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md)   | Si verifica prima che [**IInkAnalyzer**](iinkanalyzer.md) sposti un oggetto [**IContextNode**](icontextnode.md) in una nuova posizione all'interno della relativa raccolta di nodi padre.<br/> |
| [**ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) | Si verifica dopo che [**IInkAnalyzer**](iinkanalyzer.md) aggiorna una o più proprietà di un oggetto [**IContextNode**](icontextnode.md) .<br/>                                        |
| [**L'ContextNodeReparenting**](-ianalysisproxyevents-contextnodereparenting.md)             | Si verifica prima che [**IInkAnalyzer**](iinkanalyzer.md) sposti un oggetto [**IContextNode**](icontextnode.md) modificando il relativo nodo padre.<br/>                                       |
| [**InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md)         | Si verifica prima che i [**IInkAnalyzer**](iinkanalyzer.md) riconciliano i risultati dell'analisi in modo che un'applicazione possa sincronizzare i dati con **IInkAnalyzer**.<br/>                      |
| [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md)                   | Si verifica prima che [**IInkAnalyzer**](iinkanalyzer.md) esegua l'analisi all'interno dell'area di un oggetto [**IContextNode**](icontextnode.md) parzialmente popolato.<br/>               |
| [**StrokeReparented**](-ianalysisproxyevents-strokereparented.md)                         | Si verifica quando [**IInkAnalyzer**](iinkanalyzer.md) sposta un tratto da un oggetto [**IContextNode**](icontextnode.md) a un altro.<br/>                                           |



 

## <a name="remarks"></a>Commenti

Usare questi eventi quando l'applicazione mantiene la propria struttura di dati, sincronizzata con quella di [**IInkAnalyzer**](iinkanalyzer.md). Per altre informazioni sulla sincronizzazione dei dati dell'applicazione con **IInkAnalyzer**, vedere [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).

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

[**Metodo IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[\_IAnalysisEvents](-ianalysisevents.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 


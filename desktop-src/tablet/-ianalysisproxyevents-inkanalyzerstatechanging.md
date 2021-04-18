---
description: Si verifica prima che i IInkAnalyzer riconciliano i risultati dell'analisi in modo che un'applicazione possa sincronizzare i dati con IInkAnalyzer.
ms.assetid: 9daa8723-5234-40d9-ac41-6dcca988a8b4
title: 'Evento _IAnalysisProxyEvents:: InkAnalyzerStateChanging (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.InkAnalyzerStateChanging
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 92535c34b5d107fb1e435e9abe229df46204f236
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320903"
---
# <a name="_ianalysisproxyeventsinkanalyzerstatechanging-event"></a>\_Evento IAnalysisProxyEvents:: InkAnalyzerStateChanging

Si verifica prima che i [**IInkAnalyzer**](iinkanalyzer.md) riconciliano i risultati dell'analisi in modo che un'applicazione possa sincronizzare i dati con **IInkAnalyzer**.

## <a name="syntax"></a>Sintassi


```C++
HRESULT InkAnalyzerStateChanging(
  [in] IInkAnalyzer *pInkAnalyzer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pInkAnalyzer* \[ in\]
</dt> <dd>

[**IInkAnalyzer**](iinkanalyzer.md) che sta per risolvere i risultati dell'analisi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Usare questo evento quando l'applicazione mantiene la propria struttura di dati, sincronizzata con quella di [**IInkAnalyzer**](iinkanalyzer.md). Quando **IInkAnalyzer** genera questo evento, l'applicazione deve popolare i sottonodi del nodo radice dell'analizzatore di input penna (vedere il metodo [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md) e [**IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md)).

[**IInkAnalyzer**](iinkanalyzer.md) genera questo evento dopo che ha generato l'evento [**\_ IAnalysisEvents:: ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) . Genera questo evento solo durante l'esecuzione dell'analisi in background.

Bloccare la struttura dei dati quando [**IInkAnalyzer**](iinkanalyzer.md) genera l'evento **\_ IAnalysisProxyEvents:: InkAnalyzerStateChanging** . Le modifiche apportate alla struttura dei dati durante questa fase dell'analisi possono causare errori nell'analisi dell'input penna e nella sincronizzazione. Sbloccare la struttura dei dati quando **IInkAnalyzer** genera l'evento [**\_ IAnalysisEvents:: IntermediateResults ()**](-ianalysisevents-intermediateresults.md) o [**\_ IAnalysisEvents:: results**](-ianalysisevents-results.md) .

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

 

 





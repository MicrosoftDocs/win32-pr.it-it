---
description: Si verifica prima che IInkAnalyzer riconcilii i risultati dell'analisi in modo che un'applicazione possa sincronizzare i dati con IInkAnalyzer.
ms.assetid: 9daa8723-5234-40d9-ac41-6dcca988a8b4
title: _IAnalysisProxyEvents::InkAnalyzerStateChanging (IACom.h)
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
ms.openlocfilehash: d4e32685e25e4c942b3c723df2152b1064bed59599fda54fcac00e22aab04206
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119884081"
---
# <a name="_ianalysisproxyeventsinkanalyzerstatechanging-event"></a>\_Evento IAnalysisProxyEvents::InkAnalyzerStateChanging

Si verifica prima che [**IInkAnalyzer**](iinkanalyzer.md) riconcilii i risultati dell'analisi in modo che un'applicazione possa sincronizzare i dati con **IInkAnalyzer.**

## <a name="syntax"></a>Sintassi


```C++
HRESULT InkAnalyzerStateChanging(
  [in] IInkAnalyzer *pInkAnalyzer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pInkAnalyzer* \[ Pollici\]
</dt> <dd>

[**IInkAnalyzer**](iinkanalyzer.md) che sta per riconciliare i risultati dell'analisi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Usare questo evento quando l'applicazione mantiene la propria struttura di dati, sincronizzata con quella di [**IInkAnalyzer.**](iinkanalyzer.md) Quando **IInkAnalyzer** genera questo evento, l'applicazione deve popolare i sottonodi del nodo radice dell'analizzatore input penna (vedere [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) e [**IInkAnalyzer::GetRootNode Method).**](iinkanalyzer-getrootnode.md)

[**IInkAnalyzer**](iinkanalyzer.md) genera questo evento dopo la generazione dell'evento [**\_ IAnalysisEvents::ReadyToReconcile.**](-ianalysisevents-readytoreconcile.md) Genera questo evento solo durante l'esecuzione dell'analisi in background.

Bloccare la struttura dei dati [**quando IInkAnalyzer**](iinkanalyzer.md) genera l'evento **\_ IAnalysisProxyEvents::InkAnalyzerStateChanging.** Le modifiche alla struttura dei dati durante questa fase di analisi possono causare errori nell'analisi e nella sincronizzazione dell'input penna. Sbloccare la struttura dei dati quando **IInkAnalyzer** genera l'evento [**\_ IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) o [**\_ IAnalysisEvents::Results.**](-ianalysisevents-results.md)

Per altre informazioni sulla sincronizzazione dei dati dell'applicazione con [**IInkAnalyzer,**](iinkanalyzer.md)vedere [Proxy dati con l'analisi dell'input penna](data-proxy-with-ink-analysis.md).

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

 

 





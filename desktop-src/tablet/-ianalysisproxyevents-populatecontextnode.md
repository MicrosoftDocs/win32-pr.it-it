---
description: Si verifica prima che IInkAnalyzer esegua l'analisi all'interno dell'area di un oggetto IContextNode parzialmente popolato.
ms.assetid: c24e8adb-672f-444a-bccb-1e9e55bea432
title: _IAnalysisProxyEvents::P opulateContextNode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.PopulateContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ff6378f7ecf3ff597f4c02740e30544ff65651d0a7fcd6d6d490ebabf2161ef7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967930"
---
# <a name="_ianalysisproxyeventspopulatecontextnode-event"></a>\_Evento IAnalysisProxyEvents::P opulateContextNode

Si verifica prima che [**IInkAnalyzer**](iinkanalyzer.md) esegua l'analisi all'interno dell'area di un [**oggetto IContextNode**](icontextnode.md) parzialmente popolato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT PopulateContextNode(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeToPopulate
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pInkAnalyzer* \[ Pollici\]
</dt> <dd>

Oggetto [**IInkAnalyzer**](iinkanalyzer.md) che sta per eseguire l'analisi.

</dd> <dt>

*pContextNodeToPopulate* \[ Pollici\]
</dt> <dd>

Oggetto [**IContextNode**](icontextnode.md) parzialmente popolato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Usare questo evento quando l'applicazione mantiene la propria struttura di dati, sincronizzata con quella di [**IInkAnalyzer.**](iinkanalyzer.md) Quando **IInkAnalyzer** genera questo evento, l'applicazione deve popolare *pContextNodeToPopulate*. Durante la fase di analisi, **IInkAnalyzer** genera questo evento per ottenere informazioni sulle aree in cui sta analizzando l'input penna.

Se il documento contiene collegamenti per *pContextNodeToPopulate,* l'applicazione deve creare e aggiungere questi collegamenti. Questo processo richiede che i nodi di origine e di destinazione, inclusi i relativi predecessori, siano completamente popolati prima che il gestore eventi per questo evento venga chiuso (vedere [**IContextLink::GetSourceNode**](icontextlink-getsourcenode.md) e [**IContextLink::GetDestinationNode).**](icontextlink-getdestinationnode.md)

Per altre informazioni sulla sincronizzazione dei dati dell'applicazione con [**IInkAnalyzer,**](iinkanalyzer.md)vedere [Proxy dati con](data-proxy-with-ink-analysis.md)Analisi input penna .

Durante l'analisi in background, [**IInkAnalyzer**](iinkanalyzer.md) genera questo evento dopo la generazione dell'evento [**\_ IAnalysisEvents::ReadyToReconcile.**](-ianalysisevents-readytoreconcile.md)

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

 

 





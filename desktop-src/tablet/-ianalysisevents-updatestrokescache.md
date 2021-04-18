---
description: Si verifica prima che IInkAnalyzer acceda ai dati del tratto.
ms.assetid: fed46476-4531-4516-9375-d7b654efb3be
title: 'Evento _IAnalysisEvents:: UpdateStrokesCache (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.UpdateStrokesCache
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5d16011d8c5fe571d228b632fecb7a973bafcbf5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320915"
---
# <a name="_ianalysiseventsupdatestrokescache-event"></a>\_Evento IAnalysisEvents:: UpdateStrokesCache

Si verifica prima che [**IInkAnalyzer**](iinkanalyzer.md) acceda ai dati del tratto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT UpdateStrokesCache(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ulStrokeIdsCount* \[ in\]
</dt> <dd>

Il numero di identificatori di tratto in *plStrokeIds*.

</dd> <dt>

*plStrokeIds* \[ in\]
</dt> <dd>

Identificatori dei tratti i cui dati del pacchetto sono stati cancellati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

[**IInkAnalyzer**](iinkanalyzer.md) genera questo evento durante l'analisi dell'input penna quando accede a uno o più tratti per i quali sono stati cancellati i dati del pacchetto. Per aggiornare i dati del pacchetto del tratto, usare il metodo [**IInkAnalyzer:: UpdateStrokesData Method**](iinkanalyzer-updatestrokesdata.md) .

[**IInkAnalyzer**](iinkanalyzer.md) non genera questo evento quando si accede a un nodo foglia input penna parzialmente popolato quando il percorso del nodo non è stato impostato da **IInkAnalyzer**.

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

[**\_IAnalysisEvents**](-ianalysisevents.md)
</dt> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: UpdateStrokesData**](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[**IContextNode:: CreatePartiallyPopulatedSubNode**](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





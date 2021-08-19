---
description: Si verifica prima dell'accesso di IInkAnalyzer ai dati del tratto.
ms.assetid: fed46476-4531-4516-9375-d7b654efb3be
title: evento _IAnalysisEvents::UpdateStrokesCache (IACom.h)
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
ms.openlocfilehash: 9a5854c8061a12dc558a2ca20ebd893880f899b2113065abd9b8122c53812aa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118047373"
---
# <a name="_ianalysiseventsupdatestrokescache-event"></a>\_Evento IAnalysisEvents::UpdateStrokesCache

Si verifica prima [**dell'accesso di IInkAnalyzer**](iinkanalyzer.md) ai dati del tratto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT UpdateStrokesCache(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ulStrokeIdsCount* \[ Pollici\]
</dt> <dd>

Numero di identificatori di tratto in *plStrokeIds.*

</dd> <dt>

*plStrokeIds* \[ Pollici\]
</dt> <dd>

Identificatori dei tratti i cui dati del pacchetto sono stati cancellati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Commenti

[**L'IInkAnalyzer**](iinkanalyzer.md) genera questo evento durante l'analisi input penna quando accede a uno o più tratti per cui sono stati cancellati i dati del pacchetto. Per aggiornare i dati dei pacchetti di tratti, usare il metodo [**IInkAnalyzer::UpdateStrokesData.**](iinkanalyzer-updatestrokesdata.md)

[**IInkAnalyzer**](iinkanalyzer.md) non genera questo evento quando accede a un nodo foglia dell'input penna parzialmente popolato quando la posizione del nodo non è stata impostata da **IInkAnalyzer.**

Per altre informazioni sulla sincronizzazione dei dati dell'applicazione con [**IInkAnalyzer,**](iinkanalyzer.md)vedere [Proxy dati con analisi input penna.](data-proxy-with-ink-analysis.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_IAnalysisEvents**](-ianalysisevents.md)
</dt> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Metodo IInkAnalyzer::Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Metodo IInkAnalyzer::BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**Metodo IInkAnalyzer::UpdateStrokesData**](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[**IContextNode::CreatePartiallyPopulatedSubNode**](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





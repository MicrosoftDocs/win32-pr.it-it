---
description: Si verifica quando IInkAnalyzer sposta un tratto da un oggetto IContextNode a un altro.
ms.assetid: a90214af-c3ea-4e2a-94b4-bb5746a2b476
title: evento _IAnalysisProxyEvents::StrokeReparented (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.StrokeReparented
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1e9262eb7b4ce2b323669eeb084abb597b5fe00488df90fc5fde0b2876b7e953
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967870"
---
# <a name="_ianalysisproxyeventsstrokereparented-event"></a>\_Evento IAnalysisProxyEvents::StrokeReparented

Si verifica quando [**IInkAnalyzer**](iinkanalyzer.md) sposta un tratto da un [**oggetto IContextNode**](icontextnode.md) a un altro.

## <a name="syntax"></a>Sintassi


```C++
HRESULT StrokeReparented(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] LONG         lStrokeIdToMove,
  [in] IContextNode *pSourceContextNode,
  [in] IContextNode *pDestinationContextNode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pInkAnalyzer* \[ Pollici\]
</dt> <dd>

Oggetto [**IInkAnalyzer**](iinkanalyzer.md) che sposta il tratto.

</dd> <dt>

*lStrokeIdToMove* \[ Pollici\]
</dt> <dd>

Identificatore del tratto da spostare.

</dd> <dt>

*pSourceContextNode* \[ Pollici\]
</dt> <dd>

Oggetto [**IContextNode**](icontextnode.md) da cui viene spostato il tratto.

</dd> <dt>

*pDestinationContextNode* \[ Pollici\]
</dt> <dd>

Oggetto [**IContextNode**](icontextnode.md) in cui viene spostato il tratto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Commenti

Usare questo evento quando l'applicazione mantiene la propria struttura di dati, sincronizzata con quella di [**IInkAnalyzer.**](iinkanalyzer.md) Questo evento si verifica durante la fase di riconciliazione dell'analisi input penna o in risposta a un metodo **IInkAnalyzer** che sposta i dati del tratto da [**un IContextNode**](icontextnode.md) a un altro.

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

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





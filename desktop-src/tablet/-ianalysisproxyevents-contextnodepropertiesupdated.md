---
description: Si verifica dopo che IInkAnalyzer aggiorna una o più proprietà di un oggetto IContextNode.
ms.assetid: f626c263-31a4-45ee-ae04-3251eac0d652
title: 'Evento _IAnalysisProxyEvents:: ContextNodePropertiesUpdated (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodePropertiesUpdated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fa035b89c531f3b2d230ab849ba20b945dd2d25c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320879"
---
# <a name="_ianalysisproxyeventscontextnodepropertiesupdated-event"></a>\_Evento IAnalysisProxyEvents:: ContextNodePropertiesUpdated

Si verifica dopo che [**IInkAnalyzer**](iinkanalyzer.md) aggiorna una o più proprietà di un oggetto [**IContextNode**](icontextnode.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT ContextNodePropertiesUpdated(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeUpdated
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pInkAnalyzer* \[ in\]
</dt> <dd>

Oggetto [**IInkAnalyzer**](iinkanalyzer.md) che aggiorna le proprietà.

</dd> <dt>

*pContextNodeUpdated* \[ in\]
</dt> <dd>

Oggetto [**IContextNode**](icontextnode.md) le cui proprietà sono aggiornate.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Usare questo evento quando l'applicazione mantiene la propria struttura di dati, sincronizzata con quella di [**IInkAnalyzer**](iinkanalyzer.md). Questo evento si verifica durante la fase di riconciliazione dell'analisi dell'input penna o in risposta a un metodo dell'analizzatore di input penna che modifica le proprietà di un [**IContextNode**](icontextnode.md) (vedere [**IContextNode:: GetPropertyData**](icontextnode-getpropertydata.md)).

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

[Proprietà del nodo di contesto](context-node-properties.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





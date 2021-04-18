---
description: Si verifica prima che IInkAnalyzer sposti un oggetto IContextNode modificando il relativo nodo padre.
ms.assetid: 91261270-aa7c-4f0a-a790-1b2bf322a3ad
title: "Evento _IAnalysisProxyEvents:: l'ContextNodeReparenting (IACom. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeReparenting
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 084f971edc5adce0845fc7e1c3ea6ea59a066bb0
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320950"
---
# <a name="_ianalysisproxyeventscontextnodereparenting-event"></a>\_Evento IAnalysisProxyEvents:: l'ContextNodeReparenting

Si verifica prima che [**IInkAnalyzer**](iinkanalyzer.md) sposti un oggetto [**IContextNode**](icontextnode.md) modificando il relativo nodo padre.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ContextNodeReparenting(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pNewParentContextNode,
  [in] IContextNode *pContextNodeToBeReparented
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pInkAnalyzer* \[ in\]
</dt> <dd>

Oggetto [**IInkAnalyzer**](iinkanalyzer.md) che trasferisce l'oggetto [**IContextNode**](icontextnode.md) .

</dd> <dt>

*pNewParentContextNode* \[ in\]
</dt> <dd>

Nuovo oggetto [**IContextNode**](icontextnode.md) padre.

</dd> <dt>

*pContextNodeToBeReparented* \[ in\]
</dt> <dd>

Oggetto [**IContextNode**](icontextnode.md) da spostare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Usare questo evento quando l'applicazione mantiene la propria struttura di dati, sincronizzata con quella di [**IInkAnalyzer**](iinkanalyzer.md). Questo evento si verifica durante la fase di riconciliazione dell'analisi dell'input penna o in risposta a un metodo che sposta un [**IContextNode**](icontextnode.md) da una raccolta di sottonodi a un'altra (vedere [**IContextNode:: GetParentNode**](icontextnode-getparentnode.md) e [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md)).

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

[**IContextNode:: GetParentNode**](icontextnode-getparentnode.md)
</dt> <dt>

[**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





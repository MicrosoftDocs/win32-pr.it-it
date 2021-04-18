---
description: Si verifica prima che IInkAnalyzer sposti un oggetto IContextNode in una nuova posizione all'interno della relativa raccolta di nodi padre.
ms.assetid: c7a5956e-ffc4-4205-9de3-e8b7d672156d
title: 'Evento _IAnalysisProxyEvents:: ContextNodeMovingToPosition (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeMovingToPosition
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 462e7428fb43fd998d769dd152e19f8109b04158
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320904"
---
# <a name="_ianalysisproxyeventscontextnodemovingtoposition-event"></a>\_Evento IAnalysisProxyEvents:: ContextNodeMovingToPosition

Si verifica prima che [**IInkAnalyzer**](iinkanalyzer.md) sposti un oggetto [**IContextNode**](icontextnode.md) in una nuova posizione all'interno della relativa raccolta di nodi padre.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ContextNodeMovingToPosition(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pISubNodeToMove,
  [in] IContextNode *pParentContextNode,
  [in] ULONG        ulNewIndex
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pInkAnalyzer* \[ in\]
</dt> <dd>

Oggetto [**IInkAnalyzer**](iinkanalyzer.md) che trasferisce l'oggetto [**IContextNode**](icontextnode.md) .

</dd> <dt>

*pISubNodeToMove* \[ in\]
</dt> <dd>

Oggetto [**IContextNode**](icontextnode.md) da spostare.

</dd> <dt>

*pParentContextNode* \[ in\]
</dt> <dd>

Oggetto [**IContextNode**](icontextnode.md) padre di *pISubNodeToMove*.

</dd> <dt>

*ulNewIndex* \[ in\]
</dt> <dd>

Nuova posizione di *pISubNodeToMove* nella raccolta di sottonodi del nodo padre.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Usare questo evento quando l'applicazione mantiene la propria struttura di dati, sincronizzata con quella di [**IInkAnalyzer**](iinkanalyzer.md). Questo evento si verifica durante la fase di riconciliazione dell'analisi dell'input penna o in risposta a un metodo dell'analizzatore di input penna che sposta un [**IContextNode**](icontextnode.md) all'interno della relativa raccolta di nodi padre (vedere [**IContextNode:: GetParentNode**](icontextnode-getparentnode.md) e [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md)).

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

[**IContextNode:: GetParentNode**](icontextnode-getparentnode.md)
</dt> <dt>

[**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





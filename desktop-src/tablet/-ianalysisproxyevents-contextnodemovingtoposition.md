---
description: Si verifica prima che IInkAnalyzer smuova un oggetto IContextNode in una nuova posizione all'interno della raccolta di sottonodi del nodo padre.
ms.assetid: c7a5956e-ffc4-4205-9de3-e8b7d672156d
title: _IAnalysisProxyEvents::ContextNodeMovingToPosition (IACom.h)
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
ms.openlocfilehash: 4cd814e45692d90c77bad8c46fea5dfd8534bd769a07a9d0bc1648ecafc7b2f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857150"
---
# <a name="_ianalysisproxyeventscontextnodemovingtoposition-event"></a>\_Evento IAnalysisProxyEvents::ContextNodeMovingToPosition

Si verifica prima [**che IInkAnalyzer**](iinkanalyzer.md) smuova un [**oggetto IContextNode**](icontextnode.md) in una nuova posizione all'interno della raccolta di sottonodi del nodo padre.

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

*pInkAnalyzer* \[ Pollici\]
</dt> <dd>

Oggetto [**IInkAnalyzer**](iinkanalyzer.md) che sposta [**l'oggetto IContextNode.**](icontextnode.md)

</dd> <dt>

*pISubNodeToMove* \[ Pollici\]
</dt> <dd>

Oggetto [**IContextNode**](icontextnode.md) da spostare.

</dd> <dt>

*pParentContextNode* \[ Pollici\]
</dt> <dd>

Oggetto [**IContextNode padre**](icontextnode.md) di *pISubNodeToMove.*

</dd> <dt>

*ulNewIndex* \[ Pollici\]
</dt> <dd>

Nuova posizione di *pISubNodeToMove* nella raccolta di sottonodi del nodo padre.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Usare questo evento quando l'applicazione mantiene la propria struttura di dati, sincronizzata con quella di [**IInkAnalyzer.**](iinkanalyzer.md) Questo evento si verifica durante la fase di riconciliazione dell'analisi dell'input penna o in risposta a un metodo dell'analizzatore input penna che sposta un [**oggetto IContextNode**](icontextnode.md) all'interno della raccolta di sottonodi del nodo padre (vedere [**IContextNode::GetParentNode**](icontextnode-getparentnode.md) e [**IContextNode::GetSubNodes).**](icontextnode-getsubnodes.md)

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

[**IContextNode::GetParentNode**](icontextnode-getparentnode.md)
</dt> <dt>

[**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





---
description: Si verifica prima che IInkAnalyzer smuova un oggetto IContextNode modificandone il nodo padre.
ms.assetid: 91261270-aa7c-4f0a-a790-1b2bf322a3ad
title: _IAnalysisProxyEvents::ContextNodeReparenting (IACom.h)
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
ms.openlocfilehash: eafb37fd4083f0ecf7c68eaf45fc3339a730e818864f4be15eca4b94d4bd5b7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857110"
---
# <a name="_ianalysisproxyeventscontextnodereparenting-event"></a>\_Evento IAnalysisProxyEvents::ContextNodeReparenting

Si verifica prima [**che IInkAnalyzer**](iinkanalyzer.md) smuova un [**oggetto IContextNode**](icontextnode.md) modificandone il nodo padre.

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

*pInkAnalyzer* \[ Pollici\]
</dt> <dd>

Oggetto [**IInkAnalyzer**](iinkanalyzer.md) che sposta [**l'oggetto IContextNode.**](icontextnode.md)

</dd> <dt>

*pNewParentContextNode* \[ Pollici\]
</dt> <dd>

Nuovo oggetto [**IContextNode**](icontextnode.md) padre.

</dd> <dt>

*pContextNodeToBeReparented* \[ Pollici\]
</dt> <dd>

Oggetto [**IContextNode**](icontextnode.md) da spostare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Usare questo evento quando l'applicazione mantiene la propria struttura di dati, sincronizzata con quella di [**IInkAnalyzer.**](iinkanalyzer.md) Questo evento si verifica durante la fase di riconciliazione dell'analisi input penna o in risposta a un metodo che sposta [**un oggetto IContextNode**](icontextnode.md) da una raccolta di sottonodi a un'altra (vedere [**IContextNode::GetParentNode**](icontextnode-getparentnode.md) e [**IContextNode::GetSubNodes).**](icontextnode-getsubnodes.md)

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

[**IContextNode::GetParentNode**](icontextnode-getparentnode.md)
</dt> <dt>

[**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)
</dt> <dt>

[**Metodo IInkAnalyzer::Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Metodo IInkAnalyzer::BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





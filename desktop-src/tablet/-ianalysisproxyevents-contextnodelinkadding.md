---
description: Si verifica prima dell'aggiunta di un oggetto IContextLink da parte dell'analizzatore input penna tra due oggetti IContextNode.
ms.assetid: ec56cb8e-5154-45ee-911d-e2a240d19dc3
title: _IAnalysisProxyEvents::ContextNodeLinkAdding (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeLinkAdding
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1d100d4ecb4caa6fb7230afd3d4ae6572466ae86855ac9bd28155b6b181cdd5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452156"
---
# <a name="_ianalysisproxyeventscontextnodelinkadding-event"></a>\_Evento IAnalysisProxyEvents::ContextNodeLinkAdding

Si verifica prima dell'aggiunta di un [**oggetto IContextLink**](icontextlink.md) da parte dell'analizzatore input penna tra due [**oggetti IContextNode.**](icontextnode.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT ContextNodeLinkAdding(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextLink *pContextLinkToBeAdded
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pInkAnalyzer* \[ Pollici\]
</dt> <dd>

Oggetto [**IInkAnalyzer che aggiunge**](iinkanalyzer.md) il collegamento.

</dd> <dt>

*pContextLinkToBeAdded* \[ Pollici\]
</dt> <dd>

Oggetto [**IContextLink**](icontextlink.md) da aggiungere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Usare questo evento quando l'applicazione mantiene la propria struttura di dati, sincronizzata con quella di [**IInkAnalyzer.**](iinkanalyzer.md) Questo evento si verifica durante la fase di riconciliazione dell'analisi dell'input penna o in risposta a un metodo dell'analizzatore input penna che aggiunge un nuovo [**IContextLink**](icontextlink.md) a [**un oggetto IContextNode**](icontextnode.md).

Per altre informazioni sulla sincronizzazione dei dati dell'applicazione con [**IInkAnalyzer,**](iinkanalyzer.md)vedere [Proxy dati con](data-proxy-with-ink-analysis.md)Analisi input penna .

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

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**Metodo IInkAnalyzer::Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Metodo IInkAnalyzer::BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





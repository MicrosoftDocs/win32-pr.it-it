---
description: Si verifica prima che IInkAnalyzer elimini un oggetto IContextLink tra due oggetti IContextNode.
ms.assetid: bc9716b8-8793-4886-aff4-d880024129a6
title: evento _IAnalysisProxyEvents::ContextNodeLinkDeleting (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeLinkDeleting
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2bf45b8ae900d574bc50151e1bd17f0a124211272d4a83ccb43216ebbf82e2f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452086"
---
# <a name="_ianalysisproxyeventscontextnodelinkdeleting-event"></a>\_Evento IAnalysisProxyEvents::ContextNodeLinkDeleting

Si verifica prima [**che IInkAnalyzer**](iinkanalyzer.md) elimini un [**oggetto IContextLink**](icontextlink.md) tra due [**oggetti IContextNode.**](icontextnode.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT ContextNodeLinkDeleting(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextLink *pContextLinkToBeDeleted
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pInkAnalyzer* \[ Pollici\]
</dt> <dd>

Eliminazione del collegamento da parte di [**IInkAnalyzer.**](iinkanalyzer.md)

</dd> <dt>

*pContextLinkToBeDeleted* \[ Pollici\]
</dt> <dd>

Oggetto [**IContextLink**](icontextlink.md) da eliminare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Commenti

Usare questo evento quando l'applicazione mantiene la propria struttura di dati, sincronizzata con quella di [**IInkAnalyzer.**](iinkanalyzer.md) Questo evento si verifica durante la fase di riconciliazione dell'analisi input penna o in risposta a un metodo **IInkAnalyzer** che rimuove un [**oggetto IContextLink**](icontextlink.md) da [**un oggetto IContextNode.**](icontextnode.md)

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

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**Metodo IInkAnalyzer::Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Metodo IInkAnalyzer::BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





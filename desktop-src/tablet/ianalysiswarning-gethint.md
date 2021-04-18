---
description: Recupera l'hint di analisi che ha generato l'avviso.
ms.assetid: 715aa4b2-6c45-414b-96f2-44c73a073213
title: 'Metodo IAnalysisWarning:: GetHint (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetHint
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2c38a22b799eb6836a85a42748f60207ee7e997e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307455"
---
# <a name="ianalysiswarninggethint-method"></a>Metodo IAnalysisWarning:: GetHint

Recupera l'hint di analisi che ha generato l'avviso.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetHint(
  [out] IContextNode **pAnalysisHint
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pAnalysisHint* \[ out\]
</dt> <dd>

Nodo di contesto dell'hint di analisi che ha causato questo avviso o **null** se un hint di analisi non ha causato questo avviso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su \* *pAnalysisHint* quando non è più necessario usare il nodo di contesto dell'hint di analisi.

 

Un esempio di hint di analisi che genera un [**IAnalysisWarning**](ianalysiswarning.md) è un hint di analisi che contiene un controllo del controllo ortografico digitato in modo errato. In questo caso, l'analisi dell'input penna restituisce un [**IAnalysisStatus**](ianalysisstatus.md) contenente un **IAnalysisWarning** che fa riferimento al nodo di contesto dell'hint di analisi con il controllo ortografico errato. Inoltre, in questo caso, il metodo [**IAnalysisWarning:: GetWarningCode**](ianalysiswarning-getwarningcode.md) dell'avviso di analisi restituisce un valore [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) di **AnalysisWarningCode \_ FactoidNotSupported**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IAnalysisWarning**](ianalysiswarning.md)
</dt> <dt>

[**IAnalysisStatus**](ianalysisstatus.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 


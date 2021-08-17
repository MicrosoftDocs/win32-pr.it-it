---
description: Modifica i flag che controllano il modo in cui IInkAnalyzer esegue l'analisi dell'input penna.
ms.assetid: cb82edd0-1f15-4313-a286-1fcd715ac6df
title: Metodo IInkAnalyzer::SetAnalysisModes (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetAnalysisModes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c7edd167cd40b80a01fd2f23243c931fe6a15795da08d7735b6e2433c462ee01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091503"
---
# <a name="iinkanalyzersetanalysismodes-method"></a>Metodo IInkAnalyzer::SetAnalysisModes

Modifica i flag che controllano il modo in cui [**IInkAnalyzer esegue**](iinkanalyzer.md) l'analisi dell'input penna.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetAnalysisModes(
  [in] AnalysisModes analysisMode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*analysisMode* \[ Pollici\]
</dt> <dd>

Combinazione bit per bit dei [**valori di enumerazione AnalysisModes.**](analysismodes.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Analysismodes**](analysismodes.md)
</dt> <dt>

[**Metodo IInkAnalyzer::Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Metodo IInkAnalyzer::BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**Metodo IInkAnalyzer::GetAnalysisModes**](iinkanalyzer-getanalysismodes.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





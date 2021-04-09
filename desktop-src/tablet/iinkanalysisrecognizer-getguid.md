---
description: Recupera l'identificatore univoco globale (GUID) del riconoscimento.
ms.assetid: 9b98993b-eaf3-4207-9d56-33efeceb75cf
title: 'Metodo IInkAnalysisRecognizer:: GetGuid (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetGuid
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 9a027a405829e6d1237a8ec90dd59fcc8905006d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879354"
---
# <a name="iinkanalysisrecognizergetguid-method"></a>Metodo IInkAnalysisRecognizer:: GetGuid

Recupera l'identificatore univoco globale (GUID) del riconoscimento.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetGuid(
  [out] GUID *pId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PID* \[ out\]
</dt> <dd>

GUID che identifica questo [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





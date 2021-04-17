---
description: Ottiene il valore stringa riconosciuto dell'oggetto IAnalysisAlternate.
ms.assetid: cdf41824-77a4-4c71-8712-f380a6cbf4c5
title: 'Metodo IAnalysisAlternate:: GetRecognizedString (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetRecognizedString
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5489773b29ade35d4b7297065c1104bfecefa117
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526569"
---
# <a name="ianalysisalternategetrecognizedstring-method"></a>Metodo IAnalysisAlternate:: GetRecognizedString

Ottiene il valore stringa riconosciuto dell'oggetto [**IAnalysisAlternate**](ianalysisalternate.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetRecognizedString(
  [out] BSTR *pbstrRecognizedString
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbstrRecognizedString* \[ out\]
</dt> <dd>

Puntatore a **BSTR** impostato sul valore stringa riconosciuto.

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

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: GetRecognizedString**](iinkanalyzer-getrecognizedstring.md)
</dt> </dl>

 

 





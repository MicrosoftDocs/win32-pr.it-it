---
description: Ottiene il valore stringa riconosciuto dell'oggetto IAnalysisAlternate.
ms.assetid: cdf41824-77a4-4c71-8712-f380a6cbf4c5
title: Metodo IAnalysisAlternate::GetRecognizedString (IACom.h)
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
ms.openlocfilehash: 79d0967d2653a68145a9a50c34134d176d78674c5ea5729230035edd65a5e6b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008491"
---
# <a name="ianalysisalternategetrecognizedstring-method"></a>Metodo IAnalysisAlternate::GetRecognizedString

Ottiene il valore stringa riconosciuto [**dell'oggetto IAnalysisAlternate.**](ianalysisalternate.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetRecognizedString(
  [out] BSTR *pbstrRecognizedString
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbstrRecognizedString* \[ Cambio\]
</dt> <dd>

Puntatore a **BSTR** impostato sul valore stringa riconosciuto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**Metodo IInkAnalyzer::GetRecognizedString**](iinkanalyzer-getrecognizedstring.md)
</dt> </dl>

 

 





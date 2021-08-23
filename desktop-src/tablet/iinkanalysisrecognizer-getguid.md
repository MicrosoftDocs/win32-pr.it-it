---
description: Recupera l'identificatore univoco globale (GUID) del riconoscimento.
ms.assetid: 9b98993b-eaf3-4207-9d56-33efeceb75cf
title: Metodo IInkAnalysisRecognizer::GetGuid (IACom.h)
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
ms.openlocfilehash: b5fbf2b07b2a63f2fdb088c38a5e03e4182c4e38528208c039f927b282755344
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119596741"
---
# <a name="iinkanalysisrecognizergetguid-method"></a>Metodo IInkAnalysisRecognizer::GetGuid

Recupera l'identificatore univoco globale (GUID) del riconoscimento.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetGuid(
  [out] GUID *pId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pId* \[ Cambio\]
</dt> <dd>

GUID che identifica [**l'oggetto IInkAnalysisRecognizer.**](iinkanalysisrecognizer.md)

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

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





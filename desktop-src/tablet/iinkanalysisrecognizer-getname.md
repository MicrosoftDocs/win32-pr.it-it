---
description: Recupera il nome del riconoscitore.
ms.assetid: bd97fead-1e80-49dc-ada0-38eb5dc015ae
title: Metodo IInkAnalysisRecognizer::GetName (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetName
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: df86f5526a6b28f8a7f383ddfb49ca999875b8aa08c66e07a9ac95c41acd13cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773621"
---
# <a name="iinkanalysisrecognizergetname-method"></a>Metodo IInkAnalysisRecognizer::GetName

Recupera il nome del riconoscitore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetName(
  [out] BSTR *pbstrName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbstrName* \[ Cambio\]
</dt> <dd>

Nome del sistema di riconoscimento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) su \* *pbstrName* quando non è più necessario usare la stringa.

 

Il nome è localizzato per la lingua indipendente dall'area geografica che il riconoscimento supporta.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

 


---
description: Recupera una matrice di intervalli di caratteri che rappresentano gli intervalli di caratteri Unicode supportati.
ms.assetid: 334cf545-832a-4e8a-8fe6-76a173676be7
title: Metodo IInkAnalysisRecognizer::GetUnicodeRanges (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetUnicodeRanges
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: cf8c0fe75d2eff0cdd8f2f9d3eb5366f6bab4dd4588c854455804ce4196971bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008401"
---
# <a name="iinkanalysisrecognizergetunicoderanges-method"></a>Metodo IInkAnalysisRecognizer::GetUnicodeRanges

Recupera una matrice di intervalli di caratteri che rappresentano gli intervalli di caratteri Unicode supportati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetUnicodeRanges(
  [in, out] ULONG  *pulNumberOfRanges,
  [out]     WCHAR  **ppulLowUnicode,
  [out]     USHORT **ppusUnicodeRangeLength
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pulNumberOfRanges* \[ in, out\]
</dt> <dd>

Numero di intervalli di caratteri a cui punta *ppulLowUnicode.*

</dd> <dt>

*ppulLowUnicode* \[ Cambio\]
</dt> <dd>

Puntatore a una matrice di intervalli di caratteri che rappresentano gli intervalli di caratteri Unicode supportati.

</dd> <dt>

*ppusUnicodeRangeLength* \[ Cambio\]
</dt> <dd>

Puntatore a una matrice di valori che indica la lunghezza di ogni punto della matrice a da *ppulLowUnicode*.

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
</dt> </dl>

 

 





---
description: Recupera una matrice di intervalli di caratteri che rappresenta gli intervalli di caratteri Unicode supportati.
ms.assetid: 334cf545-832a-4e8a-8fe6-76a173676be7
title: 'Metodo IInkAnalysisRecognizer:: GetUnicodeRanges (IACom. h)'
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
ms.openlocfilehash: 939c2d5bf45c5dfbf0f1866cb6d0c7a58c38320f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879350"
---
# <a name="iinkanalysisrecognizergetunicoderanges-method"></a>Metodo IInkAnalysisRecognizer:: GetUnicodeRanges

Recupera una matrice di intervalli di caratteri che rappresenta gli intervalli di caratteri Unicode supportati.

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

*pulNumberOfRanges* \[ in uscita\]
</dt> <dd>

Numero di intervalli di caratteri a cui punta *ppulLowUnicode*.

</dd> <dt>

*ppulLowUnicode* \[ out\]
</dt> <dd>

Puntatore a una matrice di intervalli di caratteri che rappresenta gli intervalli di caratteri Unicode supportati.

</dd> <dt>

*ppusUnicodeRangeLength* \[ out\]
</dt> <dd>

Puntatore a una matrice di valori che indica la lunghezza di ogni matrice puntata da *ppulLowUnicode*.

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
</dt> </dl>

 

 





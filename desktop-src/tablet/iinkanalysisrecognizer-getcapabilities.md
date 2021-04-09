---
description: Recupera le funzionalità del riconoscimento.
ms.assetid: 9014bd9b-54fb-4735-9eb8-56a6188a5fc0
title: 'Metodo IInkAnalysisRecognizer:: GetCapabilities (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetCapabilities
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 07b66ffbed6f3e57edb8a6bfad36959fabbc047c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129478"
---
# <a name="iinkanalysisrecognizergetcapabilities-method"></a>Metodo IInkAnalysisRecognizer:: GetCapabilities

Recupera le funzionalità del riconoscimento.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCapabilities(
  [out] InkAnalysisRecognizerCapabilities *pCapabilities
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCapabilities* \[ out\]
</dt> <dd>

Combinazione bit per bit dei valori [**RecognizerCapabilities**](recognizercapabilities.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Questo valore è costante per ogni [ **IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)

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

[**RecognizerCapabilities**](recognizercapabilities.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





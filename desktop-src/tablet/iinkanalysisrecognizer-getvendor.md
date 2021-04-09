---
description: Recupera il nome del fornitore del IInkAnalysisRecognizer.
ms.assetid: 62ff209e-2a34-4c04-90a0-661d06898298
title: 'Metodo IInkAnalysisRecognizer:: getvendor (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetVendor
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a48bec62ed4a6a9d94d54ea3a1ba4a53eddd4b7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129474"
---
# <a name="iinkanalysisrecognizergetvendor-method"></a>Metodo IInkAnalysisRecognizer:: getvendor

Recupera il nome del fornitore del [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetVendor(
  [out] BSTR *pbstrVendor
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbstrVendor* \[ out\]
</dt> <dd>

Nome del fornitore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) su \* *pbstrVendor* quando non è più necessario usare la stringa.

 

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

 


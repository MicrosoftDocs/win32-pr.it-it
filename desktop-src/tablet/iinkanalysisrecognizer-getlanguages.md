---
description: Recupera gli identificatori per le impostazioni locali supportate da questo IInkAnalysisRecognizer.
ms.assetid: 14c91ad0-f49e-43e7-848c-abc96b0dffa8
title: 'Metodo IInkAnalysisRecognizer:: GetLanguages (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetLanguages
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1e2b9792957b2de02daf45f8b662cfcb1174be72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879353"
---
# <a name="iinkanalysisrecognizergetlanguages-method"></a>Metodo IInkAnalysisRecognizer:: GetLanguages

Recupera gli identificatori per le impostazioni locali supportate da questo [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetLanguages(
  [in, out] ULONG *pulLanguagesCount,
  [out]     ULONG **ppulLanguages
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pulLanguagesCount* \[ in uscita\]
</dt> <dd>

Il numero di identificatori in *ppulLanguages*.

</dd> <dt>

*ppulLanguages* \[ out\]
</dt> <dd>

Puntatore agli identificatori per le impostazioni locali supportate da questo [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, usare [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) per rilasciare la memoria da \* *ppulLanguages* quando le informazioni non sono più necessarie.

 

Questo metodo restituisce una matrice vuota per i riconoscitori di oggetto e di movimento.

Per altre informazioni sugli identificatori di lingua, vedere [costanti e stringhe degli identificatori di lingua](/windows/desktop/Intl/language-identifier-constants-and-strings).

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

 


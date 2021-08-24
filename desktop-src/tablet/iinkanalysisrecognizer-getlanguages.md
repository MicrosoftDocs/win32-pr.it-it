---
description: Recupera gli identificatori per le impostazioni locali supportate da IInkAnalysisRecognizer.
ms.assetid: 14c91ad0-f49e-43e7-848c-abc96b0dffa8
title: Metodo IInkAnalysisRecognizer::GetLanguages (IACom.h)
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
ms.openlocfilehash: 8a94b85dfe9a6b5dbbd755ff1e0a4cf2d68dccd5178da6d0578d6f50e8b48936
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350971"
---
# <a name="iinkanalysisrecognizergetlanguages-method"></a>Metodo IInkAnalysisRecognizer::GetLanguages

Recupera gli identificatori per le impostazioni locali supportate da [**IInkAnalysisRecognizer.**](iinkanalysisrecognizer.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetLanguages(
  [in, out] ULONG *pulLanguagesCount,
  [out]     ULONG **ppulLanguages
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pulLanguagesCount* \[ in, out\]
</dt> <dd>

Numero di identificatori in *ppulLanguages*.

</dd> <dt>

*ppulLanguages* \[ Cambio\]
</dt> <dd>

Puntatore agli identificatori per le impostazioni locali supportate da [**IInkAnalysisRecognizer.**](iinkanalysisrecognizer.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, usare [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) per rilasciare la memoria da \* *ppulLanguages* quando non sono più necessarie le informazioni.

 

Questo metodo restituisce una matrice vuota per i riconoscitori di oggetti e movimenti.

Per altre informazioni sugli identificatori di lingua, vedere Costanti e stringhe degli [identificatori di lingua](/windows/desktop/Intl/language-identifier-constants-and-strings).

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

 


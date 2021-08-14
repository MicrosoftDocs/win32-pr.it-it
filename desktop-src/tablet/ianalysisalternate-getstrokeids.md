---
description: Restituisce gli identificatori di tratto associati a questo oggetto IAnalysisAlternate.
ms.assetid: 495d485f-0d16-4085-9213-cc55f3f259f0
title: Metodo IAnalysisAlternate::GetStrokeIds (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetStrokeIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2682107a58f126011c4d80a02a119219ccea0976408937e19eb7b511eb82cff9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967500"
---
# <a name="ianalysisalternategetstrokeids-method"></a>Metodo IAnalysisAlternate::GetStrokeIds

Restituisce gli identificatori dei tratti associati a questo [**oggetto IAnalysisAlternate.**](ianalysisalternate.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetStrokeIds(
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     LONG  **pplStrokeIds
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pulStrokeIdsCount* \[ in, out\]
</dt> <dd>

Puntatore a **un ULONG** impostato sul numero di identificatori di tratto associati a [**questo oggetto IAnalysisAlternate.**](ianalysisalternate.md)

</dd> <dt>

*pplStrokeIds* \[ Cambio\]
</dt> <dd>

\[out, size \_ is( \* *pulStrokeIdsCount* \* sizeof(LONG))\]

Matrice di **long di** lunghezza *pulStrokeIdsCount* impostata per gli identificatori di tratto associati a questo oggetto [**IAnalysisAlternate.**](ianalysisalternate.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, usare [CoTaskMemFree](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) per rilasciare la memoria da \* *pplStrokeIds* quando non sono più necessarie le informazioni.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

 


---
description: Recupera l'oggetto IInkAnalysisRecognizer in corrispondenza dell'indice specificato.
ms.assetid: e4db56c6-7c15-4336-bc0a-f50222c3520e
title: Metodo IInkAnalysisRecognizers::GetInkAnalysisRecognizer (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizers.GetInkAnalysisRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6755b82beaea1bec9a38b9c15ea57a97c1d19fc4eecb5a2b55c80e2070562d07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967340"
---
# <a name="iinkanalysisrecognizersgetinkanalysisrecognizer-method"></a>Metodo IInkAnalysisRecognizers::GetInkAnalysisRecognizer

Recupera [**l'oggetto IInkAnalysisRecognizer in**](iinkanalysisrecognizer.md) corrispondenza dell'indice specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetInkAnalysisRecognizer(
  [in]  ULONG                  ulIndex,
  [out] IInkAnalysisRecognizer **ppInkAnalysisRecognizer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ulIndex* \[ Pollici\]
</dt> <dd>

Indice in base zero [**dell'oggetto IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) da ottenere.

</dd> <dt>

*ppInkAnalysisRecognizer* \[ Cambio\]
</dt> <dd>

Puntatore a [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) in corrispondenza dell'indice specificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su \* *ppInkAnalysisRecognizer* quando non è più necessario usare il riconoscimento dell'analisi input penna.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**InkAnalysisRecognizers**](iinkanalysisrecognizers.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

 


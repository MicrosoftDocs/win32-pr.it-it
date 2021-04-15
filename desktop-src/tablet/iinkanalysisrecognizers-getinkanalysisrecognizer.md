---
description: Recupera l'oggetto IInkAnalysisRecognizer in corrispondenza dell'indice specificato.
ms.assetid: e4db56c6-7c15-4336-bc0a-f50222c3520e
title: 'Metodo IInkAnalysisRecognizers:: GetInkAnalysisRecognizer (IACom. h)'
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
ms.openlocfilehash: 1008ae0b26d30233c3b00167391523d321cd381e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485092"
---
# <a name="iinkanalysisrecognizersgetinkanalysisrecognizer-method"></a>Metodo IInkAnalysisRecognizers:: GetInkAnalysisRecognizer

Recupera l'oggetto [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) in corrispondenza dell'indice specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetInkAnalysisRecognizer(
  [in]  ULONG                  ulIndex,
  [out] IInkAnalysisRecognizer **ppInkAnalysisRecognizer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ulIndex* \[ in\]
</dt> <dd>

Indice in base zero dell'oggetto [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) da ottenere.

</dd> <dt>

*ppInkAnalysisRecognizer* \[ out\]
</dt> <dd>

Puntatore a [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) in corrispondenza dell'indice specificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su \* *ppInkAnalysisRecognizer* quando non è più necessario usare il sistema di riconoscimento dell'analisi dell'input penna.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**InkAnalysisRecognizers**](iinkanalysisrecognizers.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 


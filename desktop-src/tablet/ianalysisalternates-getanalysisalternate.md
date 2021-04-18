---
description: Recupera l'oggetto IAnalysisAlternate in corrispondenza dell'indice specificato all'interno dell'insieme.
ms.assetid: d927e2f1-ca21-415d-90ad-d1ded575fcb7
title: 'Metodo IAnalysisAlternates:: GetAnalysisAlternate (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternates.GetAnalysisAlternate
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 122bccc4985ed7ba5617e9d373ecdf3d0c84dac2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307475"
---
# <a name="ianalysisalternatesgetanalysisalternate-method"></a>Metodo IAnalysisAlternates:: GetAnalysisAlternate

Recupera l'oggetto [**IAnalysisAlternate**](ianalysisalternate.md) in corrispondenza dell'indice specificato all'interno dell'insieme.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetAnalysisAlternate(
  [in]  ULONG              ulIndex,
  [out] IAnalysisAlternate **ppAlternate
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ulIndex* \[ in\]
</dt> <dd>

Indice in base zero dell'oggetto [**IAnalysisAlternate**](ianalysisalternate.md) da ottenere.

</dd> <dt>

*ppAlternate* \[ out\]
</dt> <dd>

Puntatore all'oggetto [**IAnalysisAlternate**](ianalysisalternate.md) in corrispondenza dell'indice specificato all'interno dell'insieme.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su \* *ppAlternate* quando non è più necessario usare l'alternativa di analisi.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IAnalysisAlternates**](ianalysisalternates.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 


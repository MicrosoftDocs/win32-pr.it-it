---
description: Recupera il numero di oggetti IContextNode contenuti in questa raccolta.
ms.assetid: 7cc60bea-9a4c-4ac8-ad1a-0fca5e941c5e
title: 'Metodo IContextNodes:: GetCount (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes.GetCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8d694849b3436f9f30a687579362d01a111ace80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129483"
---
# <a name="icontextnodesgetcount-method"></a>Metodo IContextNodes:: GetCount

Recupera il numero di oggetti [**IContextNode**](icontextnode.md) contenuti in questa raccolta.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCount(
  [out] ULONG *pulCount
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pulCount* \[ out\]
</dt> <dd>

Numero di oggetti [**IContextNode**](icontextnode.md) contenuti in questa raccolta.

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

[**IContextNodes**](icontextnodes.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





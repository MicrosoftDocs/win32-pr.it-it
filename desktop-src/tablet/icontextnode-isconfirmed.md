---
description: Recupera un valore che indica se l'oggetto ConfirmationType passato a questo metodo è stato impostato su questo IContextNode.
ms.assetid: 4a96bc46-b627-4784-ad1d-1079f49592e5
title: 'Metodo IContextNode:: IsValid (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.IsConfirmed
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 300e0126b4a1ff55d372ff31deebde0eab686645
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526520"
---
# <a name="icontextnodeisconfirmed-method"></a>Metodo IContextNode:: IsValid

Recupera un valore che indica se l'oggetto ConfirmationType passato a questo metodo è stato impostato su questo IContextNode.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsConfirmed(
  [in]  ConfirmationType confirmedType,
  [out] VARIANT_BOOL     *pfTypeConfirmed
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*confirmedType* \[ in\]
</dt> <dd>

Tipo di conferma sottoposto a test.

</dd> <dt>

*pfTypeConfirmed* \[ out\]
</dt> <dd>

**Variante \_ TRUE** se il tipo passato in confirmedType è stato impostato su questo oggetto [**IContextNode**](icontextnode.md) ; in caso contrario, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Questo valore viene impostato dal metodo [**IContextNode:: Confirm**](icontextnode-confirm.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode:: Confirm**](icontextnode-confirm.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





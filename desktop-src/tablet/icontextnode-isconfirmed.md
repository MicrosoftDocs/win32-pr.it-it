---
description: Recupera un valore che indica se l'elemento ConfirmationType passato a questo metodo è stato impostato su questo IContextNode.
ms.assetid: 4a96bc46-b627-4784-ad1d-1079f49592e5
title: Metodo IContextNode::IsConfirmed (IACom.h)
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
ms.openlocfilehash: 2e378aaf344e177514115c82b1179f8d1ebe25faefa0d5d840d5a0af62ff1c07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967360"
---
# <a name="icontextnodeisconfirmed-method"></a>Metodo IContextNode::IsConfirmed

Recupera un valore che indica se l'elemento ConfirmationType passato a questo metodo è stato impostato su questo IContextNode.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsConfirmed(
  [in]  ConfirmationType confirmedType,
  [out] VARIANT_BOOL     *pfTypeConfirmed
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*confirmedType* \[ Pollici\]
</dt> <dd>

Tipo di conferma di cui eseguire il test.

</dd> <dt>

*pfTypeConfirmed* \[ Cambio\]
</dt> <dd>

**VARIANT \_ TRUE** se il tipo passato in confirmedType è stato impostato su questo [**oggetto IContextNode;**](icontextnode.md) in caso contrario, **VARIANT \_ FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Commenti

Questo valore viene impostato dal [**metodo IContextNode::Confirm.**](icontextnode-confirm.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::Confirm**](icontextnode-confirm.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





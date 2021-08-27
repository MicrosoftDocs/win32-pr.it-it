---
description: Recupera il numero di versione del sistema di eventi.
ms.assetid: 6355f1b3-e1e7-435f-9795-d92464e004ae
title: Metodo IEventSystem2::GetVersion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSystem2.GetVersion
api_type:
- COM
api_location: ''
ms.openlocfilehash: 77452ccebac71cb8de8357fee0199bc04b690d59cf8d113d57a5850db0771315
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070621"
---
# <a name="ieventsystem2getversion-method"></a>Metodo IEventSystem2::GetVersion

Recupera il numero di versione del sistema di eventi.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetVersion(
  [out] int *pnVersion
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pnVersion* \[ Cambio\]
</dt> <dd>

Numero di versione del sistema di eventi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire i valori restituiti standard E \_ INVALIDARG, E \_ OUTOFMEMORY, E \_ UNEXPECTED, E \_ FAIL e S \_ OK.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IEventSystem2**](ieventsystem2.md)
</dt> </dl>

 

 





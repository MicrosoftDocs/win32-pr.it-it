---
description: Restituisce il numero di elementi archiviati da questo enumeratore.
ms.assetid: d374ec81-0bd5-4b5d-8002-e3b53476421a
title: Metodo IEnumWiaItem2::GetCount (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.GetCount
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 0a64a7c015f7c21ff19a736570aa104f0b229bc1b6561001b612045824f9a31d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882421"
---
# <a name="ienumwiaitem2getcount-method"></a>Metodo IEnumWiaItem2::GetCount

Restituisce il numero di elementi archiviati da questo enumeratore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCount(
  [out] ULONG *cElt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*cElt* \[ Cambio\]
</dt> <dd>

Tipo: **ULONG \***

Riceve un puntatore a **un ULONG** che riceve il numero di elementi nell'enumerazione .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 





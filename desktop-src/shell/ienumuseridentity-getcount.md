---
description: GetCount non è supportato e potrebbe essere modificato o non disponibile in futuro. Usare invece gli account utente con cambio utente rapido e Desktop remoto.
ms.assetid: 1fe39f2d-f95e-4436-a780-40fe8bd41b74
title: Metodo IEnumUserIdentity::GetCount (Msident.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.GetCount
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: e4848ec183096b37adbc04521fab04fd800d3783377d1e14b3abd068819648ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117678938"
---
# <a name="ienumuseridentitygetcount-method"></a>Metodo IEnumUserIdentity::GetCount

\[**GetCount** non è supportato e potrebbe essere modificato o non disponibile in futuro. Usare invece gli [account utente con cambio utente rapido e Desktop remoto](fastuserswitching.md).\]

Ottiene il conteggio delle identità utente attualmente presenti nel sistema.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCount(
  [out] ULONG *pnCount
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pnCount* \[ Cambio\]
</dt> <dd>

Tipo: **ULONG \***

Puntatore a **un ULONG** che riceve il conteggio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Se il supporto per più identità utente è disabilitato, *pnCount* riceverà il valore 1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                            |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                   |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                  |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                         |
| Intestazione<br/>                   | <dl> <dt>Msident.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msident.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IEnumUserIdentity**](ienumuseridentity.md)
</dt> <dt>

[**IEnumUserIdentity::Skip**](ienumuseridentity-skip.md)
</dt> <dt>

[**IEnumUserIdentity::Reset**](ienumuseridentity-reset.md)
</dt> <dt>

[**IEnumUserIdentity::Next**](ienumuseridentity-next.md)
</dt> </dl>

 

 





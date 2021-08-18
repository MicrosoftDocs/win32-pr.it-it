---
description: IEnumUserIdentity::Next non è supportato e potrebbe essere modificato o non disponibile in futuro. Usare invece gli account utente con cambio rapido utente e Desktop remoto.
ms.assetid: 2c8dfe36-c1bb-49f8-8847-f355cfab2984
title: Metodo IEnumUserIdentity::Next (Msident.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Next
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: eb3074a7b55ce03e7372491fce11160f1df1bc5fc8a4e45ad0f12d4538d4b2f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009401"
---
# <a name="ienumuseridentitynext-method"></a>Metodo IEnumUserIdentity::Next

\[**IEnumUserIdentity::Next** non è supportato e potrebbe essere modificato o non disponibile in futuro. Usare invece gli [account utente con cambio rapido utente e](fastuserswitching.md)Desktop remoto .\]

Deprecato. Recupera una matrice di interfacce di identità utente dall'enumerazione .

## <a name="syntax"></a>Sintassi


```C++
HRESULT Next(
  [in]  ULONG    celt,
  [out] IUnknown **rgelt,
  [out] ULONG    *pceltFetched
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*celt* \[ Pollici\]
</dt> <dd>

Tipo: **ULONG**

Valore **ULONG** che rappresenta il numero di interfacce da recuperare.

</dd> <dt>

*rgelt* \[ Cambio\]
</dt> <dd>

Tipo: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***

Indirizzo di un puntatore che riceve le interfacce.

</dd> <dt>

*pceltFetched* \[ Cambio\]
</dt> <dd>

Tipo: **ULONG \***

Indirizzo di un puntatore che riceve il numero di interfacce recuperate correttamente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

[**IEnumUserIdentity**](ienumuseridentity.md) mantiene un conteggio interno che specifica quale interfaccia deve essere recuperata. Più chiamate a questo metodo non reimpostano questo conteggio. Per reimpostare il conteggio, chiamare [**IEnumUserIdentity::Reset**](ienumuseridentity-reset.md). Per incrementare il conteggio senza recuperare le interfacce, chiamare [**IEnumUserIdentity::Skip**](ienumuseridentity-skip.md).

Il valore di *celt* non deve superare il valore restituito da [**IEnumUserIdentity::GetCount**](ienumuseridentity-getcount.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                            |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                   |
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

[**IEnumUserIdentity::GetCount**](ienumuseridentity-getcount.md)
</dt> </dl>

 

 

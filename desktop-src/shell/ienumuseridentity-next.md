---
description: 'IEnumUserIdentity:: Next non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli account utente con cambio rapido utente e Desktop remoto.'
ms.assetid: 2c8dfe36-c1bb-49f8-8847-f355cfab2984
title: 'Metodo IEnumUserIdentity:: Next (Msident. h)'
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
ms.openlocfilehash: 763b2b4a612596c5f02a9826ad2e9c09ab8e4b0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994608"
---
# <a name="ienumuseridentitynext-method"></a>IEnumUserIdentity:: Next (metodo)

\[**IEnumUserIdentity:: Next** non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli [account utente con cambio rapido utente e desktop remoto](fastuserswitching.md).\]

Deprecato. Recupera una matrice di interfacce di identità utente dall'enumerazione.

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

*celt* \[ in\]
</dt> <dd>

Tipo: **ULONG**

Valore **ULONG** che rappresenta il numero di interfacce da recuperare.

</dd> <dt>

*rgelt* \[ out\]
</dt> <dd>

Tipo: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***

Indirizzo di un puntatore che riceve le interfacce.

</dd> <dt>

*pceltFetched* \[ out\]
</dt> <dd>

Tipo: **ULONG \** _

Indirizzo di un puntatore che riceve il numero di interfacce recuperate correttamente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: _ *HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

[**IEnumUserIdentity**](ienumuseridentity.md) mantiene un conteggio interno che specifica l'interfaccia successiva da recuperare. Per più chiamate a questo metodo non verrà reimpostato questo conteggio. Per reimpostare il conteggio, chiamare [**IEnumUserIdentity:: Reset**](ienumuseridentity-reset.md). Per incrementare il conteggio senza recuperare le interfacce, chiamare [**IEnumUserIdentity:: Skip**](ienumuseridentity-skip.md).

Il valore di *celt* non deve superare il valore restituito da [**IEnumUserIdentity:: GetCount**](ienumuseridentity-getcount.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                   |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                  |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                         |
| Intestazione<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IEnumUserIdentity**](ienumuseridentity.md)
</dt> <dt>

[**IEnumUserIdentity:: Skip**](ienumuseridentity-skip.md)
</dt> <dt>

[**IEnumUserIdentity:: Reset**](ienumuseridentity-reset.md)
</dt> <dt>

[**IEnumUserIdentity:: GetCount**](ienumuseridentity-getcount.md)
</dt> </dl>

 

 

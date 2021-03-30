---
description: 'IEnumUserIdentity:: Skip non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli account utente con cambio rapido utente e Desktop remoto.'
ms.assetid: bb19ae50-b384-48fb-9272-15e3e3eaa9d0
title: 'Metodo IEnumUserIdentity:: Skip (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Skip
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: cedd4f3c6e9736e26cbf8d58f27f805f0f5d33a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994600"
---
# <a name="ienumuseridentityskip-method"></a>Metodo IEnumUserIdentity:: Skip

\[**IEnumUserIdentity:: Skip** non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli [account utente con cambio rapido utente e desktop remoto](fastuserswitching.md).\]

Ignora un determinato numero di interfacce di identità utente nell'enumerazione. Utilizzato durante il recupero delle interfacce.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*celt* \[ in\]
</dt> <dd>

Tipo: **ULONG**

Numero di interfacce da ignorare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

[**IEnumUserIdentity**](ienumuseridentity.md) mantiene un conteggio interno che specifica l'interfaccia successiva da recuperare. Per incrementare il conteggio senza recuperare le interfacce, chiamare questo metodo. Per reimpostare il conteggio, chiamare [**IEnumUserIdentity:: Reset**](ienumuseridentity-reset.md).

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

[**IEnumUserIdentity:: Reset**](ienumuseridentity-reset.md)
</dt> <dt>

[**IEnumUserIdentity:: Next**](ienumuseridentity-next.md)
</dt> <dt>

[**IEnumUserIdentity:: GetCount**](ienumuseridentity-getcount.md)
</dt> </dl>

 

 





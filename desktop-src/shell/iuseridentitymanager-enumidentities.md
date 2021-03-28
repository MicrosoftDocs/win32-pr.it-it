---
description: 'IUserIdentityManager:: EnumIdentities non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli account utente con cambio rapido utente e Desktop remoto.'
ms.assetid: 8111fbcd-dc4d-45cb-83e0-3c2cd7c4df27
title: 'Metodo IUserIdentityManager:: EnumIdentities (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.EnumIdentities
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 3109867651b69e311639d8b2e70e5f02e33a3dc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127834"
---
# <a name="iuseridentitymanagerenumidentities-method"></a>Metodo IUserIdentityManager:: EnumIdentities

\[**IUserIdentityManager:: EnumIdentities** non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli [account utente con cambio rapido utente e desktop remoto](fastuserswitching.md).\]

Ottiene un oggetto [**IEnumUserIdentity**](ienumuseridentity.md) che può essere utilizzato per enumerare le identità utente presenti nel sistema.

## <a name="syntax"></a>Sintassi


```C++
HRESULT EnumIdentities(
  [out] IEnumUserIdentity **ppEnumUser
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppEnumUser* \[ out\]
</dt> <dd>

Tipo: **[ **IEnumUserIdentity**](ienumuseridentity.md)\*\***

Indirizzo del puntatore al nuovo oggetto di enumerazione di identità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Risultato dell'operazione di recupero. Se ha esito positivo, restituisce S \_ OK. Se non è stato possibile creare l'oggetto di enumerazione, viene restituito E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Questo metodo è utile per l'iterazione dell'elenco di identità nel sistema. Per recuperare una singola identità tramite il cookie senza accedere all'elenco, chiamare [**IUserIdentityManager:: GetIdentityByCookie**](iuseridentitymanager-getidentitybycookie.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Fine del supporto client<br/>    | Windows 2000 Professional<br/>                                                   |
| Fine del supporto server<br/>    | Windows 2000 Server<br/>                                                         |
| Intestazione<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IUserIdentityManager**](iuseridentitymanager.md)
</dt> <dt>

[**IEnumUserIdentity**](ienumuseridentity.md)
</dt> <dt>

[**IUserIdentityManager::GetIdentityByCookie**](iuseridentitymanager-getidentitybycookie.md)
</dt> </dl>

 

 





---
description: GetIdentityByCookie non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli account utente con cambio rapido utente e Desktop remoto.
ms.assetid: c2f549ac-e13d-4198-864f-7f5fbec30c72
title: 'Metodo IUserIdentityManager:: GetIdentityByCookie (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.GetIdentityByCookie
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: eb4e5ad5bda349a5b1650b090abc44a9fd1e6332
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524441"
---
# <a name="iuseridentitymanagergetidentitybycookie-method"></a>Metodo IUserIdentityManager:: GetIdentityByCookie

\[**GetIdentityByCookie** non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli [account utente con cambio rapido utente e desktop remoto](fastuserswitching.md).\]

Ottiene un'identità utente specifica dal cookie usato per identificarla in modo univoco.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetIdentityByCookie(
  [in]  GUID          *uidCookie,
  [out] IUserIdentity **ppIdentity
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*uidCookie* \[ in\]
</dt> <dd>

Tipo: **GUID \** _

Indirizzo di un valore _ *GUID** che rappresenta il cookie per l'identità che si vuole recuperare.

</dd> <dt>

*ppIdentity* \[ out\]
</dt> <dd>

Tipo: **[ **IUserIdentity**](iuseridentity.md)\*\***

Indirizzo del puntatore che riceverà l'oggetto identità utente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Risultato della richiesta di recupero. Se ha esito positivo, restituisce S \_ OK. In caso contrario, verrà restituito uno dei codici di errore seguenti.



| Codice restituito                                                                                            | Descrizione                                               |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**\_identità E \_ non \_ trovate**</dt> </dl> | Impossibile trovare l'identità richiesta.<br/>     |
| <dl> <dt>**\_identità E \_ disabilitate**</dt> </dl> | Gestione identità è disabilitato nel sistema.<br/> |



 

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



 

 





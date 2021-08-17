---
description: GetIdentityByCookie non è supportato e potrebbe essere modificato o non disponibile in futuro. Usare invece gli account utente con cambio utente rapido e Desktop remoto.
ms.assetid: c2f549ac-e13d-4198-864f-7f5fbec30c72
title: Metodo IUserIdentityManager::GetIdentityByCookie (Msident.h)
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
ms.openlocfilehash: a077f3e6a65a04e4c018198dde39b80c5a6e5acbee282c9e2cc282642526894b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117678155"
---
# <a name="iuseridentitymanagergetidentitybycookie-method"></a>Metodo IUserIdentityManager::GetIdentityByCookie

\[**GetIdentityByCookie** non è supportato e potrebbe essere modificato o non disponibile in futuro. Usare invece gli [account utente con cambio utente rapido e Desktop remoto](fastuserswitching.md).\]

Ottiene un'identità utente specifica dal cookie utilizzato per identificarla in modo univoco.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetIdentityByCookie(
  [in]  GUID          *uidCookie,
  [out] IUserIdentity **ppIdentity
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*uidCookie* \[ Pollici\]
</dt> <dd>

Tipo: **\* GUID**

Indirizzo di un **valore GUID** che rappresenta il cookie per l'identità che si desidera recuperare.

</dd> <dt>

*ppIdentity* \[ Cambio\]
</dt> <dd>

Tipo: **[ **IUserIdentity**](iuseridentity.md)\*\***

Indirizzo del puntatore che riceverà l'oggetto identità utente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Risultato della richiesta di recupero. Se ha esito positivo, restituisce S \_ OK. In caso contrario, verrà restituito uno dei codici di errore seguenti.



| Codice restituito                                                                                            | Descrizione                                               |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**E \_ IDENTITÀ \_ NON \_ TROVATA**</dt> </dl> | Impossibile trovare l'identità richiesta.<br/>     |
| <dl> <dt>**IDENTITÀ E \_ \_ DISABILITATE**</dt> </dl> | La gestione delle identità è disabilitata nel sistema.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Fine del supporto client<br/>    | Windows 2000 Professional<br/>                                                   |
| Fine del supporto server<br/>    | Windows 2000 Server<br/>                                                         |
| Intestazione<br/>                   | <dl> <dt>Msident.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msident.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



 

 





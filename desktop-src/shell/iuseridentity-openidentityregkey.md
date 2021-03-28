---
description: Deprecato. Recupera la chiave nel registro di sistema che corrisponde a questa identità utente.
ms.assetid: eecf8b73-e86a-4274-8d9c-c601153f81db
title: 'Metodo IUserIdentity:: OpenIdentityRegKey (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.OpenIdentityRegKey
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: f1d67918f4a9802e63682e0663994c1ea6a06200
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977895"
---
# <a name="iuseridentityopenidentityregkey-method"></a>Metodo IUserIdentity:: OpenIdentityRegKey

\[Il metodo **IUserIdentity:: OpenIdentityRegKey** è disponibile per l'uso in Windows 2000. In Windows XP questa funzionalità è stata sostituita dagli [account utente con cambio rapido utente e desktop remoto](fastuserswitching.md)e potrebbe essere modificata o non disponibile nelle versioni successive.\]

Deprecato. Recupera la chiave nel registro di sistema che corrisponde a questa identità utente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OpenIdentityRegKey(
  [in]  DWORD dwDesiredAccess,
  [out] HKEY  *phKey
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwDesiredAccess* \[ in\]
</dt> <dd>

Tipo: **DWORD**

Valore che descrive il livello di accesso richiesto dalla chiave del registro di sistema.

</dd> <dt>

*phKey* \[ out\]
</dt> <dd>

Tipo: **HKEY \** _

Puntatore che riceve la chiave del registro di sistema.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: _ *HRESULT**

Risultato della richiesta del registro di sistema. Se ha esito positivo, restituisce **S \_ OK**. In caso contrario, verrà restituito uno dei codici di errore seguenti.



| Codice restituito                                                                                            | Descrizione                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**\_identità E \_ non \_ trovate**</dt> </dl> | A questa identità non è associata una chiave del registro di sistema.<br/> |
| <dl> <dt>**E \_ non riescono**</dt> </dl>                 | Impossibile accedere alla chiave del registro di sistema.<br/>             |



 

## <a name="remarks"></a>Commenti

Il parametro *dwDesiredAccess* è un descrittore di sicurezza di accesso al registro di sistema standard che descrive l'accesso che si desidera ottenere alla chiave del registro di sistema. Per altre informazioni sulla sicurezza del registro di sistema, incluso un elenco di valori accettabili per questo parametro, vedere [sicurezza e diritti di accesso per la chiave del registro di sistema](../sysinfo/registry-key-security-and-access-rights.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IUserIdentity**](iuseridentity.md)
</dt> <dt>

[**IUserIdentity::GetIdentityFolder**](iuseridentity-getidentityfolder.md)
</dt> </dl>

 

 

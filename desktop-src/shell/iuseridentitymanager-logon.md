---
description: 'IUserIdentityManager:: Logon non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli account utente con cambio rapido utente e Desktop remoto.'
ms.assetid: ba146ee1-6c9c-4f97-ae90-431aa084ea16
title: 'Metodo IUserIdentityManager:: Logon (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.Logon
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: eee6e0555d45d3f52173fce085d19c14f2ccfe8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127830"
---
# <a name="iuseridentitymanagerlogon-method"></a>Metodo IUserIdentityManager:: Logon

\[**IUserIdentityManager:: Logon** non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli [account utente con cambio rapido utente e desktop remoto](fastuserswitching.md).\]

Visualizza un'interfaccia utente per l'utente, consentendo all'utente di scegliere un'identità utente. Se l'esito è positivo, l'identità utente verrà registrata e recuperata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Logon(
  [in]  HWND          hwndParent,
  [in]  DWORD         dwFlags,
  [out] IUserIdentity **ppIdentity
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hwndParent* \[ in\]
</dt> <dd>

Tipo: **HWND**

Valore **HWND** che identifica una finestra che verrà portata in primo piano dopo che l'interfaccia utente di accesso viene rilasciata.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Tipo: **DWORD**

Flag facoltativi per definire il comportamento dell'interfaccia utente. Impostare su UIL \_ Force \_ UI per forzare la visualizzazione dell'interfaccia utente, anche se è già stata scelta un'identità.

</dd> <dt>

*ppIdentity* \[ out\]
</dt> <dd>

Tipo: **[ **IUserIdentity**](iuseridentity.md)\*\***

Indirizzo del puntatore che riceve l'identità utente scelta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Risultato dell'operazione di accesso. Se ha esito positivo, restituisce S \_ OK. In caso contrario, verrà restituito uno dei codici di errore seguenti.



| Codice restituito                                                                                            | Descrizione                                                                                 |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ utente \_ annullato**</dt> </dl>      | L'utente ha annullato l'operazione di accesso dall'interfaccia utente.<br/>                               |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl>          | Non è stato possibile creare l'identità utente.<br/>                                          |
| <dl> <dt>**E \_ imprevisto**</dt> </dl>           | L'operazione non è riuscita in modo imprevisto.<br/>                                               |
| <dl> <dt>**\_identità E \_ disabilitate**</dt> </dl> | Gestione identità è disabilitato nel sistema.<br/>                                   |
| <dl> <dt>**\_identità \_ disabilitate**</dt> </dl> | Gestione identità è disabilitato nel sistema.<br/>                                   |
| <dl> <dt>**\_modifica dell'identità E \_**</dt> </dl>   | Il sistema sta attualmente cambiando identità e non è in grado di completare l'operazione.<br/> |



 

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

[**IUserIdentityManager:: disconnessione**](iuseridentitymanager-logoff.md)
</dt> <dt>

[**IUserIdentityManager::ManageIdentities**](iuseridentitymanager-manageidentities.md)
</dt> </dl>

 

 





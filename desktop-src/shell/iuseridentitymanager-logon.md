---
description: IUserIdentityManager::Logon non è supportato e potrebbe essere modificato o non disponibile in futuro. Usare invece gli account utente con cambio utente rapido e Desktop remoto.
ms.assetid: ba146ee1-6c9c-4f97-ae90-431aa084ea16
title: Metodo IUserIdentityManager::Logon (Msident.h)
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
ms.openlocfilehash: e5be9402dbbbf7c46528ceeab944317fa35857f9521db41b621ab246c8da86be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821131"
---
# <a name="iuseridentitymanagerlogon-method"></a>Metodo IUserIdentityManager::Logon

\[**IUserIdentityManager::Logon** non è supportato e potrebbe essere modificato o non disponibile in futuro. Usare invece gli [account utente con cambio rapido utente e Desktop remoto](fastuserswitching.md).\]

Visualizza un'interfaccia utente all'utente, consentendo all'utente di scegliere un'identità utente. In caso di esito positivo, l'identità utente verrà registrata e recuperata.

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

*hwndParent* \[ Pollici\]
</dt> <dd>

Tipo: **HWND**

Valore **HWND** che identifica una finestra che verrà portata in primo piano dopo la chiusura dell'interfaccia utente di accesso.

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Tipo: **DWORD**

Flag facoltativi per definire il comportamento dell'interfaccia utente. Impostare su UIL FORCE UI per forzare la visualizzazione \_ dell'interfaccia \_ utente, anche se è già stata scelta un'identità.

</dd> <dt>

*ppIdentity* \[ Cambio\]
</dt> <dd>

Tipo: **[ **IUserIdentity**](iuseridentity.md)\*\***

Indirizzo del puntatore che riceve l'identità utente scelta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Risultato dell'operazione di accesso. Se ha esito positivo, restituisce S \_ OK. In caso contrario, restituirà uno dei codici di errore seguenti.



| Codice restituito                                                                                            | Descrizione                                                                                 |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ UTENTE \_ ANNULLATO**</dt> </dl>      | L'utente ha annullato l'operazione di accesso dall'interfaccia utente.<br/>                               |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Impossibile creare l'identità utente.<br/>                                          |
| <dl> <dt>**E \_ IMPREVISTO**</dt> </dl>           | L'operazione non è riuscita in modo imprevisto.<br/>                                               |
| <dl> <dt>**IDENTITÀ E \_ \_ DISABILITATE**</dt> </dl> | La gestione delle identità è disabilitata nel sistema.<br/>                                   |
| <dl> <dt>**IDENTITÀ S \_ \_ DISABILITATE**</dt> </dl> | La gestione delle identità è disabilitata nel sistema.<br/>                                   |
| <dl> <dt>**E \_ MODIFICA \_ DELL'IDENTITÀ**</dt> </dl>   | Il sistema sta attualmente scambiando identità e non può completare l'operazione.<br/> |



 

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



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IUserIdentityManager**](iuseridentitymanager.md)
</dt> <dt>

[**IUserIdentityManager::Logoff**](iuseridentitymanager-logoff.md)
</dt> <dt>

[**IUserIdentityManager::ManageIdentities**](iuseridentitymanager-manageidentities.md)
</dt> </dl>

 

 





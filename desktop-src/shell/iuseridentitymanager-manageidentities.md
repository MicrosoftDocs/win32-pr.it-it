---
description: IUserIdentityManager::ManageIdentities non è supportato e potrebbe essere modificato o non disponibile in futuro. Usare invece gli account utente con cambio rapido utente e Desktop remoto.
ms.assetid: 9a5a85bd-d007-4247-859b-e402ed290785
title: Metodo IUserIdentityManager::ManageIdentities (Msident.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.ManageIdentities
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: a816ee16e128b992b18be274d814fe3369e1a59c0204201a9c6bd4a6cbc23857
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859239"
---
# <a name="iuseridentitymanagermanageidentities-method"></a>Metodo IUserIdentityManager::ManageIdentities

\[**IUserIdentityManager::ManageIdentities** non è supportato e potrebbe essere modificato o non disponibile in futuro. Usare invece gli [account utente con cambio rapido utente e](fastuserswitching.md)Desktop remoto .\]

Visualizza un'interfaccia utente per l'utente, consentendo all'utente di gestire le identità utente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ManageIdentities(
  [in] HWND  hwndParent,
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hwndParent* \[ Pollici\]
</dt> <dd>

Tipo: **HWND**

Valore **HWND** che identifica una finestra che verrà portata in primo piano dopo la chiusura dell'interfaccia utente.

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Tipo: **DWORD**

Flag facoltativi per definire il comportamento dell'interfaccia utente. Impostare su UIMI \_ CREATE NEW IDENTITY per richiedere \_ \_ all'utente di creare una nuova identità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Risultato dell'operazione di gestione. Se ha esito positivo, restituisce S \_ OK. In caso contrario, restituirà uno dei codici di errore seguenti.



| Codice restituito                                                                                            | Descrizione                                               |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**IDENTITÀ E \_ \_ DISABILITATE**</dt> </dl> | La gestione delle identità è disabilitata nel sistema.<br/> |
| <dl> <dt>**E \_ UTENTE \_ ANNULLATO**</dt> </dl>      | L'utente ha annullato la finestra di dialogo.<br/>                  |



 

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

[**IUserIdentityManager::Logon**](iuseridentitymanager-logon.md)
</dt> <dt>

[**IUserIdentityManager::Logoff**](iuseridentitymanager-logoff.md)
</dt> </dl>

 

 





---
description: 'IUserIdentityManager:: ManageIdentities non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli account utente con cambio rapido utente e Desktop remoto.'
ms.assetid: 9a5a85bd-d007-4247-859b-e402ed290785
title: 'Metodo IUserIdentityManager:: ManageIdentities (Msident. h)'
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
ms.openlocfilehash: b5b782a56324faf19dd1527d2cd363d26f0e337c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342436"
---
# <a name="iuseridentitymanagermanageidentities-method"></a>Metodo IUserIdentityManager:: ManageIdentities

\[**IUserIdentityManager:: ManageIdentities** non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli [account utente con cambio rapido utente e desktop remoto](fastuserswitching.md).\]

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

*hwndParent* \[ in\]
</dt> <dd>

Tipo: **HWND**

Valore **HWND** che identifica una finestra che verrà portata in primo piano dopo la chiusura dell'interfaccia utente.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Tipo: **DWORD**

Flag facoltativi per definire il comportamento dell'interfaccia utente. Impostare su UIMI \_ Crea \_ nuova \_ identità per richiedere all'utente di creare una nuova identità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Risultato dell'operazione di gestione. Se ha esito positivo, restituisce S \_ OK. In caso contrario, verrà restituito uno dei codici di errore seguenti.



| Codice restituito                                                                                            | Descrizione                                               |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**\_identità E \_ disabilitate**</dt> </dl> | Gestione identità è disabilitato nel sistema.<br/> |
| <dl> <dt>**E \_ utente \_ annullato**</dt> </dl>      | L'utente ha annullato la finestra di dialogo.<br/>                  |



 

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

[**IUserIdentityManager:: Logon**](iuseridentitymanager-logon.md)
</dt> <dt>

[**IUserIdentityManager:: disconnessione**](iuseridentitymanager-logoff.md)
</dt> </dl>

 

 





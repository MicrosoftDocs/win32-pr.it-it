---
description: Deprecato. Fornisce la notifica delle modifiche alle identità utente nel sistema, nonché le richieste degli utenti per cambiare l'identità dell'utente corrente.
ms.assetid: 09903aa6-62bf-4820-9a09-79956d775441
title: Interfaccia IIdentityChangeNotify (Msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: 4a217b2cfb046bfb9ae5546e015264f74d00b1d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227425"
---
# <a name="iidentitychangenotify-interface"></a>Interfaccia IIdentityChangeNotify

\[L'interfaccia **IIdentityChangeNotify** è disponibile per l'uso in Windows 2000. In Windows XP questa funzionalità è stata sostituita dagli [account utente con cambio rapido utente e desktop remoto](fastuserswitching.md)e potrebbe essere modificata o non disponibile nelle versioni successive.\]

Deprecato. Fornisce la notifica delle modifiche alle identità utente nel sistema, nonché le richieste degli utenti per cambiare l'identità dell'utente corrente.

## <a name="members"></a>Membri

L'interfaccia **IIdentityChangeNotify** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IIdentityChangeNotify** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IIdentityChangeNotify** dispone di questi metodi.



| Metodo                                                                                 | Descrizione                                                                                                                           |
|:---------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------|
| [**IdentityInformationChanged**](iidentitychangenotify-identityinformationchanged.md) | Deprecato. Chiamato quando le informazioni relative a un'identità utente sono state modificate o quando un'identità utente è stata aggiunta o eliminata.<br/>  |
| [**QuerySwitchIdentities**](iidentitychangenotify-queryswitchidentities.md)           | Deprecato. Viene chiamato quando l'utente corrente ha richiesto la commutazione dell'identità utente, ma prima che si verifichi l'opzione.<br/> |
| [**SwitchIdentities**](iidentitychangenotify-switchidentities.md)                     | Deprecato. Chiamato quando le identità utente sono cambiate.<br/>                                                                      |



 

## <a name="remarks"></a>Commenti

Per implementare le notifiche, un'interfaccia derivata deve connettersi a [**IUserIdentityManager**](iuseridentitymanager.md) chiamando [**IConnectionPoint:: Advise**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) e passando un puntatore all'interfaccia.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msoe.dll</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IUserIdentityManager**](iuseridentitymanager.md)
</dt> <dt>

[**IConnectionPoint**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpoint)
</dt> </dl>

 

 

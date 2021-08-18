---
description: Deprecato. Fornisce la notifica delle modifiche alle identità utente nel sistema, nonché le richieste utente di cambiare l'identità utente corrente.
ms.assetid: 09903aa6-62bf-4820-9a09-79956d775441
title: Interfaccia IIdentityChangeNotify (Msident.h)
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
ms.openlocfilehash: 4419f55b2fe4561a22035d962da5e3c271108d06fa417cfbed1b603c883e5b32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118721909"
---
# <a name="iidentitychangenotify-interface"></a>Interfaccia IIdentityChangeNotify

\[**L'interfaccia IIdentityChangeNotify** è disponibile per l'uso in Windows 2000. In Windows XP questa funzionalità è stata sostituita dagli account utente con cambio utente rapido e [Desktop remoto](fastuserswitching.md)e potrebbe essere modificata o non disponibile nelle versioni successive.\]

Deprecato. Fornisce la notifica delle modifiche alle identità utente nel sistema, nonché le richieste utente di cambiare l'identità utente corrente.

## <a name="members"></a>Membri

**L'interfaccia IIdentityChangeNotify** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IIdentityChangeNotify** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IIdentityChangeNotify** include questi metodi.



| Metodo                                                                                 | Descrizione                                                                                                                           |
|:---------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------|
| [**IdentityInformationChanged**](iidentitychangenotify-identityinformationchanged.md) | Deprecato. Chiamato quando le informazioni su un'identità utente vengono modificate o quando un'identità utente è stata aggiunta o eliminata.<br/>  |
| [**QuerySwitchIdentities**](iidentitychangenotify-queryswitchidentities.md)           | Deprecato. Chiamato quando l'utente corrente ha richiesto il cambio di identità dell'utente, ma prima che si verifichi il cambio.<br/> |
| [**SwitchIdentities**](iidentitychangenotify-switchidentities.md)                     | Deprecato. Chiamato quando le identità utente vengono cambiate.<br/>                                                                      |



 

## <a name="remarks"></a>Commenti

Per implementare le notifiche, un'interfaccia derivata deve connettersi a [**IUserIdentityManager**](iuseridentitymanager.md) chiamando [**IConnectionPoint::Advise e**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) passando un puntatore all'interfaccia .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Msident.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msident.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msoe.dll</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IUserIdentityManager**](iuseridentitymanager.md)
</dt> <dt>

[**IConnectionPoint**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpoint)
</dt> </dl>

 

 

---
description: IUserIdentityManager non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli account utente con cambio rapido utente e Desktop remoto.
ms.assetid: 3d24b858-bbaf-455c-83cd-3f6f93aba2a8
title: Interfaccia IUserIdentityManager (Msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: d0d00399e0ba958ef63c5e6597eb4a34387f92f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878426"
---
# <a name="iuseridentitymanager-interface"></a>Interfaccia IUserIdentityManager

\[**IUserIdentityManager** non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli [account utente con cambio rapido utente e desktop remoto](fastuserswitching.md).\]

Espone metodi che identificano, enumerano e gestiscono le identità utente nel sistema.

## <a name="members"></a>Membri

L'interfaccia **IUserIdentityManager** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IUserIdentityManager** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IUserIdentityManager** dispone di questi metodi.



| Metodo                                                                  | Descrizione                                                                                                                                                             |
|:------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumIdentities**](iuseridentitymanager-enumidentities.md)           | Deprecato. Ottiene un oggetto [**IEnumUserIdentity**](ienumuseridentity.md) che può essere utilizzato per enumerare le identità utente presenti nel sistema.<br/> |
| [**GetIdentityByCookie**](iuseridentitymanager-getidentitybycookie.md) | Deprecato. Ottiene un'identità utente specifica dal cookie usato per identificarla in modo univoco.<br/>                                                                        |
| [**Disconnessione**](iuseridentitymanager-logoff.md)                           | Deprecato. Disconnettere l'identità corrente.<br/>                                                                                                                    |
| [**Accesso**](iuseridentitymanager-logon.md)                             | Deprecato. Visualizza un'interfaccia utente per l'utente, consentendo all'utente di scegliere un'identità utente. Se l'esito è positivo, l'identità utente verrà registrata e recuperata.<br/>        |
| [**ManageIdentities**](iuseridentitymanager-manageidentities.md)       | Deprecato. Visualizza un'interfaccia utente per l'utente, consentendo all'utente di gestire le identità utente.<br/>                                                                          |



 

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

[**IUserIdentity**](iuseridentity.md)
</dt> <dt>

[**IUserIdentity2**](iuseridentity2.md)
</dt> <dt>

[**IEnumUserIdentity**](ienumuseridentity.md)
</dt> <dt>

[**IIdentityChangeNotify**](iidentitychangenotify.md)
</dt> </dl>

 

 

---
description: IUserIdentity non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli account utente con cambio rapido utente e Desktop remoto.
ms.assetid: c2f11f8b-f944-445b-b4fc-ac57b0fe3a74
title: Interfaccia IUserIdentity (Msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 068d806086aff44db172a4a7b09f55b600204478
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979482"
---
# <a name="iuseridentity-interface"></a>Interfaccia IUserIdentity

\[**IUserIdentity** non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli [account utente con cambio rapido utente e desktop remoto](fastuserswitching.md).\]

Espone i metodi che forniscono i dati di identificazione, registro di sistema e cartella per un'identità utente specifica.

## <a name="members"></a>Membri

L'interfaccia **IUserIdentity** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IUserIdentity** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IUserIdentity** dispone di questi metodi.



| Metodo                                                         | Descrizione                                                                                      |
|:---------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**GetCookie**](iuseridentity-getcookie.md)                   | Deprecato. Ottiene il cookie utilizzato per identificare in modo univoco l'identità dell'utente.<br/>             |
| [**GetIdentityFolder**](iuseridentity-getidentityfolder.md)   | Deprecato. Ottiene la cartella di file associata a questa identità.<br/>                       |
| [**GetName**](iuseridentity-getname.md)                       | Deprecato. Ottiene il nome associato a questa identità utente.<br/>                         |
| [**OpenIdentityRegKey**](iuseridentity-openidentityregkey.md) | Deprecato. Recupera la chiave nel registro di sistema che corrisponde a questa identità utente.<br/> |



 

## <a name="remarks"></a>Commenti

Questa interfaccia fornisce informazioni che corrispondono a una specifica identità utente presente nel sistema. È possibile accedere alla cartella Identity dell'identità utente, alla relativa chiave del registro di sistema e al relativo cookie di identificazione, nonché recuperare il nome associato all'identità utente.

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

[**IUserIdentity2**](iuseridentity2.md)
</dt> <dt>

[**IUserIdentityManager**](iuseridentitymanager.md)
</dt> <dt>

[**IEnumUserIdentity**](ienumuseridentity.md)
</dt> </dl>

 

 

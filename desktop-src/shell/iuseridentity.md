---
description: IUserIdentity non è supportato e potrebbe essere modificato o non disponibile in futuro. Usare invece gli account utente con cambio utente rapido e Desktop remoto.
ms.assetid: c2f11f8b-f944-445b-b4fc-ac57b0fe3a74
title: Interfaccia IUserIdentity (Msident.h)
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
ms.openlocfilehash: f7e721f60198791e530300d5181abaa84e96c1a04f285972314ab866dd86215f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713781"
---
# <a name="iuseridentity-interface"></a>Interfaccia IUserIdentity

\[**IUserIdentity** non è supportato e potrebbe essere modificato o non disponibile in futuro. Usare invece gli [account utente con cambio utente rapido e Desktop remoto](fastuserswitching.md).\]

Espone metodi che forniscono dati di identificazione, registro e cartella per un'identità utente specifica.

## <a name="members"></a>Membri

**L'interfaccia IUserIdentity** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IUserIdentity** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IUserIdentity** include questi metodi.



| Metodo                                                         | Descrizione                                                                                      |
|:---------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**GetCookie**](iuseridentity-getcookie.md)                   | Deprecato. Ottiene il cookie utilizzato per identificare in modo univoco questa identità utente.<br/>             |
| [**GetIdentityFolder**](iuseridentity-getidentityfolder.md)   | Deprecato. Ottiene la cartella di file associata a questa identità.<br/>                       |
| [**GetName**](iuseridentity-getname.md)                       | Deprecato. Ottiene il nome associato a questa identità utente.<br/>                         |
| [**OpenIdentityRegKey**](iuseridentity-openidentityregkey.md) | Deprecato. Recupera la chiave nel Registro di sistema che corrisponde a questa identità utente.<br/> |



 

## <a name="remarks"></a>Commenti

Questa interfaccia fornisce informazioni che corrispondono a un'identità utente specifica presente nel sistema. È possibile accedere alla cartella dell'identità dell'utente, alla relativa chiave del Registro di sistema e al cookie di identificazione, nonché recuperare il nome associato all'identità utente.

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

[**IUserIdentity2**](iuseridentity2.md)
</dt> <dt>

[**IUserIdentityManager**](iuseridentitymanager.md)
</dt> <dt>

[**IEnumUserIdentity**](ienumuseridentity.md)
</dt> </dl>

 

 

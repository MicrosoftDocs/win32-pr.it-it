---
description: IUserIdentity2 non è supportato e potrebbe essere modificato o non disponibile in futuro. Usare invece gli account utente con cambio utente rapido e Desktop remoto.
ms.assetid: 85238574-f6bf-43d7-a41b-3ea086c45e07
title: Interfaccia IUserIdentity2 (Msident.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: a1a23ea6e0d5832ee6d78453f3a246b9db749c0d7b24b90a2199a7e8cfd225b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118720587"
---
# <a name="iuseridentity2-interface"></a>Interfaccia IUserIdentity2

\[**IUserIdentity2** non è supportato e potrebbe essere modificato o non disponibile in futuro. Usare invece gli [account utente con cambio utente rapido e Desktop remoto](fastuserswitching.md).\]

Espone metodi che forniscono la denominazione, la password e il controllo ordinale per un'identità utente specifica.

## <a name="members"></a>Membri

**L'interfaccia IUserIdentity2** eredita da [**IUserIdentity.**](iuseridentity.md) **IUserIdentity2** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IUserIdentity2** include questi metodi.



| Metodo                                                  | Descrizione                                                       |
|:--------------------------------------------------------|:------------------------------------------------------------------|
| [**ChangePassword**](iuseridentity2-changepassword.md) | Deprecato. Imposta una nuova password per l'identità.<br/>      |
| [**GetOrdinal**](iuseridentity2-getordinal.md)         | Deprecato. Ottiene il numero ordinale per questa identità.<br/> |
| [**SetName**](iuseridentity2-setname.md)               | Deprecato. Imposta il nome visualizzato dell'identità.<br/>     |



 

## <a name="remarks"></a>Commenti

Questa interfaccia fornisce anche i metodi [**dell'interfaccia IUserIdentity,**](iuseridentity.md) da cui eredita.

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

[**IUserIdentity**](iuseridentity.md)
</dt> </dl>

 

 





---
description: IUserIdentity2 non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli account utente con cambio rapido utente e Desktop remoto.
ms.assetid: 85238574-f6bf-43d7-a41b-3ea086c45e07
title: Interfaccia IUserIdentity2 (Msident. h)
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
ms.openlocfilehash: 88142e462566a6afaf299096744a0b8f9ea83dfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524442"
---
# <a name="iuseridentity2-interface"></a>Interfaccia IUserIdentity2

\[**IUserIdentity2** non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli [account utente con cambio rapido utente e desktop remoto](fastuserswitching.md).\]

Espone metodi che forniscono la denominazione, la password e il controllo ordinale per un'identità utente specifica.

## <a name="members"></a>Membri

L'interfaccia **IUserIdentity2** eredita da [**IUserIdentity**](iuseridentity.md). **IUserIdentity2** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IUserIdentity2** dispone di questi metodi.



| Metodo                                                  | Descrizione                                                       |
|:--------------------------------------------------------|:------------------------------------------------------------------|
| [**ChangePassword**](iuseridentity2-changepassword.md) | Deprecato. Imposta una nuova password per l'identità.<br/>      |
| [**GetOrdinal**](iuseridentity2-getordinal.md)         | Deprecato. Ottiene il numero ordinale per l'identità.<br/> |
| [**SetName**](iuseridentity2-setname.md)               | Deprecato. Imposta il nome visualizzato dell'identità.<br/>     |



 

## <a name="remarks"></a>Commenti

Questa interfaccia fornisce anche i metodi dell'interfaccia [**IUserIdentity**](iuseridentity.md) , da cui eredita.

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
</dt> </dl>

 

 





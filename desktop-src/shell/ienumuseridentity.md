---
description: IEnumUserIdentity non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli account utente con cambio rapido utente e Desktop remoto.
ms.assetid: df4b6235-e66a-4187-b1f9-33c042cae2f2
title: Interfaccia IEnumUserIdentity (Msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 48abf182942f90ecd477a241be3bf45323bdbdf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979503"
---
# <a name="ienumuseridentity-interface"></a>Interfaccia IEnumUserIdentity

\[**IEnumUserIdentity** non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli [account utente con cambio rapido utente e desktop remoto](fastuserswitching.md).\]

Fornisce l'enumerazione di tutte le identità utente presenti nel sistema.

## <a name="members"></a>Membri

L'interfaccia **IEnumUserIdentity** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IEnumUserIdentity** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IEnumUserIdentity** dispone di questi metodi.



| Metodo                                         | Descrizione                                                                                                                  |
|:-----------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [**Clone**](ienumuseridentity-clone.md)       | Deprecato. Ottiene una copia dell'enumerazione corrente.<br/>                                                               |
| [**GetCount**](ienumuseridentity-getcount.md) | Deprecato. Ottiene il numero di identità utente attualmente presenti nel sistema.<br/>                                            |
| [**Avanti**](ienumuseridentity-next.md)         | Deprecato. Recupera una matrice di interfacce di identità utente dall'enumerazione.<br/>                                  |
| [**Reset**](ienumuseridentity-reset.md)       | Deprecato. Reimposta il numero interno di interfacce recuperate nell'enumerazione.<br/>                                 |
| [**Ignora**](ienumuseridentity-skip.md)         | Deprecato. Ignora un determinato numero di interfacce di identità utente nell'enumerazione. Utilizzato durante il recupero delle interfacce.<br/> |



 

## <a name="remarks"></a>Commenti

Per recuperare informazioni sulle identità utente presenti nel sistema, è possibile usare questa interfaccia. Da un'interfaccia [**IUserIdentityManager**](iuseridentitymanager.md) è possibile chiamare [**IUserIdentityManager:: EnumIdentities**](iuseridentitymanager-enumidentities.md) per recuperare questa interfaccia.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                   |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                  |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                         |
| Intestazione<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IUserIdentityManager**](iuseridentitymanager.md)
</dt> </dl>

 

 

---
description: Rappresenta il servizio di sicurezza. Viene usato per configurare le impostazioni di sicurezza del sistema virtuale.
ms.assetid: 00097d81-9fea-4b84-b5dd-e45af46d6e0a
title: Msvm_SecurityService classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 32596a46abaa6d745223ab01f8da734e167909f01621deef85f0b21ddfc0b99e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118146896"
---
# <a name="msvm_securityservice-class"></a>Classe \_ Msvm SecurityService

Rappresenta il servizio di sicurezza. Viene usato per configurare le impostazioni di sicurezza del sistema virtuale.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SecurityService : CIM_Service
{
};
```

## <a name="members"></a>Members

La **classe Msvm \_ SecurityService** ha questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

La **classe Msvm \_ SecurityService** include questi metodi.



| Metodo                                                                                            | Descrizione                                                             |
|:--------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [**GetKeyProtector**](msvm-securityservice-getkeyprotector.md)                                   | Metodo per recuperare la protezione della chiave per un sistema virtuale.<br/>   |
| [**ModifySecuritySettings**](msvm-securityservice-modifysecuritysettings.md)                     | Modifica le impostazioni di sicurezza correnti di una macchina virtuale.<br/> |
| [**RestoreLastKnownGoodKeyProtector**](msvm-securityservice-restorelastknowngoodkeyprotector.md) | Metodo per ripristinare l'ultima protezione con chiave buona nota.<br/> |
| [**SetKeyProtector**](msvm-securityservice-setkeyprotector.md)                                   | Metodo per impostare la protezione della chiave per un sistema virtuale.<br/>        |
| [**SetSecurityPolicy**](msvm-securityservice-setsecuritypolicy.md)                               | Metodo per impostare la protezione della chiave per un sistema virtuale.<br/>        |
| [**Startservice**](msvm-securityservice-startservice.md)                                         | avvia il servizio.<br/>                                          |
| [**StopService**](msvm-securityservice-stopservice.md)                                           | arresta il servizio.<br/>                                           |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1703 \[\]<br/>                                               |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Servizio \_ CIM**](cim-service.md)
</dt> </dl>

 

 





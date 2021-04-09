---
description: Rappresenta il servizio di sicurezza. Viene usato per configurare le impostazioni di sicurezza del sistema virtuale.
ms.assetid: 00097d81-9fea-4b84-b5dd-e45af46d6e0a
title: Classe Msvm_SecurityService
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
ms.openlocfilehash: cc7b15af3d3033487464fe7b29a93dc649ffbd62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967629"
---
# <a name="msvm_securityservice-class"></a>\_Classe MSVM SecurityService

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

La **classe \_ SecurityService di MSVM** dispone di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

La **classe \_ SecurityService di MSVM** dispone di questi metodi.



| Metodo                                                                                            | Descrizione                                                             |
|:--------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [**GetKeyProtector**](msvm-securityservice-getkeyprotector.md)                                   | Metodo per recuperare la protezione con chiave per un sistema virtuale.<br/>   |
| [**ModifySecuritySettings**](msvm-securityservice-modifysecuritysettings.md)                     | Modifica le impostazioni di sicurezza correnti di una macchina virtuale.<br/> |
| [**RestoreLastKnownGoodKeyProtector**](msvm-securityservice-restorelastknowngoodkeyprotector.md) | Metodo di ripristino all'ultima protezione con chiave corretta nota.<br/> |
| [**SetKeyProtector**](msvm-securityservice-setkeyprotector.md)                                   | Metodo per impostare la protezione con chiave per un sistema virtuale.<br/>        |
| [**SetSecurityPolicy**](msvm-securityservice-setsecuritypolicy.md)                               | Metodo per impostare la protezione con chiave per un sistema virtuale.<br/>        |
| [**StartService**](msvm-securityservice-startservice.md)                                         | avvia il servizio.<br/>                                          |
| [**StopService**](msvm-securityservice-stopservice.md)                                           | arresta il servizio.<br/>                                           |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1703 \[\]<br/>                                               |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Servizio CIM**](cim-service.md)
</dt> </dl>

 

 





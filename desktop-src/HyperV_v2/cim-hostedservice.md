---
description: Rappresenta un'associazione tra un servizio e il sistema che ospita il servizio. Un sistema può ospitare molti servizi, tuttavia questa classe non rappresenta servizi ospitati in più sistemi.
ms.assetid: ede67a81-cf1b-41aa-b907-5b635cf80423
title: Classe CIM_HostedService (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedService
- CIM_HostedService.Antecedent
- CIM_HostedService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 841c0e26898ed3baa4b4947779a395ee9ce870d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484205"
---
# <a name="cim_hostedservice-class-hyper-v-management"></a>Classe CIM_HostedService (gestione Hyper-V)

Rappresenta un'associazione tra un servizio e il sistema che ospita il servizio. Un sistema può ospitare molti servizi, tuttavia questa classe non rappresenta servizi ospitati in più sistemi.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_HostedService : CIM_HostedDependency
{
  CIM_System  REF Antecedent;
  CIM_Service REF Dependent;
};
```

## <a name="members"></a>Members

La classe **CIM \_ servizio ospitato** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ servizio ospitato** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ sistema CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Sistema di hosting.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ servizio CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente"), [**debole**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Servizio ospitato nel sistema.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_HOSTEDDEPENDENCY CIM**](cim-hosteddependency.md)
</dt> </dl>

 


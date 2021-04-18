---
description: Rappresenta un'associazione tra un servizio e un punto di accesso al servizio (SAP) che fornisce al servizio funzionalità.
ms.assetid: 9b82fad2-9731-4e0d-bdb0-d1be13ea20fc
title: Classe CIM_ServiceSAPDependency (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceSAPDependency
- CIM_ServiceSAPDependency.Antecedent
- CIM_ServiceSAPDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d49b63dfb37dfddf009f01122f4aa49af316fa58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313863"
---
# <a name="cim_servicesapdependency-class-hyper-v-management"></a>Classe CIM_ServiceSAPDependency (gestione Hyper-V)

Rappresenta un'associazione tra un servizio e un punto di accesso al servizio (SAP) che fornisce al servizio funzionalità.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service")]
class CIM_ServiceSAPDependency : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Antecedent;
  CIM_Service            REF Dependent;
};
```

## <a name="members"></a>Members

La classe **CIM \_ ServiceSAPDependency** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ ServiceSAPDependency** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ serviceAccessPoint**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

Il punto di accesso al servizio richiesto.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ servizio CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")
</dt> </dl>

Il servizio che dipende da SAP.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1<br/>                                                                                  |
| Server minimo supportato<br/> | Windows Server 2012 R2<br/>                                                                       |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Dipendenza CIM**](cim-dependency.md)
</dt> </dl>

 


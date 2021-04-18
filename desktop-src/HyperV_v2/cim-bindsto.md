---
description: Rappresenta un'associazione in cui un \_ oggetto CIM serviceAccessPoint richiede servizi di protocollo da un \_ oggetto CIM ProtocolEndpoint.
ms.assetid: d1ef774d-f0e0-43e7-8a9d-63c2fad5ca4a
title: Classe CIM_BindsTo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BindsTo
- CIM_BindsTo.Antecedent
- CIM_BindsTo.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ae32bd10d1e7d1944519fe8fb039453989c165fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313868"
---
# <a name="cim_bindsto-class"></a>CIM \_ BindsTo (classe)

Rappresenta un'associazione in cui un oggetto [**CIM \_ serviceAccessPoint**](cim-serviceaccesspoint.md) richiede servizi di protocollo da un oggetto [**CIM \_ ProtocolEndpoint**](cim-protocolendpoint.md) .

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_BindsTo : CIM_SAPSAPDependency
{
  CIM_ProtocolEndpoint   REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a>Members

La classe **CIM \_ BindsTo** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ BindsTo** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ProtocolEndpoint**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

Endpoint di livello inferiore a cui si accede dal punto di accesso al servizio.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ serviceAccessPoint**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")
</dt> </dl>

Endpoint del protocollo o del punto di accesso dipendente dall'endpoint di livello inferiore.

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

[**\_SAPSAPDEPENDENCY CIM**](cim-sapsapdependency.md)
</dt> </dl>

 


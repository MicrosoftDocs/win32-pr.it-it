---
description: Rappresenta un'associazione in cui un oggetto ServiceAccessPoint CIM richiede servizi \_ di protocollo da un oggetto \_ ProtocolEndpoint CIM.
ms.assetid: d1ef774d-f0e0-43e7-8a9d-63c2fad5ca4a
title: CIM_BindsTo classe
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
ms.openlocfilehash: b0b2dc2f767ad409cece300fc33ecde0e6a0d2f55ce659ea9d77fe332f3529a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813422"
---
# <a name="cim_bindsto-class"></a>Classe \_ CiM BindsTo

Rappresenta un'associazione in cui [**un oggetto \_ ServiceAccessPoint CIM**](cim-serviceaccesspoint.md) richiede servizi di protocollo da un [**oggetto \_ ProtocolEndpoint CIM.**](cim-protocolendpoint.md)

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

La **classe \_ CIM BindsTo** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ BindsTo** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **Protocollo \_ CIMEndpoint**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Endpoint di livello inferiore a cui accede il punto di accesso del servizio.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **\_ CIM ServiceAccessPoint**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dipendente")
</dt> </dl>

Punto di accesso o endpoint del protocollo che dipende dall'endpoint di livello inferiore.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ SAPSAPDependency**](cim-sapsapdependency.md)
</dt> </dl>

 


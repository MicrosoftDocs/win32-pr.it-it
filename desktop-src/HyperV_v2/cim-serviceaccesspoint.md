---
description: Rappresenta un punto di accesso del servizio (SAP), in grado di utilizzare o richiamare un servizio. I punti di accesso condiviso indicano che un servizio è disponibile per l'uso da parte di altre entità.
ms.assetid: 09349c95-3f7e-46c5-bea1-c3d14ee16a2a
title: CIM_ServiceAccessPoint classe (gestione di Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceAccessPoint
- CIM_ServiceAccessPoint.SystemCreationClassName
- CIM_ServiceAccessPoint.SystemName
- CIM_ServiceAccessPoint.CreationClassName
- CIM_ServiceAccessPoint.Name
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: aad557ed5ec13e56a53912a44b11a69a69febf118bb3c2bf9aa68971cfd88de0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118647557"
---
# <a name="cim_serviceaccesspoint-class-hyper-v-management"></a>CIM_ServiceAccessPoint classe (gestione di Hyper-V)

Rappresenta un punto di accesso del servizio (SAP), in grado di utilizzare o richiamare un servizio. I punti di accesso condiviso indicano che un servizio è disponibile per l'uso da parte di altre entità.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_ServiceAccessPoint : CIM_EnabledLogicalElement
{
  string SystemCreationClassName;
  string SystemName;
  string CreationClassName;
  string Name;
};
```

## <a name="members"></a>Members

La **classe \_ CiM ServiceAccessPoint** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ CiM ServiceAccessPoint** ha queste proprietà.

<dl> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key,**](/windows/desktop/WmiSdk/key-qualifier) [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nome della classe utilizzato per creare un'istanza di questa classe. **CreationClassName viene** combinato con altre proprietà chiave di questa classe per identificare in modo univoco le istanze di questa classe e le relative sottoclassi.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key,**](/windows/desktop/WmiSdk/key-qualifier) [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nome univoco di SAP che indica le funzionalità supportate da SAP.

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key,**](/windows/desktop/WmiSdk/key-qualifier) [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**")
</dt> </dl>

Nome della classe usato per creare un'istanza del sistema che contiene SAP. **SystemCreationClassName viene** combinato con altre proprietà chiave di questa classe per identificare in modo univoco le istanze di questa classe e le relative sottoclassi.

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key,**](/windows/desktop/WmiSdk/key-qualifier) [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Nome**")
</dt> </dl>

Nome del sistema che contiene SAP.

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

[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md)
</dt> </dl>

 


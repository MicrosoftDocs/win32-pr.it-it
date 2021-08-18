---
description: Rappresenta un'associazione tra un punto di accesso del servizio (SAP) e il sistema che lo ospita.
ms.assetid: 82db71d6-6d14-408e-87e0-fe869e454d4d
title: CIM_HostedAccessPoint classe (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedAccessPoint
- CIM_HostedAccessPoint.Antecedent
- CIM_HostedAccessPoint.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2079d34af64b7819f7c7dc4991a00a9a01b350ee45c54b910a35f1008d45e510
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014629"
---
# <a name="cim_hostedaccesspoint-class-hyper-v-management"></a>CIM_HostedAccessPoint classe (gestione Hyper-V)

Rappresenta un'associazione tra un punto di accesso del servizio (SAP) e il sistema che lo ospita. Un sistema può ospitare più punti di accesso. Se l'implementazione di SAP è modellata, deve essere implementata da un dispositivo o da una funzionalità software che fa parte del sistema che ospita SAP.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service")]
class CIM_HostedAccessPoint : CIM_HostedDependency
{
  CIM_System             REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a>Members

La **classe CIM \_ HostedAccessPoint** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ HostedAccessPoint** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **SISTEMA CIM \_**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Sistema di hosting.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ServiceAccessPoint**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

SaP ospitati nel sistema.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1<br/>                                                                                  |
| Server minimo supportato<br/> | R2 per Windows Server 2012<br/>                                                                       |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ HostedDependency**](cim-hosteddependency.md)
</dt> </dl>

 


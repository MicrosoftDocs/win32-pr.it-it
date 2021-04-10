---
description: La \_ classe CIM HostedAccessPoint rappresenta un'associazione tra un punto di accesso al servizio (SAP) e il sistema in cui viene fornito. Ogni sistema può ospitare molti SAP.
ms.assetid: 7da9b781-a5cb-42f5-b03c-4fc818c94e88
ms.tgt_platform: multiple
title: Classe CIM_HostedAccessPoint (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedAccessPoint
- CIM_HostedAccessPoint.Dependent
- CIM_HostedAccessPoint.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d451cec7ad42fa519b70c576fbd02a32d0289e8b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126974"
---
# <a name="cim_hostedaccesspoint-class-cimwin32-wmi-providers"></a>Classe CIM_HostedAccessPoint (provider WMI CIMWin32)

La classe **CIM \_ HostedAccessPoint** rappresenta un'associazione tra un punto di accesso al servizio (SAP) e il sistema in cui viene fornito. Ogni sistema può ospitare molti SAP.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{576C3C56-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedAccessPoint : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_System             REF Antecedent;
};
```

## <a name="members"></a>Members

La classe **CIM \_ HostedAccessPoint** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ HostedAccessPoint** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ sistema CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

[**\_ Sistema CIM**](cim-system.md) che descrive il sistema host.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ serviceAccessPoint**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente"), [**debole**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Un [**\_ serviceAccessPoint CIM**](cim-serviceaccesspoint.md) che descrive i SAP ospitati in questo sistema.

</dd> </dl>

## <a name="remarks"></a>Commenti

**CIM \_ HostedAccessPoint** è derivato dalla [**\_ dipendenza CIM**](cim-dependency.md).

WMI non implementa questa classe.

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Dipendenza CIM**](cim-dependency.md)
</dt> </dl>

 


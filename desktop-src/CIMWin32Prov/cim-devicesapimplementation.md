---
description: La \_ classe CIM DeviceSAPImplementation rappresenta un'associazione tra un punto di accesso al servizio (SAP) e il modo in cui viene implementato.
ms.assetid: 6c059507-bfc0-4630-9b39-9c4bae2bf138
ms.tgt_platform: multiple
title: Classe CIM_DeviceSAPImplementation (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceSAPImplementation
- CIM_DeviceSAPImplementation.Dependent
- CIM_DeviceSAPImplementation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: eadc1e42427c06717c7b0d7a13aba8a2a71ccddb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748698"
---
# <a name="cim_devicesapimplementation-class-cimwin32-wmi-providers"></a>Classe CIM_DeviceSAPImplementation (provider WMI CIMWin32)

La classe **CIM \_ DeviceSAPImplementation** rappresenta un'associazione tra un punto di accesso al servizio (SAP) e il modo in cui viene implementato. Quando molti dispositivi logici sono associati a un SAP, gli elementi operano insieme per fornire il punto di accesso. Se esistono implementazioni diverse di un SAP, ogni implementazione genera singole creazioni di istanze dell'oggetto SAP.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[UUID("{1BE949DA-DB36-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_DeviceSAPImplementation : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_LogicalDevice      REF Antecedent;
};
```

## <a name="members"></a>Members

La classe **CIM \_ DeviceSAPImplementation** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ DeviceSAPImplementation** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ LogicalDevice**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

Un [**\_ LogicalDevice CIM**](cim-logicaldevice.md) che descrive il dispositivo logico.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ serviceAccessPoint**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")
</dt> </dl>

Un [**\_ serviceAccessPoint CIM**](cim-serviceaccesspoint.md) che descrive il punto di accesso al servizio implementato usando il dispositivo logico.

</dd> </dl>

## <a name="remarks"></a>Commenti

WMI non implementa questa classe.

La classe **CIM \_ DeviceSAPImplementation** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).

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

 


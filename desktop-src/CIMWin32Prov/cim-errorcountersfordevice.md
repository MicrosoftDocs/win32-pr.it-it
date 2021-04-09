---
description: La \_ classe CIM ErrorCountersForDevice associa la \_ classe CIM DeviceErrorCounts al dispositivo logico a cui si applica.
ms.assetid: 200971ab-df85-4a45-beb3-4ffe11ce92dc
ms.tgt_platform: multiple
title: Classe CIM_ErrorCountersForDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ErrorCountersForDevice
- CIM_ErrorCountersForDevice.Element
- CIM_ErrorCountersForDevice.Stats
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7c4e11b1f58cae7b544b251044657bb737525b37
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877909"
---
# <a name="cim_errorcountersfordevice-class"></a>CIM \_ ErrorCountersForDevice (classe)

La classe **CIM \_ ErrorCountersForDevice** associa la classe [**CIM \_ DeviceErrorCounts**](cim-deviceerrorcounts.md) al dispositivo logico a cui si applica.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{2D79F3A0-D025-11d2-85F5-0000F8102E5F}"), AMENDMENT]
class CIM_ErrorCountersForDevice : CIM_Statistics
{
  CIM_LogicalDevice     REF Element;
  CIM_DeviceErrorCounts REF Stats;
};
```

## <a name="members"></a>Members

La classe **CIM \_ ErrorCountersForDevice** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ ErrorCountersForDevice** dispone di queste proprietà.

<dl> <dt>

**elemento**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ LogicalDevice**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("element"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Un [**\_ LogicalDevice CIM**](cim-logicaldevice.md) che descrive il dispositivo a cui si applicano i contatori degli errori.

</dd> <dt>

**Statistiche**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ DeviceErrorCounts**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("stats"), [**debole**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Un [**\_ DeviceErrorCounts CIM**](cim-deviceerrorcounts.md) che descrive l'oggetto statistico, in questo caso la classe del contatore degli errori.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **CIM \_ ErrorCountersForDevice** viene ereditata [**dalle \_ statistiche CIM**](cim-statistics.md).

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

[**\_Statistiche CIM**](cim-statistics.md)
</dt> </dl>

 


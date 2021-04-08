---
description: La \_ classe CIM DeviceErrorCounts è una classe statistica che contiene contatori correlati agli errori per un dispositivo logico. I tipi di errore sono definiti da CCITT (REC X. 733) e ISO (IEC 10164-4).
ms.assetid: d65cbc78-40f2-4846-bd47-76e04b2f588b
ms.tgt_platform: multiple
title: Classe CIM_DeviceErrorCounts
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceErrorCounts
- CIM_DeviceErrorCounts.Caption
- CIM_DeviceErrorCounts.Description
- CIM_DeviceErrorCounts.CriticalErrorCount
- CIM_DeviceErrorCounts.DeviceCreationClassName
- CIM_DeviceErrorCounts.DeviceID
- CIM_DeviceErrorCounts.Name
- CIM_DeviceErrorCounts.IndeterminateErrorCount
- CIM_DeviceErrorCounts.MajorErrorCount
- CIM_DeviceErrorCounts.MinorErrorCount
- CIM_DeviceErrorCounts.SystemCreationClassName
- CIM_DeviceErrorCounts.SystemName
- CIM_DeviceErrorCounts.WarningCount
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1602e68b7254811ba8c09726feda8baa7bf23d29
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966231"
---
# <a name="cim_deviceerrorcounts-class"></a>CIM \_ DeviceErrorCounts (classe)

La classe **CIM \_ DeviceErrorCounts** è una classe statistica che contiene contatori correlati agli errori per un dispositivo logico. I tipi di errore sono definiti da CCITT (REC X. 733) e ISO (IEC 10164-4).

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{117FDB8C-D025-11d2-85F5-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceErrorCounts : CIM_StatisticalInformation
{
  string Caption;
  string Description;
  uint64 CriticalErrorCount;
  string DeviceCreationClassName;
  string DeviceID;
  string Name;
  uint64 IndeterminateErrorCount;
  uint64 MajorErrorCount;
  uint64 MinorErrorCount;
  string SystemCreationClassName;
  string SystemName;
  uint64 WarningCount;
};
```

## <a name="members"></a>Members

La classe **CIM \_ DeviceErrorCounts** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **CIM \_ DeviceErrorCounts** presenta questi metodi.



| Metodo                                                                     | Descrizione                                                               |
|:---------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [**ResetCounter**](resetcounter-method-in-class-cim-deviceerrorcounts.md) | Reimposta i contatori degli errori e degli avvisi. Non implementato da WMI.<br/> |



 

### <a name="properties"></a>Proprietà

La classe **CIM \_ DeviceErrorCounts** dispone di queste proprietà.

<dl> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Breve descrizione testuale per la statistica o la metrica.

Questa proprietà viene ereditata da [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).

</dd> <dt>

**CriticalErrorCount**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,7 ")
</dt> </dl>

Conteggio degli errori critici.

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione testuale della statistica o della metrica.

Questa proprietà viene ereditata da [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).

</dd> <dt>

**DeviceCreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagati**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ LogicalDevice**](cim-logicaldevice.md).**CreationClassName**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Proprietà **CreationClassName** del dispositivo di ambito.

</dd> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagati**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ LogicalDevice**](cim-logicaldevice.md).**DeviceID**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Identificatore del dispositivo di ambito.

</dd> <dt>

**IndeterminateErrorCount**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Conteggio degli errori indeterminati.

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**MajorErrorCount**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,8 ")
</dt> </dl>

Conteggio degli errori principali.

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**MinorErrorCount**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Conteggio degli errori secondari.

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

La proprietà nome ereditato funge da parte della chiave per l'istanza **di \_ DeviceErrorCounts CIM** . L'ambito dell'oggetto è costituito dal dispositivo logico a cui si applicano le statistiche.

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagati**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ LogicalDevice**](cim-logicaldevice.md).**SystemCreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

**CreationClassName** del sistema di ambito.

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagati**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ LogicalDevice**](cim-logicaldevice.md).**SystemName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Proprietà **Name** del sistema di ambito.

</dd> <dt>

**WarningCount**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,9 ")
</dt> </dl>

Conteggio degli avvisi.

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Commenti

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

[**\_STATISTICALINFORMATION CIM**](cim-statisticalinformation.md)
</dt> </dl>

 


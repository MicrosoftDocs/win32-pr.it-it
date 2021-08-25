---
description: Fornisce informazioni aggiuntive da usare con il metodo CreateSnapshot della classe Msvm \_ VirtualSystemSnapshotService.
ms.assetid: d4a025c4-6a3c-4ae0-8f2c-421c1aa1eb23
title: Msvm_VirtualSystemSnapshotSettingData classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotSettingData
- Msvm_VirtualSystemSnapshotSettingData.ConsistencyLevel
- Msvm_VirtualSystemSnapshotSettingData.IgnoreNonSnapshottableDisks
- Msvm_VirtualSystemSnapshotSettingData.GuestBackupType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d112e4109ed6d0ab899aadf59f0e991f52259eaf2c514c6d9215b04a8cafcab8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046251"
---
# <a name="msvm_virtualsystemsnapshotsettingdata-class"></a>Classe Msvm \_ VirtualSystemSnapshotSettingData

Fornisce informazioni aggiuntive da usare con il [**metodo CreateSnapshot**](cim-virtualsystemsnapshotservice-createsnapshot.md) della [**classe Msvm \_ VirtualSystemSnapshotService.**](msvm-virtualsystemsnapshotservice.md)

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[AMENDMENT]
class Msvm_VirtualSystemSnapshotSettingData : CIM_SettingData
{
  uint8   ConsistencyLevel;
  boolean IgnoreNonSnapshottableDisks;
  uint8   GuestBackupType;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ VirtualSystemSnapshotSettingData** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ VirtualSystemSnapshotSettingData** ha queste proprietà.

<dl> <dt>

**ConsistencyLevel**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Livello di coerenza dello snapshot.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

**Coerente con l'applicazione** (1)


</dt> <dd></dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

**Coerenza arresto anomalo** del sistema (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**GuestBackupType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di backup da usare all'interno del guest.

> [!Note]  
> Proprietà aggiunta in Windows 10, versione 1703

 

<dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

**Non definito** (0)


</dt> <dd></dd> <dt>

<span id="Full"></span><span id="full"></span><span id="FULL"></span>

**Completo** (1)


</dt> <dd></dd> <dt>

<span id="Copy"></span><span id="copy"></span><span id="COPY"></span>

**Copia** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**IgnoreNonSnapshottableDisks**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se i dischi non snapshottable, ad esempio i dischi pass-through e Fibre Channel, devono essere ignorati durante la creazione dello snapshot.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> </dl>

 

 





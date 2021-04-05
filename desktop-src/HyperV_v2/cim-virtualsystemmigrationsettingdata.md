---
description: Definisce le impostazioni per la migrazione del sistema virtuale gestita da un'istanza della classe CIM \_ VirtualSystemMigrationService.
ms.assetid: c28ed48b-bacc-49c8-9131-2543c0edb3fd
title: Classe CIM_VirtualSystemMigrationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationSettingData
- CIM_VirtualSystemMigrationSettingData.MigrationType
- CIM_VirtualSystemMigrationSettingData.Priority
- CIM_VirtualSystemMigrationSettingData.Bandwidth
- CIM_VirtualSystemMigrationSettingData.BandwidthUnit
- CIM_VirtualSystemMigrationSettingData.OtherTransportType
- CIM_VirtualSystemMigrationSettingData.TransportType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0d33479d0148bc4004fbbbda216e508c276c7ee9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756272"
---
# <a name="cim_virtualsystemmigrationsettingdata-class"></a>CIM \_ VirtualSystemMigrationSettingData (classe)

Definisce le impostazioni per la migrazione del sistema virtuale gestita da un'istanza della classe [**CIM \_ VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) .

## <a name="syntax"></a>Sintassi

``` syntax
[Experimental, Abstract, Version("2.20.0"), UMLPackagePath("CIM::System::Virtualization"), AMENDMENT]
class CIM_VirtualSystemMigrationSettingData : CIM_SettingData
{
  uint16 MigrationType;
  uint16 Priority;
  uint16 Bandwidth;
  string BandwidthUnit;
  string OtherTransportType;
  uint16 TransportType;
};
```

## <a name="members"></a>Members

La classe **CIM \_ VirtualSystemMigrationSettingData** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ VirtualSystemMigrationSettingData** dispone di queste proprietà.

<dl> <dt>

**Larghezza di banda**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**misuratore**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ CIM VirtualSystemMigrationSettingData**.**BandwidthUnit**")
</dt> </dl>

Larghezza di banda assegnata o richiesta per un'operazione di migrazione del sistema virtuale. "0" è la larghezza di banda predefinita per le richieste di migrazione.

Le proprietà **larghezza di banda** e **priorità** possono essere utilizzate insieme. I processi di migrazione con i valori con la massima **priorità** uguale condividono la larghezza di banda disponibile in base alla larghezza di banda richiesta. Se non viene utilizzata tutta la larghezza di banda da questo set di processi, i processi di migrazione con i successivi valori di **priorità** più bassa condividono la larghezza di banda rimanente. Se rimane una maggiore larghezza di banda, verranno presi in considerazione i processi di migrazione con i valori di **priorità** inferiore uguali.

L'unità utilizzata nella proprietà **Bandwidth** è specificata dal valore della proprietà **BandwidthUnit** .

Se il valore della proprietà **BandwidthUnit** è "percent", si applicano le regole seguenti:

-   Il valore della proprietà della **larghezza di banda** deve essere compreso tra "0" e "100", con valori più elevati che indicano una larghezza di banda maggiore.
-   Il valore "100" indica tutta la larghezza di banda disponibile per l'esecuzione delle operazioni di migrazione del sistema virtuale.
-   I valori compresi tra "1" e "100" sono correlati in modo lineare con l'intervallo della larghezza di banda disponibile. Ad esempio, un valore di 50 richiede metà della larghezza di banda disponibile.

</dd> <dt>

**BandwidthUnit**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VirtualSystemMigrationSettingData**.**Larghezza di banda**"), **IsPUnit**
</dt> </dl>

Unità utilizzata dalla proprietà della **larghezza di banda** . Il valore di questa proprietà deve essere un valore valido del qualificatore unità di codice definito nell'Appendice C. 1 di DSP0004 V 2.4 o versione successiva.

> [!Note]  
> I profili come DMTF DSP1081 definiscono il modo in cui i client possono individuare il set di unità supportate da un'implementazione e gli intervalli e gli incrementi per i valori della proprietà della **larghezza di banda** .

 

</dd> <dt>

**MigrationType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di operazione di migrazione da eseguire.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Live"></span><span id="live"></span><span id="LIVE"></span>

**Live** (2)


</dt> <dd></dd> <dt>

<span id="Resume"></span><span id="resume"></span><span id="RESUME"></span>

**Riprendi** (3)


</dt> <dd></dd> <dt>

<span id="Restart"></span><span id="restart"></span><span id="RESTART"></span>

**Riavvio** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**OtherTransportType**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VirtualSystemMigrationSettingData**.**TransportType**")
</dt> </dl>

Tipo di trasporto da applicare se il valore di **TransportType** è "1" (other).

</dd> <dt>

**Priorità**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Importanza della migrazione relativa che l'implementazione della migrazione del sistema virtuale può utilizzare per ordinare o assegnare preferenza tra più richieste di migrazione in sospeso. Più basso è il valore, maggiore è la priorità. "0" è la larghezza di banda predefinita per le richieste di migrazione.

</dd> <dt>

**TransportType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VirtualSystemMigrationSettingData**.**OtherTransportType**")
</dt> </dl>

Tipo di trasporto da applicare a un'operazione di migrazione del sistema virtuale.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="SSH"></span><span id="ssh"></span>

**SSH** (2)


</dt> <dd></dd> <dt>

<span id="TLS"></span><span id="tls"></span>

**TLS** (3)


</dt> <dd></dd> <dt>

<span id="TLS_Strict"></span><span id="tls_strict"></span><span id="TLS_STRICT"></span>

**TLS Strict** (4)


</dt> <dd></dd> <dt>

<span id="TCP"></span><span id="tcp"></span>

**TCP** (5)


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

**IPC** (6)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF riservato** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fornitore riservato** (32768...)


</dt> <dd></dd> </dl>

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

[**\_SETTINGDATA CIM**](cim-settingdata.md)
</dt> </dl>

 


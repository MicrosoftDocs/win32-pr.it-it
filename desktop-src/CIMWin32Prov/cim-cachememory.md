---
description: La \_ classe CIM CacheMemory definisce le funzionalità e la gestione della memoria cache.
ms.assetid: cdf35122-2057-45fa-818b-ce542d8e82b0
ms.tgt_platform: multiple
title: Classe CIM_CacheMemory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CacheMemory
- CIM_CacheMemory.Caption
- CIM_CacheMemory.Description
- CIM_CacheMemory.InstallDate
- CIM_CacheMemory.Name
- CIM_CacheMemory.Status
- CIM_CacheMemory.Availability
- CIM_CacheMemory.ConfigManagerErrorCode
- CIM_CacheMemory.ConfigManagerUserConfig
- CIM_CacheMemory.CreationClassName
- CIM_CacheMemory.DeviceID
- CIM_CacheMemory.PowerManagementCapabilities
- CIM_CacheMemory.ErrorCleared
- CIM_CacheMemory.ErrorDescription
- CIM_CacheMemory.LastErrorCode
- CIM_CacheMemory.PNPDeviceID
- CIM_CacheMemory.PowerManagementSupported
- CIM_CacheMemory.StatusInfo
- CIM_CacheMemory.SystemCreationClassName
- CIM_CacheMemory.SystemName
- CIM_CacheMemory.Access
- CIM_CacheMemory.BlockSize
- CIM_CacheMemory.NumberOfBlocks
- CIM_CacheMemory.Purpose
- CIM_CacheMemory.ErrorMethodology
- CIM_CacheMemory.AdditionalErrorData
- CIM_CacheMemory.CorrectableError
- CIM_CacheMemory.EndingAddress
- CIM_CacheMemory.ErrorAccess
- CIM_CacheMemory.ErrorAddress
- CIM_CacheMemory.ErrorData
- CIM_CacheMemory.ErrorDataOrder
- CIM_CacheMemory.ErrorInfo
- CIM_CacheMemory.ErrorResolution
- CIM_CacheMemory.ErrorTime
- CIM_CacheMemory.ErrorTransferSize
- CIM_CacheMemory.OtherErrorDescription
- CIM_CacheMemory.StartingAddress
- CIM_CacheMemory.SystemLevelAddress
- CIM_CacheMemory.Associativity
- CIM_CacheMemory.CacheType
- CIM_CacheMemory.FlushTimer
- CIM_CacheMemory.Level
- CIM_CacheMemory.LineSize
- CIM_CacheMemory.ReadPolicy
- CIM_CacheMemory.ReplacementPolicy
- CIM_CacheMemory.WritePolicy
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0b7a7add96c523dae6b683d597ba36953c605d28
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878006"
---
# <a name="cim_cachememory-class"></a>CIM \_ CacheMemory (classe)

La classe **CIM \_ CacheMemory** definisce le funzionalità e la gestione della memoria cache.

Memoria cache è la RAM dedicata o allocata in cui un processore cerca i dati. I dati nella memoria cache vengono recapitati rapidamente al processore e vengono in genere descritti in prossimità del processore, ad esempio la cache primaria o secondaria. Anche un'unità disco che include RAM allocata per contenere i dati letti o adiacenti del disco più recenti (per velocizzare il recupero) viene modellata come memoria della cache.

> [!Note]  
> La memoria cache non è un buffer a livello di sistema operativo o di applicazione. si tratta di una RAM allocata per la memorizzazione nella cache dei dati del processore.

 

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[abstract, UUID("{FAF76B65-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_CacheMemory : CIM_Memory
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint16   Availability;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   DeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint32   LastErrorCode;
  string   PNPDeviceID;
  boolean  PowerManagementSupported;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   Access;
  uint64   BlockSize;
  uint64   NumberOfBlocks;
  string   Purpose;
  string   ErrorMethodology;
  uint8    AdditionalErrorData[];
  boolean  CorrectableError;
  uint64   EndingAddress;
  uint16   ErrorAccess;
  uint64   ErrorAddress;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  uint16   ErrorInfo;
  uint64   ErrorResolution;
  datetime ErrorTime;
  uint32   ErrorTransferSize;
  string   OtherErrorDescription;
  uint64   StartingAddress;
  boolean  SystemLevelAddress;
  uint16   Associativity;
  uint16   CacheType;
  uint32   FlushTimer;
  uint16   Level;
  uint32   LineSize;
  uint16   ReadPolicy;
  uint16   ReplacementPolicy;
  uint16   WritePolicy;
};
```

## <a name="members"></a>Members

La classe **CIM \_ CacheMemory** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **CIM \_ CacheMemory** presenta questi metodi.



| Metodo                                                                 | Descrizione                                                                                                                                |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**Reset**](reset-method-in-class-cim-cachememory.md)                 | Richiede la reimpostazione del dispositivo logico. Non implementato da WMI.<br/>                                                                 |
| [**SetPowerState**](setpowerstate-method-in-class-cim-cachememory.md) | Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando il dispositivo deve essere inserito in tale stato. Non implementato da WMI.<br/> |



 

### <a name="properties"></a>Proprietà

La classe **CIM \_ CacheMemory** dispone di queste proprietà.

<dl> <dt>

**Accesso**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrive le proprietà di lettura/scrittura del supporto.

Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

**Leggibile** (1)


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

**Scrivibile** (2)


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

**Lettura/scrittura supportata** (3)


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

**Scrivi una sola volta** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**AdditionalErrorData**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,18 "," MIF. DMTF \| array di memoria fisica \| 001,13 "), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Matrice di ottetti che contengono informazioni aggiuntive sull'errore. Un esempio è la sindrome di controllo degli errori e correzione (ECC) oppure la restituzione dei bit di controllo se viene utilizzata una metodologia di errore basata su CRC. Nel secondo caso, se viene riconosciuto un errore a bit singolo e l'algoritmo CRC è noto, è possibile determinare il bit esatto che ha avuto esito negativo. In questo campo sono inclusi questo tipo di dati (la sindrome ECC, i dati di controllo o di bit di parità o altre informazioni fornite dal fornitore). Se la proprietà **errorInfo** è uguale a 3 ("OK"), questa proprietà non ha alcun significato.

Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).

</dd> <dt>

**Associatività**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| cache di sistema \| 003,15 ")
</dt> </dl>

Enumerazione che definisce l'associatività della cache di sistema.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (2)


</dt> <dd></dd> <dt>

<span id="Direct_Mapped"></span><span id="direct_mapped"></span><span id="DIRECT_MAPPED"></span>

Con **mapping diretto** (3)


</dt> <dd></dd> <dt>

<span id="2-way_Set-Associative"></span><span id="2-way_set-associative"></span><span id="2-WAY_SET-ASSOCIATIVE"></span>

**set bidirezionale-associativo** (4)


</dt> <dd></dd> <dt>

<span id="4-way_Set-Associative"></span><span id="4-way_set-associative"></span><span id="4-WAY_SET-ASSOCIATIVE"></span>

**set-associativo a 4 vie** (5)


</dt> <dd></dd> <dt>

<span id="Fully_Associative"></span><span id="fully_associative"></span><span id="FULLY_ASSOCIATIVE"></span>

**Completamente associativo** (6)


</dt> <dd></dd> <dt>

<span id="8-way_Set-Associative"></span><span id="8-way_set-associative"></span><span id="8-WAY_SET-ASSOCIATIVE"></span>

**set a 8 vie-associativo** (7)


</dt> <dd></dd> <dt>

<span id="16-way_Set-Associative"></span><span id="16-way_set-associative"></span><span id="16-WAY_SET-ASSOCIATIVE"></span>

**set-associativo a 16 vie** (8)


</dt> <dd></dd> </dl>

</dd> <dt>

**Disponibilità**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")
</dt> </dl>

Disponibilità e stato del dispositivo.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)


</dt> <dd>

Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)


</dt> <dd>

Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)


</dt> <dd>

Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)


</dt> <dd>

Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)


</dt> <dd>

Il dispositivo è sospeso.

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)


</dt> <dd>

Il dispositivo non è pronto.

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)


</dt> <dd>

Il dispositivo non è configurato.

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)


</dt> <dd>

Il dispositivo è silenzioso.

</dd> </dl>

</dd> <dt>

**BlockSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-Resources-MIB. hrStorageAllocationUnits "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")
</dt> </dl>

Dimensioni, in byte, dei blocchi che formano l'extent di archiviazione. Se la dimensione del blocco di variabili è, è necessario specificare la dimensione massima del blocco in byte. Se le dimensioni del blocco sono sconosciute o se un concetto di blocco non è valido, ad esempio per extent di aggregazione, memoria o dischi logici, immettere 1 (uno).

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).

</dd> <dt>

**CacheType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| cache di sistema \| 003,9 ")
</dt> </dl>

Specifica la memorizzazione nella cache delle istruzioni, la memorizzazione dei dati o entrambe. È possibile definire anche "other" e "Unknown".

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (2)


</dt> <dd></dd> <dt>

<span id="Instruction"></span><span id="instruction"></span><span id="INSTRUCTION"></span>

**Istruzione** (3)


</dt> <dd></dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>

**Dati** (4)


</dt> <dd></dd> <dt>

<span id="Unified"></span><span id="unified"></span><span id="UNIFIED"></span>

**Unificato** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Breve descrizione testuale dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**ConfigManagerErrorCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")
</dt> </dl>

Codice di errore Win32 Configuration Manager.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

**Il dispositivo funziona correttamente.**  (0)


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

**Questo dispositivo non è configurato correttamente.** (1)


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

**Windows non è in grado di caricare il driver per questo dispositivo.** (2)


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.** (3)


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.** (4)


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.** (5)


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**  (6)


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

**Impossibile filtrare.** (7)


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

**Il caricatore driver del dispositivo è mancante.** (8)


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.** (9)


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

**Impossibile avviare il dispositivo.** (10)


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

**Errore del dispositivo.** (11)


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.** 12


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

**Windows non è in grado di verificare le risorse del dispositivo.** (13)


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

**Questo dispositivo non funziona correttamente finché non si riavvia il computer.** (14)


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.** (15)


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.** (16)


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

**Il dispositivo richiede un tipo di risorsa sconosciuto.** (17)


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

**Reinstallare i driver per questo dispositivo.** (18)


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

**Errore durante l'utilizzo del caricatore VxD.** (19)


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

**Il registro di sistema potrebbe essere danneggiato.** (20)


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.** (21)


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

**Il dispositivo è disabilitato.** (22)


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.** (23)


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.** (24)


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

**Windows sta ancora impostando questo dispositivo.** (25)


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

**Windows sta ancora impostando questo dispositivo.** (26)


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

**Questo dispositivo non ha una configurazione di log valida.** (27)


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

**I driver per questo dispositivo non sono installati.** (28)


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.** (29)


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.** (30)


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.** 31


</dt> <dd></dd> </dl>

</dd> <dt>

**ConfigManagerUserConfig**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")
</dt> </dl>

Se **true**, il dispositivo usa una configurazione definita dall'utente.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**CorrectableError**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,12 "," MIF. DMTF \| matrice di memoria fisica \| 001,8 ")
</dt> </dl>

Se **true**, l'errore più recente è correggibile. Se la proprietà **errorInfo** è uguale a 3 ("OK"), questa proprietà non ha alcun significato.

Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di. Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")
</dt> </dl>

Descrizione testuale dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**EndingAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Array con mapping degli indirizzi \| 001,4 "," MIF. \|Indirizzi con mapping del dispositivo \| di memoria DMTF 001,5 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobyte ")
</dt> </dl>

Indirizzo finale a cui fa riferimento un'applicazione o un sistema operativo e mappato da un controller di memoria per questo oggetto memoria. L'indirizzo finale è specificato in kilobyte.

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).

</dd> <dt>

**ErrorAccess**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,15 "," MIF. DMTF \| matrice di memoria fisica \| 001,10 ")
</dt> </dl>

Operazione di accesso alla memoria che ha causato l'ultimo errore. Il tipo di errore è descritto dalla proprietà **errorInfo** . Se la proprietà **errorInfo** è uguale a 3 ("OK"), questa proprietà non ha alcun significato.

Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (2)


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

**Lettura** (3)


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

**Scrittura** (4)


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

**Scrittura parziale** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**ErrorAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,19 "," MIF. DMTF \| Memory Device \| 002,20 "," MIF. DMTF \| matrice di memoria fisica \| 001,14 ")
</dt> </dl>

Indirizzo dell'ultimo errore di memoria. Il tipo di errore è descritto dalla proprietà **errorInfo** . Se la proprietà **errorInfo** è uguale a 3 ("OK"), questa proprietà non ha alcun significato.

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **true**, l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**ErrorData**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,17 "," MIF. DMTF \| array di memoria fisica \| 001,12 "), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Dati acquisiti durante l'ultimo accesso errato alla memoria. I dati occupano i primi *n* ottetti della matrice necessari per conservare il numero di bit specificato dalla proprietà **ErrorTransferSize** . Se **ErrorTransferSize** è 0, questa proprietà non ha alcun significato.

Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).

</dd> <dt>

**ErrorDataOrder**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ordine dei dati archiviati nella proprietà **ErrorData** . Se **ErrorTransferSize** è 0, questa proprietà non ha alcun significato.

Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)


</dt> <dd>

Sconosciuto.

</dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**Byte meno significativi prima** (1)


</dt> <dd>

Byte meno significativo per primo.

</dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**Primo byte significativo** (2)


</dt> <dd>

Primo byte significativo.

</dd> </dl>

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa in formato libero che fornisce informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**ErrorInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,12 "," MIF. \|Matrice di memoria fisica DMTF \| 001,8 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Memory**](cim-memory.md).**OtherErrorDescription**")
</dt> </dl>

Tipo di errore che si è verificato più di recente. I valori da 12 a 14 non sono definiti nello schema CIM perché DMI combina la semantica del tipo di errore e se è correggibile. Se un errore è correggibile è indicato nella proprietà **CorrectableError** .

Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)


</dt> <dd>

Altro.

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)


</dt> <dd>

Sconosciuto.

</dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span id="OK"></span><span id="ok"></span>**OK** (3)


</dt> <dd>

OK.

</dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>**Lettura non valida** (4)


</dt> <dd>

Lettura non valida.

</dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>**Errore di parità** (5)


</dt> <dd>

Errore di parità.

</dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>**Errore a bit singolo** (6)


</dt> <dd>

Errore a bit singolo.

</dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>**Errore a doppio bit** (7)


</dt> <dd>

Errore a doppio bit.

</dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>**Errore a più bit** (8)


</dt> <dd>

Errore a più bit.

</dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>**Errore di roditura** (9)


</dt> <dd>

Errore di bocconcino.

</dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>**Errore di checksum** (10)


</dt> <dd>

Errore di checksum.

</dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>**Errore CRC** (11)


</dt> <dd>

Errore CRC.

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>Non **definito** (12)


</dt> <dd>

Non definito.

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>Non **definito** (13)


</dt> <dd>

Non definito.

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>Non **definito** (14)


</dt> <dd>

Non definito.

</dd> </dl>

</dd> <dt>

**ErrorMethodology**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| matrice di memoria fisica \| 001,7 ")
</dt> </dl>

Indica se vengono utilizzati algoritmi di parità o CRC, ECC o altri meccanismi. È anche possibile specificare i dettagli sull'algoritmo.

Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).

</dd> <dt>

**ErrorResolution**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,21 "," MIF. DMTF \| array di memoria fisica \| 001,15 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")
</dt> </dl>

Specifica l'intervallo, in byte, in cui è possibile risolvere l'ultimo errore. Se, ad esempio, gli indirizzi di errore vengono risolti in bit 11, ovvero in base a una tipica pagina, gli errori possono essere risolti in limiti di 4 KB e questa proprietà è impostata su 4000. Se la proprietà **errorInfo** è uguale a 3 ("OK"), questa proprietà non ha alcun significato.

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).

</dd> <dt>

**ErrorTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora in cui si è verificato l'ultimo errore di memoria. Il tipo di errore è descritto dalla proprietà **errorInfo** . Se la proprietà **errorInfo** è uguale a 3 ("OK"), questa proprietà non ha alcun significato.

Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).

</dd> <dt>

**ErrorTransferSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,16 "," MIF. DMTF \| array di memoria fisica \| 001,11 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")
</dt> </dl>

Dimensioni del trasferimento dei dati, in bit, che hanno causato l'ultimo errore. Il valore 0 indica che non è presente alcun errore. Se la proprietà **errorInfo** è uguale a 3 ("OK"), questa proprietà deve essere impostata su 0.

Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).

</dd> <dt>

**FlushTimer**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| cache \| di sistema 003,14 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" secondi ")
</dt> </dl>

Quantità massima di tempo, in secondi, per cui è possibile che le righe o i bucket sporchi rimangano nella cache prima che vengano scaricati. Il valore 0 indica che uno scaricamento della cache non è controllato da un timer di scaricamento.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")
</dt> </dl>

Indica quando l'oggetto è stato installato. La mancanza di un valore non indica che l'oggetto non è installato.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ultimo codice di errore segnalato dal dispositivo logico.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**Level**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| cache di sistema \| 003,2 ")
</dt> </dl>

Specifica se si tratta della cache primaria, secondaria o terziaria. È possibile definire anche "other", "Unknown" e "not applicabile".

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)


</dt> <dd>

Altro.

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)


</dt> <dd>

Sconosciuto.

</dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Primario** (3)


</dt> <dd>

Primario.

</dd> <dt>

<span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>

<span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>**Secondario** (4)


</dt> <dd>

Secondario.

</dd> <dt>

<span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>

<span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>**Terziario** (5)


</dt> <dd>

Terziario.

</dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)


</dt> <dd>

Non applicabile.

</dd> </dl>

</dd> <dt>

**LineSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| System Cache \| 003,10 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")
</dt> </dl>

Dimensione, in byte, di un singolo bucket o riga della cache.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")
</dt> </dl>

Etichetta con cui l'oggetto è noto. Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**NumberOfBlocks**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Host IETF-risorse-MIB. hrStorageSize ")
</dt> </dl>

Numero di blocchi consecutivi, ciascuno dei quali blocca la dimensione del valore contenuto nella proprietà **blockSize** , che costituisce l'extent di archiviazione. Le dimensioni totali dell'extent di archiviazione possono essere calcolate moltiplicando il valore della proprietà **blockSize** in base al valore di questa proprietà. Se il valore di **blockSize** è 1 (uno), questa proprietà corrisponde alla dimensione totale dell'extent di archiviazione.

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).

</dd> <dt>

**OtherErrorDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Memory**](cim-memory.md).**ErrorInfo**")
</dt> </dl>

Stringa in formato libero che fornisce informazioni se la proprietà **ErrorType** è impostata su 1 ("other"). Se non è impostato su 1, questa stringa non ha alcun significato.

Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).

</dd> <dt>

**PNPDeviceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")
</dt> </dl>

Indica l'identificatore del dispositivo Plug and Play Win32 del dispositivo logico.

Esempio: " \* PNP030b"

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica le funzionalità specifiche relative al risparmio di energia del dispositivo logico.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)


</dt> <dd>

Le capacità relative al risparmio di energia sono sconosciute.

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)


</dt> <dd>

Le capacità relative al risparmio di energia non sono supportate per questo dispositivo.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)


</dt> <dd>

Le capacità correlate all'alimentazione sono state disabilitate.

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)


</dt> <dd>

Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)


</dt> <dd>

Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)


</dt> <dd>

Il metodo **SetPowerState** è supportato. Questo metodo è disponibile nella classe [**\_ LogicalDevice CIM**](cim-logicaldevice.md) padre e può essere implementato. Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)


</dt> <dd>

Il metodo **SetPowerState** può essere richiamato con il parametro *PowerState* impostato su 5 ("ciclo di alimentazione").

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)


</dt> <dd>

Il metodo **SetPowerState** può essere richiamato con il parametro *PowerState* impostato su 5 ("ciclo di alimentazione") e il parametro *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.

</dd> </dl>

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **true**, il dispositivo può essere gestito da energia elettrica, ovvero viene inserito in uno stato di risparmio energia. Se **false**, il valore intero 1 ("non supportato") deve essere l'unico elemento nella matrice **PowerManagementCapabilities** .

Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o se abilitate, quali funzionalità sono supportate. Per ulteriori informazioni, vedere la matrice **PowerManagementCapabilities** .

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**Scopo**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa in formato libero che descrive i supporti e il relativo utilizzo.

Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](cim-storageextent.md).

</dd> <dt>

**Disporre**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| cache di sistema \| 003,13 ")
</dt> </dl>

Criteri utilizzati dalla cache per gestire le richieste di lettura. Se i criteri di lettura vengono determinati singolarmente, ovvero per ogni richiesta, è necessario specificare il valore 6 ("determinazione per I/O"). Anche "other" e "Unknown" sono valori validi.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)


</dt> <dd>

Altro.

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)


</dt> <dd>

Sconosciuto.

</dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span id="Read"></span><span id="read"></span><span id="READ"></span>**Lettura** (3)


</dt> <dd>

Lettura.

</dd> <dt>

<span id="Read-Ahead"></span><span id="read-ahead"></span><span id="READ-AHEAD"></span>

<span id="Read-Ahead"></span><span id="read-ahead"></span><span id="READ-AHEAD"></span>**Read-Ahead** (4)


</dt> <dd>

Read-ahead.

</dd> <dt>

<span id="Read_and_Read-Ahead"></span><span id="read_and_read-ahead"></span><span id="READ_AND_READ-AHEAD"></span>

<span id="Read_and_Read-Ahead"></span><span id="read_and_read-ahead"></span><span id="READ_AND_READ-AHEAD"></span>**Lettura e Read-Ahead** (5)


</dt> <dd>

Lettura e Read-ahead.

</dd> <dt>

<span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>

<span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>**Determinazione per I/O** (6)


</dt> <dd>

Determinazione per I/O.

</dd> </dl>

</dd> <dt>

**ReplacementPolicy**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| cache di sistema \| 003,12 ")
</dt> </dl>

Enumerazione Integer che descrive l'algoritmo che determina quali righe o bucket della cache deve essere riutilizzato.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)


</dt> <dd>

Altro.

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)


</dt> <dd>

Sconosciuto.

</dd> <dt>

<span id="Least_Recently_Used__LRU_"></span><span id="least_recently_used__lru_"></span><span id="LEAST_RECENTLY_USED__LRU_"></span>

<span id="Least_Recently_Used__LRU_"></span><span id="least_recently_used__lru_"></span><span id="LEAST_RECENTLY_USED__LRU_"></span>**Utilizzato meno di recente (LRU)** (3)


</dt> <dd>

Utilizzato meno di recente (LRU).

</dd> <dt>

<span id="First_In_First_Out__FIFO_"></span><span id="first_in_first_out__fifo_"></span><span id="FIRST_IN_FIRST_OUT__FIFO_"></span>

<span id="First_In_First_Out__FIFO_"></span><span id="first_in_first_out__fifo_"></span><span id="FIRST_IN_FIRST_OUT__FIFO_"></span>**FIFO (First in First out)** (4)


</dt> <dd>

FIFO (First-in, First-out).

</dd> <dt>

<span id="Last_In_First_Out__LIFO_"></span><span id="last_in_first_out__lifo_"></span><span id="LAST_IN_FIRST_OUT__LIFO_"></span>

<span id="Last_In_First_Out__LIFO_"></span><span id="last_in_first_out__lifo_"></span><span id="LAST_IN_FIRST_OUT__LIFO_"></span>**LIFO (Last in First out)** (5)


</dt> <dd>

LIFO (Last-in, First-out).

</dd> <dt>

<span id="Least_Frequently_Used__LFU_"></span><span id="least_frequently_used__lfu_"></span><span id="LEAST_FREQUENTLY_USED__LFU_"></span>

<span id="Least_Frequently_Used__LFU_"></span><span id="least_frequently_used__lfu_"></span><span id="LEAST_FREQUENTLY_USED__LFU_"></span>**Uso meno frequente (LFU)** (6)


</dt> <dd>

Uso meno frequente (LFU)

</dd> <dt>

<span id="Most_Frequently_Used__MFU_"></span><span id="most_frequently_used__mfu_"></span><span id="MOST_FREQUENTLY_USED__MFU_"></span>

<span id="Most_Frequently_Used__MFU_"></span><span id="most_frequently_used__mfu_"></span><span id="MOST_FREQUENTLY_USED__MFU_"></span>**Uso più frequente (MFU)** (7)


</dt> <dd>

Utilizzato più di frequente (MFU).

</dd> <dt>

<span id="Data_Dependent_Multiple_Algorithms"></span><span id="data_dependent_multiple_algorithms"></span><span id="DATA_DEPENDENT_MULTIPLE_ALGORITHMS"></span>

<span id="Data_Dependent_Multiple_Algorithms"></span><span id="data_dependent_multiple_algorithms"></span><span id="DATA_DEPENDENT_MULTIPLE_ALGORITHMS"></span>**Più algoritmi dipendenti dai dati** (8)


</dt> <dd>

Più algoritmi dipendenti dai dati.

</dd> </dl>

</dd> <dt>

**IndirizzoIniziale**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Array con mapping degli indirizzi \| 001,3 "," MIF. \|Indirizzi con mapping del dispositivo \| di memoria DMTF 001,4 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobyte ")
</dt> </dl>

Indirizzo iniziale, a cui viene fatto riferimento da un'applicazione o da un sistema operativo e mappato da un controller di memoria, per questo oggetto memoria. L'indirizzo iniziale è specificato in kilobyte.

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")
</dt> </dl>

Stringa che indica lo stato corrente dell'oggetto. È possibile definire lo stato operativo e non operativo. Lo stato operativo può includere "OK", "danneggiato" e "errore predazione". "Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.

Lo stato non operativo può includere "Error", "starting", "stoping" e "Service". Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative. Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

Sono inclusi i valori seguenti:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Errore** ("errore")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

Ridotto **("danneggiato"** )


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** ("sconosciuto")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Errore di predazione** ("Predator fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Avvio** di ("avvio")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Arresto** in corso ("arresto")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Servizio** ("servizio")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Sottolineato** (sottolineato)


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**Noncover** ("noncover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Nessun contatto** ("nessun contatto")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Comunicazione persa** ("comunicazione persa")


</dt> <dd></dd> </dl>

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,3 ")
</dt> </dl>

Stato del dispositivo logico. Se questa proprietà non è applicabile al dispositivo logico, è necessario utilizzare il valore 5 ("non applicabile").

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (2)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Abilitato** (3)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Disabilitato** (4)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Non applicabile** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Nome della classe di creazione del sistema di ambito.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**SystemLevelAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se le informazioni sull'indirizzo nella proprietà **ErrorAddress** sono un indirizzo a livello di sistema (**true**) o un indirizzo fisico (**false**). Se la proprietà **errorInfo** è uguale a 3 ("OK"), questa proprietà non ha alcun significato.

Questa proprietà viene ereditata [**dalla \_ memoria CIM**](cim-memory.md).

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Nome del sistema di ambito.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**WritePolicy**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| cache di sistema \| 003,5 ")
</dt> </dl>

Definisce se la cache è write-back o Write-through o se le informazioni "variano in base all'indirizzo" o se sono definite singolarmente per ogni input/output. È possibile specificare anche "other" e "Unknown".

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)


</dt> <dd>

Altro.

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)


</dt> <dd>

Sconosciuto.

</dd> <dt>

<span id="Write_Back"></span><span id="write_back"></span><span id="WRITE_BACK"></span>

<span id="Write_Back"></span><span id="write_back"></span><span id="WRITE_BACK"></span>**Write back** (3)


</dt> <dd>

Write back.

</dd> <dt>

<span id="Write_Through"></span><span id="write_through"></span><span id="WRITE_THROUGH"></span>

<span id="Write_Through"></span><span id="write_through"></span><span id="WRITE_THROUGH"></span>**Scrivi fino** a (4)


</dt> <dd>

Scrivere.

</dd> <dt>

<span id="Varies_with_Address"></span><span id="varies_with_address"></span><span id="VARIES_WITH_ADDRESS"></span>

<span id="Varies_with_Address"></span><span id="varies_with_address"></span><span id="VARIES_WITH_ADDRESS"></span>**Varia in base all'indirizzo** (5)


</dt> <dd>

Varia in base all'indirizzo.

</dd> <dt>

<span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>

<span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>**Determinazione per I/O** (6)


</dt> <dd>

Determinazione per I/O.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **CIM \_ CacheMemory** è derivata dalla [**\_ memoria CIM**](cim-memory.md).

WMI non implementa questa classe. Per ulteriori informazioni sulle classi derivate da **CIM \_ CacheMemory**, vedere [Win32 Classes](win32-provider.md).

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

[**\_Memoria CIM**](cim-memory.md)
</dt> </dl>

 


---
description: La classe CIM \_ NonVolatileStorage rappresenta le funzionalità e la gestione dell'archiviazione non volatile. La memoria non volatile include in modo nativo l'archiviazione flash e ROM.
ms.assetid: 39158b31-31f7-460c-aef1-1ca423badad6
ms.tgt_platform: multiple
title: CIM_NonVolatileStorage classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NonVolatileStorage
- CIM_NonVolatileStorage.Access
- CIM_NonVolatileStorage.AdditionalErrorData
- CIM_NonVolatileStorage.Availability
- CIM_NonVolatileStorage.BlockSize
- CIM_NonVolatileStorage.Caption
- CIM_NonVolatileStorage.ConfigManagerErrorCode
- CIM_NonVolatileStorage.ConfigManagerUserConfig
- CIM_NonVolatileStorage.CorrectableError
- CIM_NonVolatileStorage.CreationClassName
- CIM_NonVolatileStorage.Description
- CIM_NonVolatileStorage.DeviceID
- CIM_NonVolatileStorage.EndingAddress
- CIM_NonVolatileStorage.ErrorAccess
- CIM_NonVolatileStorage.ErrorAddress
- CIM_NonVolatileStorage.ErrorCleared
- CIM_NonVolatileStorage.ErrorData
- CIM_NonVolatileStorage.ErrorDataOrder
- CIM_NonVolatileStorage.ErrorDescription
- CIM_NonVolatileStorage.ErrorInfo
- CIM_NonVolatileStorage.ErrorMethodology
- CIM_NonVolatileStorage.ErrorResolution
- CIM_NonVolatileStorage.ErrorTime
- CIM_NonVolatileStorage.ErrorTransferSize
- CIM_NonVolatileStorage.InstallDate
- CIM_NonVolatileStorage.IsWriteable
- CIM_NonVolatileStorage.LastErrorCode
- CIM_NonVolatileStorage.Name
- CIM_NonVolatileStorage.NumberOfBlocks
- CIM_NonVolatileStorage.OtherErrorDescription
- CIM_NonVolatileStorage.PNPDeviceID
- CIM_NonVolatileStorage.PowerManagementCapabilities
- CIM_NonVolatileStorage.PowerManagementSupported
- CIM_NonVolatileStorage.Purpose
- CIM_NonVolatileStorage.StartingAddress
- CIM_NonVolatileStorage.Status
- CIM_NonVolatileStorage.StatusInfo
- CIM_NonVolatileStorage.SystemCreationClassName
- CIM_NonVolatileStorage.SystemLevelAddress
- CIM_NonVolatileStorage.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8df8461aad42bfa1e1107a18f99f5a33c85967d52fe1eea9c22e924604be20ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119820961"
---
# <a name="cim_nonvolatilestorage-class"></a>Classe CIM \_ NonVolatileStorage

La **classe CIM \_ NonVolatileStorage** rappresenta le funzionalità e la gestione dell'archiviazione non volatile. La memoria non volatile include in modo nativo l'archiviazione flash e ROM. Inoltre, la memoria non volatile può essere basata sull'archiviazione volatile, se la memoria volatile è supportata da una batteria. Questo scenario, ad esempio, viene descritto da un'istanza della relazione [**CIM \_ AssociatedBattery**](cim-associatedbattery.md) che fa riferimento all'archiviazione non volatile come **Dependent** e alla batteria come **antecedente** e da un'istanza della relazione [**CIM \_ BasedOn**](cim-basedon.md) che fa riferimento all'archiviazione non volatile come **Dependent** e all'archiviazione volatile come **Antecedent**.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Common Information Model Distributed Management Task Force) sono le classi padre su cui vengono compilate le classi WMI. WMI attualmente supporta solo gli schemi [della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{18074AFA-F0FE-11d2-8617-0000F8102E5F}"), AMENDMENT]
class CIM_NonVolatileStorage : CIM_Memory
{
  uint16   Access;
  uint8    AdditionalErrorData[];
  uint16   Availability;
  uint64   BlockSize;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  boolean  CorrectableError;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  uint64   EndingAddress;
  uint16   ErrorAccess;
  uint64   ErrorAddress;
  boolean  ErrorCleared;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  string   ErrorDescription;
  uint16   ErrorInfo;
  string   ErrorMethodology;
  uint64   ErrorResolution;
  datetime ErrorTime;
  uint32   ErrorTransferSize;
  datetime InstallDate;
  boolean  IsWriteable;
  uint32   LastErrorCode;
  string   Name;
  uint64   NumberOfBlocks;
  string   OtherErrorDescription;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Purpose;
  uint64   StartingAddress;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  boolean  SystemLevelAddress;
  string   SystemName;
};
```

## <a name="members"></a>Members

La **classe CIM \_ NonVolatileStorage** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe CIM \_ NonVolatileStorage** include questi metodi.



| Metodo                                                                        | Descrizione                                                                                                                              |
|:------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [**Reset**](reset-method-in-class-cim-nonvolatilestorage.md)                 | Richiede una reimpostazione del dispositivo logico. Non implementato da WMI.<br/>                                                               |
| [**SetPowerState**](setpowerstate-method-in-class-cim-nonvolatilestorage.md) | Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato. Non implementato da WMI.<br/> |



 

### <a name="properties"></a>Proprietà

La **classe CIM \_ NonVolatileStorage** ha queste proprietà.

<dl> <dt>

**Accesso**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Proprietà di lettura/scrittura dei supporti.

Questa proprietà viene ereditata da [**CIM \_ StorageExtent.**](cim-storageextent.md)

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

**Lettura/Scrittura supportata** (3)


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

**Scrivi una sola volta** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**AdditionalErrorData**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002.18", "MIF. DMTF \| Physical Memory Array \| 001.13"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Matrice di ottetti che contengono informazioni aggiuntive sugli errori. Un esempio è la sintassi ECC (Error Checking and Correcting) o la restituzione dei bit di controllo se viene usata una metodologia di errore basata su CRC. In quest'ultimo caso, se viene riconosciuto un errore a bit singolo ed è noto l'algoritmo CRC, è possibile determinare il bit esatto che ha avuto esito negativo. Questo tipo di dati (Ecc Syndrome, check-bit o parity-bit o altre informazioni fornite dal fornitore) è incluso in questo campo. Se la **proprietà ErrorInfo** è uguale a 3 ("OK"), questa proprietà non ha alcun significato.

Questa proprietà viene ereditata dalla [**memoria CIM. \_**](cim-memory.md)

</dd> <dt>

**Disponibilità**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Operational State \| 003.5", "MIB. IETF \| HOST-RESOURCES-MIB.hrDeviceStatus")
</dt> </dl>

Disponibilità e stato del dispositivo.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/alimentazione completa** (3)


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

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuori servizio** (9)


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

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia - Sconosciuto** (13)


</dt> <dd>

Il dispositivo è noto per essere in modalità risparmio energia, ma lo stato esatto è sconosciuto.

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia - Modalità a basso consumo** (14)


</dt> <dd>

Il dispositivo è in stato di risparmio energia, ma funziona ancora e può presentare prestazioni ridotte.

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia - Standby** (15)


</dt> <dd>

Il dispositivo non funziona, ma può essere portato a piena potenza rapidamente.

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia - Avviso** (17)


</dt> <dd>

Il dispositivo è in uno stato di avviso, anche se in modalità risparmio energia.

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**In pausa** (18)


</dt> <dd>

Il dispositivo è sospeso.

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)


</dt> <dd>

Il dispositivo non è pronto.

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurato** (20)


</dt> <dd>

Il dispositivo non è configurato.

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)


</dt> <dd>

Il dispositivo è silenzioso.

</dd> </dl>

</dd> <dt>

**Blocksize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")
</dt> </dl>

Dimensione, in byte, dei blocchi che formano l'extent di archiviazione. Se la dimensione del blocco variabile è variabile, è necessario specificare la dimensione massima in byte del blocco. Se le dimensioni del blocco sono sconosciute o se un concetto di blocco non è valido (ad esempio, per extent aggregati, memoria o dischi logici), immettere 1 (uno).

Questa proprietà viene ereditata da [**CIM \_ StorageExtent.**](cim-storageextent.md)

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Breve descrizione testuale dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**ConfigManagerErrorCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")
</dt> </dl>

Windows Gestione configurazione codice di errore.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**  (0)


</dt> <dd>

Il dispositivo funziona correttamente.

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.** (1)


</dt> <dd>

Il dispositivo non è configurato correttamente.

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows possibile caricare il driver per questo dispositivo.** (2)


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato o il sistema potrebbe avere memoria insufficiente o altre risorse.** (3)


</dt> <dd>

Il driver per questo dispositivo potrebbe essere danneggiato o il sistema potrebbe avere memoria insufficiente o altre risorse.

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei relativi driver o il Registro di sistema potrebbe essere danneggiato.** (4)


</dt> <dd>

Il dispositivo non funziona correttamente. Uno dei relativi driver o il Registro di sistema potrebbe essere danneggiato.

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che non Windows gestire.** (5)


</dt> <dd>

Il driver per il dispositivo richiede una risorsa che non Windows gestire.

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**  (6)


</dt> <dd>

La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.** (7)


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore del driver per il dispositivo è mancante.** (8)


</dt> <dd>

Il caricatore del driver per il dispositivo è mancante.

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.** (9)


</dt> <dd>

Il dispositivo non funziona correttamente. il firmware di controllo segnala erroneamente le risorse per il dispositivo.

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.** (10)


</dt> <dd>

Impossibile avviare il dispositivo.

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Il dispositivo non è riuscito.** (11)


</dt> <dd>

Dispositivo non riuscito.

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non riesce a trovare risorse gratuite sufficienti da usare.** (12)


</dt> <dd>

Il dispositivo non riesce a trovare risorse gratuite sufficienti da usare.

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows possibile verificare le risorse del dispositivo.** (13)


</dt> <dd>

Windows possibile verificare le risorse del dispositivo.

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente fino a quando non si riavvia il computer.** (14)


</dt> <dd>

Il dispositivo non funziona correttamente finché il computer non viene riavviato.

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Questo dispositivo non funziona correttamente perché è probabile che si sia verificato un problema di enumerazione.** (15)


</dt> <dd>

Il dispositivo non funziona correttamente a causa di un possibile problema di enumerazione.

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.** (16)


</dt> <dd>

Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Questo dispositivo richiede un tipo di risorsa sconosciuto.** (17)


</dt> <dd>

Il dispositivo richiede un tipo di risorsa sconosciuto.

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.** (18)


</dt> <dd>

I driver di dispositivo devono essere reinstallati.

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'uso del caricatore VxD.** (19)


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro potrebbe essere danneggiato.** (20)


</dt> <dd>

Il Registro di sistema potrebbe essere danneggiato.

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo il dispositivo.** (21)


</dt> <dd>

Errore di sistema. Se la modifica del driver di dispositivo è inefficace, vedere la documentazione dell'hardware. Windows sta rimuovendo il dispositivo.

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Questo dispositivo è disabilitato.** (22)


</dt> <dd>

Il dispositivo è disabilitato.

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware.** (23)


</dt> <dd>

Errore di sistema. Se la modifica del driver di dispositivo è inefficace, vedere la documentazione dell'hardware.

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Il dispositivo non è presente, non funziona correttamente o non dispone di tutti i relativi driver installati.** (24)


</dt> <dd>

Il dispositivo non è presente, non funziona correttamente o non dispone di tutti i relativi driver installati.

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora configurando il dispositivo.** (25)


</dt> <dd>

Windows sta ancora configurando il dispositivo.

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora configurando il dispositivo.** (26)


</dt> <dd>

Windows sta ancora configurando il dispositivo.

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.** (27)


</dt> <dd>

Il dispositivo non ha una configurazione di log valida.

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.** (28)


</dt> <dd>

I driver di dispositivo non sono installati.

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha dato le risorse necessarie.** (29)


</dt> <dd>

Il dispositivo è disabilitato. il firmware del dispositivo non ha fornito le risorse necessarie.

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa richiesta di interrupt (IRQ) che un altro dispositivo sta usando.** (30)


</dt> <dd>

Il dispositivo usa una risorsa IRQ in uso da un altro dispositivo.

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché non Windows caricare i driver necessari per il dispositivo.** (31)


</dt> <dd>

Il dispositivo non funziona correttamente. Windows non è possibile caricare i driver di dispositivo necessari.

</dd> </dl>

</dd> <dt>

**ConfigManagerUserConfig**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")
</dt> </dl>

Se **TRUE,** il dispositivo usa una configurazione definita dall'utente.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**CorrectableError**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002.12", "MIF. DMTF \| Physical Memory Array \| 001.8")
</dt> </dl>

Se **TRUE,** l'errore più recente è stato corretto. Se la **proprietà ErrorInfo** è uguale a 3 ("OK"), questa proprietà non ha alcun significato.

Questa proprietà viene ereditata dalla [**memoria CIM. \_**](cim-memory.md)

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave \_ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Nome della classe o della sottoclasse utilizzata nella creazione di un'istanza. Se usata con altre proprietà chiave della classe , questa proprietà consente l'identificazione univoca di tutte le istanze della classe e delle relative sottoclassi.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")
</dt> </dl>

Descrizione testuale dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Deviceid**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave \_ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**EndingAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DmTF \| Memory Array Mapped Addresses \| 001.4", "MIF. DmTF \| Memory Device Mapped Addresses \| 001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")
</dt> </dl>

Indirizzo finale, a cui fa riferimento un'applicazione o un sistema operativo e mappato da un controller di memoria, per l'oggetto memoria. L'indirizzo finale è specificato in kilobyte.

Questa proprietà viene ereditata dalla [**memoria CIM. \_**](cim-memory.md)

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**ErrorAccess**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002.15", "MIF. DMTF \| Physical Memory Array \| 001.10")
</dt> </dl>

Enumerazione che indica l'operazione di accesso alla memoria che ha causato l'ultimo errore. Il tipo di errore è descritto dalla **proprietà ErrorInfo.** Se la **proprietà ErrorInfo** è uguale a 3 ("OK"), questa proprietà non ha alcun significato.

Questa proprietà viene ereditata dalla [**memoria CIM. \_**](cim-memory.md)

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

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002.19", "MIF. DMTF \| Memory Device \| 002.20", "MIF. DMTF \| Physical Memory Array \| 001.14")
</dt> </dl>

Indirizzo dell'ultimo errore di memoria. Il tipo di errore è descritto dalla **proprietà ErrorInfo.** Se la **proprietà ErrorInfo** è uguale a 3 ("OK"), questa proprietà non ha alcun significato.

Questa proprietà viene ereditata dalla [**memoria CIM. \_**](cim-memory.md)

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **TRUE,** l'errore segnalato nella **proprietà LastErrorCode** viene ora cancellato.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**Errordata**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indicizzato"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002.17", "MIF. DMTF \| Physical Memory Array \| 001.12"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Dati acquisiti durante l'ultimo accesso erro alla memoria. I dati occupano i primi *n ottetti* della matrice necessari per contenere il numero di bit specificato dalla **proprietà ErrorTransferSize.** Se **ErrorTransferSize** è 0, questa proprietà non ha alcun significato.

Questa proprietà viene ereditata dalla [**memoria CIM. \_**](cim-memory.md)

</dd> <dt>

**ErrorDataOrder**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ordinamento dei dati archiviati nella **proprietà ErrorData.** Se **ErrorTransferSize** è 0, questa proprietà non ha alcun significato.

Questa proprietà viene ereditata dalla [**memoria CIM. \_**](cim-memory.md)

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

**Byte meno significativo prima** (1)


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

**Byte più significativo per primo** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa in formato libero che fornisce informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**Errorinfo**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002.12", "MIF. DMTF \| Physical Memory Array \| 001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Memory**](cim-memory.md).**OtherErrorDescription**")
</dt> </dl>

Tipo di errore che si è verificato più di recente. I valori da 12 a 14 non sono definiti nello schema CIM perché DMI combina la semantica del tipo di errore e indica se è stato corretto. La proprietà **CorrectableError** indica se è possibile correggere un errore. Questa proprietà viene ereditata dalla [**memoria CIM. \_**](cim-memory.md)

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

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>**Lettura non erta** (4)


</dt> <dd>

Lettura non erta.

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

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>**Errore a due bit** (7)


</dt> <dd>

Errore a doppio bit.

</dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>**Errore a più bit** (8)


</dt> <dd>

Errore a più bit.

</dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>**Errore Nibble** (9)


</dt> <dd>

Errore nibble.

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

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Non definito** (12)


</dt> <dd>

Non definito.

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Non definito** (13)


</dt> <dd>

Non definito.

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Non definito** (14)


</dt> <dd>

Non definito.

</dd> </dl>

</dd> <dt>

**ErrorMethodology**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Physical Memory Array \| 001.7")
</dt> </dl>

Specifica se vengono utilizzati algoritmi di parità, algoritmi CRC, ECC o altri meccanismi. È anche possibile specificare dettagli sull'algoritmo.

Questa proprietà viene ereditata da [**CIM \_ StorageExtent.**](cim-storageextent.md)

</dd> <dt>

**ErrorResolution**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002.21", "MIF. DMTF \| Physical Memory Array \| 001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")
</dt> </dl>

Intervallo, in byte, in cui è possibile risolvere l'ultimo errore. Ad esempio, se gli indirizzi di errore vengono risolti nel bit 11 ,ovvero in base a una pagina tipica, gli errori possono essere risolti fino a limiti di 4 KB e questa proprietà è impostata su 4000. Se la **proprietà ErrorInfo** è uguale a 3 ("OK"), questa proprietà non ha alcun significato.

Questa proprietà viene ereditata dalla [**memoria CIM. \_**](cim-memory.md)

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> <dt>

**ErrorTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ora dell'ultimo errore di memoria. Il tipo di errore è descritto dalla **proprietà ErrorInfo.** Se la **proprietà ErrorInfo** è uguale a 3 ("OK"), questa proprietà non ha alcun significato.

Questa proprietà viene ereditata dalla [**memoria CIM. \_**](cim-memory.md)

</dd> <dt>

**Errortransfersize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002.16", "MIF. DMTF \| Physical Memory Array \| 001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")
</dt> </dl>

Dimensioni del trasferimento dei dati, in bit, che ha causato l'ultimo errore. Il valore 0 (zero) non indica alcun errore. Se la **proprietà ErrorInfo** è uguale a 3 ("OK"), questa proprietà deve essere impostata su 0 (zero).

Questa proprietà viene ereditata dalla [**memoria CIM. \_**](cim-memory.md)

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")
</dt> </dl>

Data e ora di installazione dell'oggetto. Questa proprietà non richiede un valore per indicare che l'oggetto è installato.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**IsWriteable**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **TRUE,** l'archiviazione non volatile è scrivibile.

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ultimo codice di errore segnalato dal dispositivo logico.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")
</dt> </dl>

Etichetta con cui l'oggetto è noto. Quando è sottoclassata, questa proprietà può essere sottoposta a override come proprietà chiave.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**NumberOfBlocks**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| HOST-RESOURCES-MIB.hrStorageSize")
</dt> </dl>

Numero totale di blocchi consecutivi. Ogni blocco è la dimensione del valore contenuto nella **proprietà BlockSize,** che costituisce l'extent di archiviazione. Le dimensioni totali dell'extent di archiviazione possono essere calcolate moltiplicando il valore della **proprietà BlockSize** per il valore di questa proprietà. Se il valore di **BlockSize** è 1 (uno), questa proprietà è la dimensione totale dell'extent di archiviazione.

Questa proprietà viene ereditata da [**CIM \_ StorageExtent.**](cim-storageextent.md)

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> <dt>

**OtherErrorDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Memory**](cim-memory.md).**ErrorInfo**")
</dt> </dl>

Stringa in formato libero che fornisce informazioni se la **proprietà ErrorType** è impostata su 1 ("Altro"). Se non è impostato su 1, questa stringa non ha alcun significato.

Questa proprietà viene ereditata dalla [**memoria CIM. \_**](cim-memory.md)

</dd> <dt>

**PNPDeviceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")
</dt> </dl>

Windows Plug and Play identificatore di dispositivo del dispositivo logico. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

Esempio: \* "PNP030b"

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice delle funzionalità specifiche correlate all'alimentazione di un dispositivo logico.

Questa proprietà viene ereditata da **CIM \_ LogicalDevice.**

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)


</dt> <dd>

Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto o le informazioni non sono disponibili.

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità risparmio energia immesse automaticamente** (4)


</dt> <dd>

Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)


</dt> <dd>

Il [**metodo SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato. Questo metodo si trova nella classe **CIM \_ LogicalDevice** padre e può essere implementato. Per altre informazioni, vedere [Progettazione di Managed Object Format (MOF).](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Alimentazione supportata** (6)


</dt> <dd>

Il [**metodo SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il *parametro PowerState* impostato su 5 (Ciclo di alimentazione).

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Accensione a tempo supportata** (7)


</dt> <dd>

Il [**metodo SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (Power Cycle) e *Time* impostato su una data e un'ora o un intervallo specifici per l'accensione.

</dd> </dl>

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **TRUE,** il dispositivo può essere gestito dall'alimentazione, vale a dire inserito in uno stato di risparmio energia. Se **FALSE,** il valore intero 1 ("Non supportato") deve essere l'unica voce nella matrice **PowerManagementCapabilities.**

Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o, se abilitate, quali funzionalità sono supportate. Per altre informazioni, vedere la matrice **PowerManagementCapabilities.** Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**Scopo**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa in formato libero che descrive il supporto e il relativo utilizzo.

Questa proprietà viene ereditata da [**CIM \_ StorageExtent.**](cim-storageextent.md)

</dd> <dt>

**StartingAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DmTF \| Memory Array Mapped Addresses \| 001.3", "MIF. DmTF \| Memory Device Mapped Addresses \| 001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")
</dt> </dl>

Indirizzo iniziale a cui fa riferimento un'applicazione o un sistema operativo ed è mappato da un controller di memoria per questo oggetto di memoria. L'indirizzo iniziale è specificato in kilobyte.

Questa proprietà viene ereditata dalla [**memoria CIM. \_**](cim-memory.md)

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Stato corrente dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

Sono inclusi i valori seguenti:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Errore** ("Errore")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degradato** ("Degraded")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** ("Sconosciuto")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred Fail** ("Pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Avvio** ("Avvio")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Arresto** ("Arresto")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Servizio** ("Servizio")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Stressed** ("Stressed")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ("NonRecover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Nessun contatto** ("Nessun contatto")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Lost Comm** ("Lost Comm")


</dt> <dd></dd> </dl>

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Operational State \| 003.3")
</dt> </dl>

Stato del dispositivo logico. Se questa proprietà non si applica al dispositivo logico, deve essere usato il valore 5 (Non applicabile).

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

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

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagati**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**SISTEMA CIM \_**](cim-system.md).**CreationClassName**"), [**chiave CIM \_**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Nome della classe di creazione del sistema di ambito.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**SystemLevelAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **TRUE,** le informazioni sull'indirizzo nella **proprietà ErrorAddress** sono un indirizzo a livello di sistema. Se **FALSE,** è un indirizzo fisico. Se la **proprietà ErrorInfo** è uguale a 3 ("OK"), questa proprietà non ha alcun significato.

Questa proprietà viene ereditata dalla [**memoria CIM. \_**](cim-memory.md)

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagati**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**SISTEMA CIM \_**](cim-system.md).**Name**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Nome del sistema di ambito.

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe CIM \_ NonVolatileStorage** deriva dalla [**memoria CIM \_**](cim-memory.md).

WMI non implementa questa classe.

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe aver apportato modifiche per correggere gli errori minori, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Memoria \_ CIM**](cim-memory.md)
</dt> </dl>

 


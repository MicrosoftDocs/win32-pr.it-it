---
description: Astrazione o emulazione di un'entità hardware che può essere o meno basata su hardware fisico.
ms.assetid: e31c82ed-2da2-4a18-a55e-16931d74f243
title: Classe CIM_LogicalDevice (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice
- CIM_LogicalDevice.SystemCreationClassName
- CIM_LogicalDevice.SystemName
- CIM_LogicalDevice.CreationClassName
- CIM_LogicalDevice.DeviceID
- CIM_LogicalDevice.PowerManagementSupported
- CIM_LogicalDevice.PowerManagementCapabilities
- CIM_LogicalDevice.Availability
- CIM_LogicalDevice.StatusInfo
- CIM_LogicalDevice.LastErrorCode
- CIM_LogicalDevice.ErrorDescription
- CIM_LogicalDevice.ErrorCleared
- CIM_LogicalDevice.OtherIdentifyingInfo
- CIM_LogicalDevice.PowerOnHours
- CIM_LogicalDevice.TotalPowerOnHours
- CIM_LogicalDevice.IdentifyingDescriptions
- CIM_LogicalDevice.AdditionalAvailability
- CIM_LogicalDevice.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 471b10f8d3c8640cfcc4277d0151bdd46d59db86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749655"
---
# <a name="cim_logicaldevice-class-hyper-v-management"></a>Classe CIM_LogicalDevice (gestione Hyper-V)

Astrazione o emulazione di un'entità hardware che può essere o meno basata su hardware fisico.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Version("2.8.0"), UMLPackagePath("CIM::Core::Device"), AMENDMENT]
class CIM_LogicalDevice : CIM_EnabledLogicalElement
{
  string  SystemCreationClassName;
  string  SystemName;
  string  CreationClassName;
  string  DeviceID;
  boolean PowerManagementSupported;
  uint16  PowerManagementCapabilities[];
  uint16  Availability;
  uint16  StatusInfo;
  uint32  LastErrorCode;
  string  ErrorDescription;
  boolean ErrorCleared;
  string  OtherIdentifyingInfo[];
  uint64  PowerOnHours;
  uint64  TotalPowerOnHours;
  string  IdentifyingDescriptions[];
  uint16  AdditionalAvailability[];
  uint64  MaxQuiesceTime;
};
```

## <a name="members"></a>Members

La classe **CIM \_ LogicalDevice** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **CIM \_ LogicalDevice** presenta questi metodi.



| Metodo                                                           | Descrizione                                                                                                                                                                                                                              |
|:-----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnableDevice**](cim-logicaldevice-enabledevice.md)           | Questo metodo è deprecato. Usare invece il metodo **RequestStateChange** .<br/> **Descrizione deprecata:** Abilita o Disabilita il dispositivo logico.<br/>                                                                     |
| [**OnlineDevice**](cim-logicaldevice-onlinedevice.md)           | Questo metodo è deprecato. Usare invece il metodo **RequestStateChange** .<br/> **Descrizione deprecata:** Porta online il dispositivo logico, in modo che possa accettare le richieste oppure offline in modo che non possa più accettare richieste.<br/> |
| [**QuiesceDevice**](cim-logicaldevice-quiescedevice.md)         | Questo metodo è deprecato. Usare invece il metodo **RequestStateChange** .<br/> **Descrizione deprecata:** Sospende temporaneamente l'attività sul dispositivo logico o Abilita nuovamente l'attività.<br/>                            |
| [**Reset**](cim-logicaldevice-reset.md)                         | Reimposta il dispositivo logico.<br/>                                                                                                                                                                                                    |
| [**RestoreProperties**](cim-logicaldevice-restoreproperties.md) | Ripristina una configurazione precedente e lo stato del dispositivo logico.<br/>                                                                                                                                                            |
| [**SaveProperties**](cim-logicaldevice-saveproperties.md)       | Salva la configurazione e lo stato del dispositivo logico.<br/>                                                                                                                                                                      |
| [**SetPowerState**](cim-logicaldevice-setpowerstate.md)         | Questo metodo è deprecato. Usare invece la proprietà **SetPowerState** della classe **CIM \_ PowerManagementService** .<br/> **Descrizione deprecata:** Imposta lo stato di alimentazione del dispositivo logico.<br/>                       |



 

### <a name="properties"></a>Proprietà

La classe **CIM \_ LogicalDevice** dispone di queste proprietà.

<dl> <dt>

**AdditionalAvailability**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ LogicalDevice**.**Disponibilità**")
</dt> </dl>

Matrice che contiene le informazioni sulla disponibilità relative al dispositivo logico, oltre a quelle della proprietà di **disponibilità** .

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (2)


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

**Esecuzione/potenza completa** (3)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

**Avviso** (4)


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

**In test** (5)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Non applicabile** (6)


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

**Spegnimento (7** )


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

**Offline (8** )


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

**Off Duty** (9)


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Danneggiato** (10)


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

**Non installato** (11)


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

**Errore di installazione** (12)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

**Risparmio energia-sconosciuto** (13)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

**Risparmio energia-modalità a basso consumo** (14)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

**Risparmio energia-standby** (15)


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

**Ciclo di alimentazione** (16)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

**Risparmio energia-avviso** (17)


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

In **pausa** (18)


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

**Non pronto** (19)


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

**Non configurata** (20)


</dt> <dd></dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

**Inattivo** (21)


</dt> <dd></dd> </dl>

</dd> <dt>

**Disponibilità**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 006,5 "," MIB. IETF \| host-Resources-MIB. hrDeviceStatus "," MIF. DMTF \| Host Device \| 001,5 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ LogicalDevice**.**AdditionalAvailability**")
</dt> </dl>

Contiene la disponibilità del dispositivo logico.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (2)


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

**Esecuzione/potenza completa** (3)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

**Avviso** (4)


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

**In test** (5)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Non applicabile** (6)


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

**Spegnimento (7** )


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

**Offline (8** )


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

**Off Duty** (9)


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Danneggiato** (10)


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

**Non installato** (11)


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

**Errore di installazione** (12)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

**Risparmio energia-sconosciuto** (13)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

**Risparmio energia-modalità a basso consumo** (14)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

**Risparmio energia-standby** (15)


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

**Ciclo di alimentazione** (16)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

**Risparmio energia-avviso** (17)


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

In **pausa** (18)


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

**Non pronto** (19)


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

**Non configurata** (20)


</dt> <dd></dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

**Inattivo** (21)


</dt> <dd></dd> </dl>

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nome della classe utilizzato per creare un'istanza del dispositivo logico. **CreationClassName** è combinato con altre proprietà chiave di questa classe per identificare in modo univoco le istanze di questa classe e le relative sottoclassi.

</dd> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Identificatore univoco del dispositivo logico, ad esempio l'indirizzo.

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).**OperationalStatus**")
</dt> </dl>

Questa proprietà è deprecata. Usare invece la proprietà **OperationalStatus** della classe **CIM \_ ManagedSystemElement** .

**Descrizione deprecata:** Indica se un errore segnalato dalla proprietà **LastErrorCode** è deselezionato.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ DeviceErrorData. ErrorDescription")
</dt> </dl>

Questa proprietà è deprecata. Usare invece la proprietà **ErrorDescription** della classe **CIM \_ DeviceErrorData** .

**Descrizione deprecata:** Informazioni aggiuntive sull'errore segnalato dalla proprietà **LastErrorCode** .

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ LogicalDevice**.**OtherIdentifyingInfo**")
</dt> </dl>

Matrice di stringhe che descrivono gli elementi della matrice **OtherIdentifyingInfo** dello stesso indice.

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ DeviceErrorData. LastErrorCode")
</dt> </dl>

Questa proprietà è deprecata. Viene invece usata la proprietà **LastErrorCode** della classe **CIM \_ DeviceErrorData** .

**Descrizione deprecata:** Ultimo codice di errore segnalato dal dispositivo logico.

</dd> <dt>

**MaxQuiesceTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("nessun valore"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("millisecondi")
</dt> </dl>

Questa proprietà è deprecata e non deve essere usata.

**Descrizione deprecata:** Tempo massimo, in millisecondi, per cui un dispositivo può rimanere in uno stato temporaneamente disabilitato (le proprietà **Availability** e **AdditionalAvailability** sono impostate su "21" riposo). Il valore "0" indica che il dispositivo logico può rimanere in uno stato temporaneamente disabilitato per un periodo illimitato.

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ LogicalDevice**.**IdentifyingDescriptions**")
</dt> </dl>

Informazioni che identificano il dispositivo logico, diverso da **DeviceID**.

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ PowerManagementCapabilities. PowerCapabilities")
</dt> </dl>

Questa proprietà è deprecata. Usare invece la classe **CIM \_ PowerManagementCapabilities** .

**Descrizione deprecata:** Matrice che contiene le funzionalità di risparmio energia del dispositivo.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

**Non supportato** (1)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Disabilitato** (2)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Abilitato** (3)


</dt> <dd></dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

**Modalità di risparmio energia immesse automaticamente** (4)


</dt> <dd></dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

**Stato di alimentazione impostabile** (5)


</dt> <dd></dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

**Power Cycling supportato** (6)


</dt> <dd></dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

**Alimentazione temporizzata supportata** (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ PowerManagementCapabilities")
</dt> </dl>

Questa proprietà è deprecata. Usare invece la classe **PowerManagementCapabilities** .

**Descrizione deprecata: true** se il dispositivo logico può essere gestito dall'alimentazione; in caso contrario, **false**.

</dd> <dt>

**PowerOnHours**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("ore"), **contatore**
</dt> </dl>

Il numero di ore consecutive in cui il dispositivo logico è stato alimentato, dall'ultimo ciclo di alimentazione.

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Stato operativo DMTF \| 006,4 ")
</dt> </dl>

Questa proprietà è deprecata. Usare invece la classe **CIM \_ PowerManagementCapabilities** .

**Descrizione deprecata:** Indica se il dispositivo logico è abilitato o in uno stato correlato.

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

Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**")
</dt> </dl>

Nome della classe utilizzato per creare un'istanza del sistema che contiene il dispositivo logico. **SystemCreationClassName** è combinato con altre proprietà chiave di questa classe per identificare in modo univoco le istanze di questa classe e le relative sottoclassi.

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**")
</dt> </dl>

Nome del sistema che contiene il dispositivo logico.

</dd> <dt>

**TotalPowerOnHours**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("ore"), **contatore**
</dt> </dl>

Il numero totale di ore in cui il dispositivo logico è stato alimentato.

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

[**\_ENABLEDLOGICALELEMENT CIM**](cim-enabledlogicalelement.md)
</dt> </dl>

 


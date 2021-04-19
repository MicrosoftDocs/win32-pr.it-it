---
description: Rappresenta lo stato del componente dell'interfaccia del servizio Guest, che fornisce un meccanismo per interagire con la macchina virtuale dalle interfacce di gestione nel sistema host.
ms.assetid: 9A158B42-052B-42B3-8539-00927056306D
title: Classe Msvm_GuestServiceInterfaceComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceComponent
- Msvm_GuestServiceInterfaceComponent.Availability
- Msvm_GuestServiceInterfaceComponent.Caption
- Msvm_GuestServiceInterfaceComponent.ConfigManagerErrorCode
- Msvm_GuestServiceInterfaceComponent.ConfigManagerUserConfig
- Msvm_GuestServiceInterfaceComponent.CreationClassName
- Msvm_GuestServiceInterfaceComponent.Description
- Msvm_GuestServiceInterfaceComponent.DeviceID
- Msvm_GuestServiceInterfaceComponent.ErrorCleared
- Msvm_GuestServiceInterfaceComponent.ErrorDescription
- Msvm_GuestServiceInterfaceComponent.InstallDate
- Msvm_GuestServiceInterfaceComponent.LastErrorCode
- Msvm_GuestServiceInterfaceComponent.Name
- Msvm_GuestServiceInterfaceComponent.PNPDeviceID
- Msvm_GuestServiceInterfaceComponent.PowerManagementCapabilities
- Msvm_GuestServiceInterfaceComponent.PowerManagementSupported
- Msvm_GuestServiceInterfaceComponent.Status
- Msvm_GuestServiceInterfaceComponent.StatusInfo
- Msvm_GuestServiceInterfaceComponent.SystemCreationClassName
- Msvm_GuestServiceInterfaceComponent.SystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4c55417edeee6d9a9fb15c474ba4ee9ca2dd93f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307907"
---
# <a name="msvm_guestserviceinterfacecomponent-class"></a>\_Classe MSVM GuestServiceInterfaceComponent

Rappresenta lo stato del componente dell'interfaccia del servizio Guest, che fornisce un meccanismo per interagire con la macchina virtuale dalle interfacce di gestione nel sistema host. Questa classe deriva dalla classe [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) .

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestServiceInterfaceComponent : CIM_LogicalDevice
{
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a>Members

La **classe \_ GuestServiceInterfaceComponent di MSVM** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ GuestServiceInterfaceComponent di MSVM** dispone di questi metodi.



| Metodo                                                                               | Descrizione                                                                                                                              |
|:-------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [**RequestStateChange**](requeststatechange-msvm-guestserviceinterfacecomponent.md) | Richiede che lo stato del componente dell'interfaccia del servizio Guest venga modificato nel valore specificato.<br/>                           |
| [**Reset**](/windows/desktop/CIMWin32Prov/reset-method-in-class-cim-logicaldevice)                        | Richiede la reimpostazione del dispositivo logico. Non implementato da WMI.<br/>                                                               |
| [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-logicaldevice)        | Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato. Non implementato da WMI.<br/> |



 

### <a name="properties"></a>Proprietà

La **classe \_ GuestServiceInterfaceComponent di MSVM** dispone di queste proprietà.

<dl> <dt>

**Disponibilità**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Disponibilità e stato del dispositivo.



| Valore                                                                                                                                                                                                                                                                                                              | Significato                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <dt>**Other**</dt> <dt>1 (0x1)</dt> </dl>                                                                                          |                                                                                                             |
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Sconosciuto**</dt> <dt>2 (0x2)</dt> </dl>                                                                                  |                                                                                                             |
| <span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span><dl> <dt>**Running/complete Power**</dt> <dt>3 (0x3)</dt> </dl>                                      |                                                                                                             |
| <span id="Warning"></span><span id="warning"></span><span id="WARNING"></span><dl> <dt>**Avviso**</dt> <dt>4 (0x4)</dt> </dl>                                                                                  |                                                                                                             |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <dt>**Nel test**</dt> <dt>5 (0x5)</dt> </dl>                                                                                  |                                                                                                             |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <dt>**Non applicabile**</dt> <dt>6 (0x6)</dt> </dl>                                                      |                                                                                                             |
| <span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span><dl> <dt>**Spegnere**</dt> <dt>7 (0x7)</dt> </dl>                                                                          |                                                                                                             |
| <span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span><dl> <dt>**Off line**</dt> <dt>8 (0x8)</dt> </dl>                                                                              |                                                                                                             |
| <span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span><dl> <dt>**Off Duty**</dt> <dt>9 (0x9)</dt> </dl>                                                                              |                                                                                                             |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <dt>**Danneggiato**</dt> <dt>10 (0xA)</dt> </dl>                                                                             |                                                                                                             |
| <span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span><dl> <dt>**Non installato**</dt> <dt>11 (0xB)</dt> </dl>                                                         |                                                                                                             |
| <span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span><dl> <dt>**Errore di installazione**</dt> <dt>12 (0xC)</dt> </dl>                                                         |                                                                                                             |
| <span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span><dl> <dt>**Risparmio energia-sconosciuto**</dt> <dt>13 (0xD)</dt> </dl>                             | Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.<br/>                 |
| <span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span><dl> <dt>**Risparmio energia-modalità a basso consumo**</dt> <dt>14 (0xe)</dt> </dl> | Il dispositivo è in uno stato di risparmio energia ma funziona ancora e può presentare prestazioni ridotte.<br/> |
| <span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span><dl> <dt>**Risparmio energia-standby**</dt> <dt>15 (0xF)</dt> </dl>                             | Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.<br/>                        |
| <span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span><dl> <dt>**Ciclo di alimentazione**</dt> <dt>16 (0x10)</dt> </dl>                                                                |                                                                                                             |
| <span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span><dl> <dt>**Risparmio energia-avviso**</dt> <dt>17 (0x11)</dt> </dl>                            | Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.<br/>                              |



 

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione testuale dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**ConfigManagerErrorCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Codice di errore Win32 Configuration Manager.



| Valore                                                                                | Significato                                                                                                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl>   | Il dispositivo funziona correttamente.<br/>                                                                                                   |
| <dl> <dt>1 (0x1)</dt> </dl>   | Il dispositivo non è configurato correttamente.<br/>                                                                                           |
| <dl> <dt>2 (0x2)</dt> </dl>   | Windows non è in grado di caricare il driver per questo dispositivo.<br/>                                                                               |
| <dl> <dt>3 (0x3)</dt> </dl>   | Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.<br/>                             |
| <dl> <dt>4 (0x4)</dt> </dl>   | Il dispositivo non funziona correttamente. Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.<br/>                                        |
| <dl> <dt>5 (0x5)</dt> </dl>   | Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.<br/>                                                         |
| <dl> <dt>6 (0x6)</dt> </dl>   | La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.<br/>                                                               |
| <dl> <dt>7 (0x7)</dt> </dl>   | Impossibile filtrare.<br/>                                                                                                                |
| <dl> <dt>8 (0x8)</dt> </dl>   | Il caricatore driver del dispositivo è mancante.<br/>                                                                                      |
| <dl> <dt>9 (0x9)</dt> </dl>   | Il dispositivo non funziona correttamente; il firmware di controllo segnala erroneamente le risorse per il dispositivo.<br/>               |
| <dl> <dt>10 (0xA)</dt> </dl>  | Non è possibile avviare il dispositivo.<br/>                                                                                                          |
| <dl> <dt>11 (0xB)</dt> </dl>  | Errore del dispositivo.<br/>                                                                                                                |
| <dl> <dt>12 (0xC)</dt> </dl>  | Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.<br/>                                                                              |
| <dl> <dt>13 (0xD)</dt> </dl>  | Windows non è in grado di verificare le risorse del dispositivo.<br/>                                                                                 |
| <dl> <dt>14 (0xE)</dt> </dl>  | Il dispositivo non funziona correttamente finché il computer non viene riavviato.<br/>                                                                  |
| <dl> <dt>15 (0xF)</dt> </dl>  | Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.<br/>                                                      |
| <dl> <dt>16 (0x10)</dt> </dl> | Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.<br/>                                                            |
| <dl> <dt>17 (0x11)</dt> </dl> | Il dispositivo richiede un tipo di risorsa sconosciuto.<br/>                                                                                |
| <dl> <dt>18 (0x12)</dt> </dl> | È necessario reinstallare i driver di dispositivo.<br/>                                                                                           |
| <dl> <dt>19 (0x13)</dt> </dl> | Errore durante l'utilizzo del caricatore VxD.<br/>                                                                                                 |
| <dl> <dt>20 (0x14)</dt> </dl> | Il registro di sistema potrebbe essere danneggiato.<br/>                                                                                                  |
| <dl> <dt>21 (0x15)</dt> </dl> | Errore di sistema. Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware. Windows sta rimuovendo il dispositivo.<br/> |
| <dl> <dt>22 (0x16)</dt> </dl> | Il dispositivo è disabilitato.<br/>                                                                                                           |
| <dl> <dt>23 (0x17)</dt> </dl> | Errore di sistema. Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.<br/>                                 |
| <dl> <dt>24 (0x18)</dt> </dl> | Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.<br/>                                   |
| <dl> <dt>25 (0x19)</dt> </dl> | Windows sta ancora impostando il dispositivo.<br/>                                                                                       |
| <dl> <dt>26 (0x1A)</dt> </dl> | Windows sta ancora impostando il dispositivo.<br/>                                                                                       |
| <dl> <dt>27 (0x1B)</dt> </dl> | La configurazione del log del dispositivo non è valida.<br/>                                                                                 |
| <dl> <dt>28 (0x1C)</dt> </dl> | I driver di dispositivo non sono installati.<br/>                                                                                             |
| <dl> <dt>29 (0x1D)</dt> </dl> | Il dispositivo è disabilitato; il firmware del dispositivo non ha fornito le risorse necessarie.<br/>                                               |
| <dl> <dt>30 (0x1E)</dt> </dl> | Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.<br/>                                                                 |
| <dl> <dt>31 (0x1F)</dt> </dl> | Il dispositivo non funziona correttamente; Windows non è in grado di caricare i driver di dispositivo necessari.<br/>                                              |



 

</dd> <dt>

**ConfigManagerUserConfig**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **true**, il dispositivo usa una configurazione definita dall'utente.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di. Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione testuale dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **true**, l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa in formato libero che fornisce informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora di installazione dell'oggetto. Questa proprietà non richiede un valore per indicare che l'oggetto è installato. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ultimo codice di errore segnalato dal dispositivo logico.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Etichetta con cui l'oggetto è noto. Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**PNPDeviceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica l'identificatore del dispositivo Plug and Play Win32 del dispositivo logico.

Esempio: " \* PNP030b"

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico. Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.



| Valore                                                                                                                                                                                                                                                                                                                                                                 | Significato                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Sconosciuto**</dt> <dt>0 (0x0)</dt> </dl>                                                                                                                                     |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span><dl> <dt>**Non supportato**</dt> <dt>1 (0x1)</dt> </dl>                                                                                                             |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**Disabilitato**</dt> <dt>2 (0x2)</dt> </dl>                                                                                                                                 |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <dt>**Abilitato**</dt> <dt>3 (0x3)</dt> </dl>                                                                                                                                     | Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.<br/>                                                                                                                                                                                               |
| <span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span><dl> <dt>**Modalità di risparmio energia immesse automaticamente**</dt> <dt>4 (0x4)</dt> </dl> | Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.<br/>                                                                                                                                                                                                                                                   |
| <span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span><dl> <dt>**Stato di alimentazione impostabile**</dt> <dt>5 (0x5)</dt> </dl>                                                                                 | Il metodo [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) è supportato. Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato. Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).<br/> |
| <span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span><dl> <dt>**Power Cycling supportato**</dt> <dt>6 (0x6)</dt> </dl>                                                                     | Il metodo [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) può essere richiamato con il parametro *PowerState* impostato su 5 ("ciclo di alimentazione").<br/>                                                                                                                                                            |
| <span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span><dl> <dt>**Accensione temporizzata su supportata**</dt> <dt>7 (0x7)</dt> </dl>                                                                 | Il metodo [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) può essere richiamato con il parametro *PowerState* impostato su 5 ("ciclo di alimentazione") e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.<br/>                                                                                       |



 

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **true**, il dispositivo può essere gestito da energia elettrica, ovvero viene inserito in uno stato di risparmio energia. Se **false**, il valore intero 1 ("non supportato") deve essere l'unico elemento nella matrice **PowerManagementCapabilities** .

Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o se abilitate, quali funzionalità sono supportate. Per ulteriori informazioni, vedere la matrice **PowerManagementCapabilities** .

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato corrente dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

Sono inclusi i valori seguenti:

<dl><span id="OK"></span><span id="ok"></span><dt>

**OK**
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

**Errore**
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

**Degradato**
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

**Sconosciuto**
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

**"Errore di predazione"**
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

**Avvio**
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

**Arresto**
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

**Servizio**
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

**Sottolineato**
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

**"Non ripristino"**
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

**"Nessun contatto"**
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

**"Lost comm"**
</dt> </dl>

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato del dispositivo logico. Se questa proprietà non è applicabile al dispositivo logico, è necessario utilizzare il valore 5 ("non applicabile"). Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).

<dl> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1 (0x1))
</dt> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2 (0x2))
</dt> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3 (0x3))
</dt> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (4 (0x4))
</dt> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (5 (0x5))
</dt> </dl>

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della classe di creazione del sistema di ambito.

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del sistema di ambito.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                                            |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                                                 |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_LOGICALDEVICE CIM**](cim-logicaldevice.md)
</dt> <dt>

[**\_LOGICALDEVICE CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 


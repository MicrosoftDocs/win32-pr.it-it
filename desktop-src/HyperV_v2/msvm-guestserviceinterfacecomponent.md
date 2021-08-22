---
description: Rappresenta lo stato del componente dell'interfaccia del servizio guest, che fornisce un meccanismo per interagire con la macchina virtuale dalle interfacce di gestione nel sistema host.
ms.assetid: 9A158B42-052B-42B3-8539-00927056306D
title: Msvm_GuestServiceInterfaceComponent classe
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
ms.openlocfilehash: c7e404a1195332b508de22fc0a26dfebb96eba29f487f08505987edcc72b6cec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119523021"
---
# <a name="msvm_guestserviceinterfacecomponent-class"></a>Classe Msvm \_ GuestServiceInterfaceComponent

Rappresenta lo stato del componente dell'interfaccia del servizio guest, che fornisce un meccanismo per interagire con la macchina virtuale dalle interfacce di gestione nel sistema host. Questa classe deriva dalla [**classe CIM \_ LogicalDevice.**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)

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

La **classe Msvm \_ GuestServiceInterfaceComponent** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe Msvm \_ GuestServiceInterfaceComponent** dispone di questi metodi.



| Metodo                                                                               | Descrizione                                                                                                                              |
|:-------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [**RequestStateChange**](requeststatechange-msvm-guestserviceinterfacecomponent.md) | Richiede che lo stato del componente dell'interfaccia del servizio guest sia modificato nel valore specificato.<br/>                           |
| [**Reset**](/windows/desktop/CIMWin32Prov/reset-method-in-class-cim-logicaldevice)                        | Richiede una reimpostazione del dispositivo logico. Non implementato da WMI.<br/>                                                               |
| [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-logicaldevice)        | Definisce lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato. Non implementato da WMI.<br/> |



 

### <a name="properties"></a>Proprietà

La **classe Msvm \_ GuestServiceInterfaceComponent** ha queste proprietà.

<dl> <dt>

**Disponibilità**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Disponibilità e stato del dispositivo.



| Valore                                                                                                                                                                                                                                                                                                              | Significato                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <dt>**Altro**</dt> <dt>1 (0x1)</dt> </dl>                                                                                          |                                                                                                             |
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Sconosciuto**</dt> <dt>2 (0x2)</dt> </dl>                                                                                  |                                                                                                             |
| <span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span><dl> <dt>**Esecuzione/Alimentazione completa**</dt> <dt>3 (0x3)</dt> </dl>                                      |                                                                                                             |
| <span id="Warning"></span><span id="warning"></span><span id="WARNING"></span><dl> <dt>**Avviso**</dt> <dt>4 (0x4)</dt> </dl>                                                                                  |                                                                                                             |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <dt>**Nel test**</dt> <dt>5 (0x5)</dt> </dl>                                                                                  |                                                                                                             |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <dt>**Non applicabile**</dt> <dt>6 (0x6)</dt> </dl>                                                      |                                                                                                             |
| <span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span><dl> <dt>**Power Off**</dt> <dt>7 (0x7)</dt> </dl>                                                                          |                                                                                                             |
| <span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span><dl> <dt>**Off Line**</dt> <dt>8 (0x8)</dt> </dl>                                                                              |                                                                                                             |
| <span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span><dl> <dt>**Off Duty**</dt> <dt>9 (0x9)</dt> </dl>                                                                              |                                                                                                             |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <dt>**Degraded**</dt> <dt>10 (0xA)</dt> </dl>                                                                             |                                                                                                             |
| <span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span><dl> <dt>**Non installato**</dt> <dt>11 (0xB)</dt> </dl>                                                         |                                                                                                             |
| <span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span><dl> <dt>**Errore di installazione**</dt> <dt>12 (0xC)</dt> </dl>                                                         |                                                                                                             |
| <span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span><dl> <dt>**Risparmio energia - Sconosciuto**</dt> <dt>13 (0xD)</dt> </dl>                             | Il dispositivo è noto per essere in modalità risparmio energia, ma lo stato esatto è sconosciuto.<br/>                 |
| <span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span><dl> <dt>**Risparmio energia - Modalità risparmio energia**</dt> <dt>14 (0xE)</dt> </dl> | Il dispositivo è in stato di risparmio energia, ma funziona ancora e può presentare prestazioni ridotte.<br/> |
| <span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span><dl> <dt>**Risparmio energia - Standby**</dt> <dt>15 (0xF)</dt> </dl>                             | Il dispositivo non funziona, ma può essere portato a piena potenza rapidamente.<br/>                        |
| <span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span><dl> <dt>**Ciclo di alimentazione**</dt> <dt>16 (0x10)</dt> </dl>                                                                |                                                                                                             |
| <span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span><dl> <dt>**Risparmio energia - Avviso**</dt> <dt>17 (0x11)</dt> </dl>                            | Il dispositivo è in uno stato di avviso, anche se in modalità risparmio energia.<br/>                              |



 

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione testuale dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**ConfigManagerErrorCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Codice di errore Gestione configurazione Win32.



| Valore                                                                                | Significato                                                                                                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl>   | Il dispositivo funziona correttamente.<br/>                                                                                                   |
| <dl> <dt>1 (0x1)</dt> </dl>   | Il dispositivo non è configurato correttamente.<br/>                                                                                           |
| <dl> <dt>2 (0x2)</dt> </dl>   | Windows possibile caricare il driver per questo dispositivo.<br/>                                                                               |
| <dl> <dt>3 (0x3)</dt> </dl>   | Il driver per questo dispositivo potrebbe essere danneggiato o il sistema potrebbe avere memoria insufficiente o altre risorse.<br/>                             |
| <dl> <dt>4 (0x4)</dt> </dl>   | Il dispositivo non funziona correttamente. Uno dei relativi driver o il Registro di sistema potrebbe essere danneggiato.<br/>                                        |
| <dl> <dt>5 (0x5)</dt> </dl>   | Il driver per il dispositivo richiede una risorsa che Windows non può gestire.<br/>                                                         |
| <dl> <dt>6 (0x6)</dt> </dl>   | La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.<br/>                                                               |
| <dl> <dt>7 (0x7)</dt> </dl>   | Impossibile filtrare.<br/>                                                                                                                |
| <dl> <dt>8 (0x8)</dt> </dl>   | Il caricatore del driver per il dispositivo è mancante.<br/>                                                                                      |
| <dl> <dt>9 (0x9)</dt> </dl>   | Il dispositivo non funziona correttamente. il firmware di controllo segnala erroneamente le risorse per il dispositivo.<br/>               |
| <dl> <dt>10 (0xA)</dt> </dl>  | Impossibile avviare il dispositivo.<br/>                                                                                                          |
| <dl> <dt>11 (0xB)</dt> </dl>  | Dispositivo non riuscito.<br/>                                                                                                                |
| <dl> <dt>12 (0xC)</dt> </dl>  | Il dispositivo non riesce a trovare risorse gratuite sufficienti da usare.<br/>                                                                              |
| <dl> <dt>13 (0xD)</dt> </dl>  | Windows possibile verificare le risorse del dispositivo.<br/>                                                                                 |
| <dl> <dt>14 (0xE)</dt> </dl>  | Il dispositivo non può funzionare correttamente fino al riavvio del computer.<br/>                                                                  |
| <dl> <dt>15 (0xF)</dt> </dl>  | Il dispositivo non funziona correttamente a causa di un possibile problema di enumerazione.<br/>                                                      |
| <dl> <dt>16 (0x10)</dt> </dl> | Windows identificare tutte le risorse utilizzate dal dispositivo.<br/>                                                            |
| <dl> <dt>17 (0x11)</dt> </dl> | Il dispositivo richiede un tipo di risorsa sconosciuto.<br/>                                                                                |
| <dl> <dt>18 (0x12)</dt> </dl> | I driver di dispositivo devono essere reinstallati.<br/>                                                                                           |
| <dl> <dt>19 (0x13)</dt> </dl> | Errore durante l'uso del caricatore VxD.<br/>                                                                                                 |
| <dl> <dt>20 (0x14)</dt> </dl> | Il Registro di sistema potrebbe essere danneggiato.<br/>                                                                                                  |
| <dl> <dt>21 (0x15)</dt> </dl> | Errore di sistema. Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware. Windows sta rimuovendo il dispositivo.<br/> |
| <dl> <dt>22 (0x16)</dt> </dl> | Il dispositivo è disabilitato.<br/>                                                                                                           |
| <dl> <dt>23 (0x17)</dt> </dl> | Errore di sistema. Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.<br/>                                 |
| <dl> <dt>24 (0x18)</dt> </dl> | Il dispositivo non è presente, non funziona correttamente o non dispone di tutti i relativi driver installati.<br/>                                   |
| <dl> <dt>25 (0x19)</dt> </dl> | Windows sta ancora configurando il dispositivo.<br/>                                                                                       |
| <dl> <dt>26 (0x1A)</dt> </dl> | Windows sta ancora configurando il dispositivo.<br/>                                                                                       |
| <dl> <dt>27 (0x1B)</dt> </dl> | Il dispositivo non ha una configurazione di log valida.<br/>                                                                                 |
| <dl> <dt>28 (0x1C)</dt> </dl> | I driver di dispositivo non sono installati.<br/>                                                                                             |
| <dl> <dt>29 (0x1D)</dt> </dl> | Il dispositivo è disabilitato. il firmware del dispositivo non ha fornito le risorse necessarie.<br/>                                               |
| <dl> <dt>30 (0x1E)</dt> </dl> | Il dispositivo usa una risorsa IRQ in uso da un altro dispositivo.<br/>                                                                 |
| <dl> <dt>31 (0x1F)</dt> </dl> | Il dispositivo non funziona correttamente. Windows possibile caricare i driver di dispositivo necessari.<br/>                                              |



 

</dd> <dt>

**ConfigManagerUserConfig**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **TRUE,** il dispositivo usa una configurazione definita dall'utente.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della classe o della sottoclasse utilizzata nella creazione di un'istanza. Se usata con altre proprietà chiave della classe , questa proprietà consente l'identificazione univoca di tutte le istanze della classe e delle relative sottoclassi.

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione testuale dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**Deviceid**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **TRUE,** l'errore segnalato nella **proprietà LastErrorCode** viene ora cancellato.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa in formato libero che fornisce informazioni sull'errore registrato nella proprietà **LastErrorCode** e sulle azioni correttive da eseguire.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora di installazione dell'oggetto. Questa proprietà non richiede un valore per indicare che l'oggetto è installato. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ultimo codice di errore segnalato dal dispositivo logico.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Etichetta con cui l'oggetto è noto. Quando è sottoclassata, questa proprietà può essere sottoposta a override per essere una proprietà chiave. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**PNPDeviceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica l'identificatore Plug and Play dispositivo win32 del dispositivo logico.

Esempio: \* "PNP030b"

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice delle funzionalità specifiche correlate all'alimentazione di un dispositivo logico. Questa proprietà viene ereditata da **CIM \_ LogicalDevice.**



| Valore                                                                                                                                                                                                                                                                                                                                                                 | Significato                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Sconosciuto**</dt> <dt>0 (0x0)</dt> </dl>                                                                                                                                     |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span><dl> <dt>**Non supportato**</dt> <dt>1 (0x1)</dt> </dl>                                                                                                             |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**Disabilitato**</dt> <dt>2 (0x2)</dt> </dl>                                                                                                                                 |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <dt>**Abilitato**</dt> <dt>3 (0x3)</dt> </dl>                                                                                                                                     | Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto o le informazioni non sono disponibili.<br/>                                                                                                                                                                                               |
| <span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span><dl> <dt>**Modalità risparmio energia immesse automaticamente**</dt> <dt>4 (0x4)</dt> </dl> | Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.<br/>                                                                                                                                                                                                                                                   |
| <span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span><dl> <dt>**Power State Settable**</dt> <dt>5 (0x5)</dt> </dl>                                                                                 | Il [**metodo SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) è supportato. Questo metodo si trova nella classe **CIM \_ LogicalDevice** padre e può essere implementato. Per altre informazioni, vedere [Progettazione di Managed Object Format (MOF).](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)<br/> |
| <span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span><dl> <dt>**Power Cycling supportato**</dt> <dt>6 (0x6)</dt> </dl>                                                                     | Il [**metodo SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) può essere richiamato con il *parametro PowerState* impostato su 5 ("Ciclo di alimentazione").<br/>                                                                                                                                                            |
| <span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span><dl> <dt>**Alimentazione a tempo supportata**</dt> <dt>7 (0x7)</dt> </dl>                                                                 | Il [**metodo SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) può essere richiamato con il parametro *PowerState* impostato su 5 ("Ciclo di alimentazione") e *Time* impostato su una data e un'ora o un intervallo specifici per l'accensione.<br/>                                                                                       |



 

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **TRUE,** il dispositivo può essere gestito dall'alimentazione, vale a dire inserito in uno stato di risparmio energia. Se **FALSE,** il valore intero 1 ("Non supportato") deve essere l'unica voce nella matrice **PowerManagementCapabilities.**

Questa proprietà non indica se le funzionalità di risparmio energia sono attualmente abilitate o, se abilitate, quali funzionalità sono supportate. Per altre informazioni, vedere la matrice **PowerManagementCapabilities.**

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato corrente dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

Sono inclusi i valori seguenti:

<dl><span id="OK"></span><span id="ok"></span><dt>

**"OK"**
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

**"Errore"**
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

**"Degraded"**
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

**"Sconosciuto"**
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

**"Pred Fail"**
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

**"Avvio"**
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

**"Arresto"**
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

**"Servizio"**
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

**"Stressed"**
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

**"NonRecover"**
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

**"Nessun contatto"**
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

**"Lost Comm"**
</dt> </dl>

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato del dispositivo logico. Se questa proprietà non si applica al dispositivo logico, deve essere usato il valore 5 ("Non applicabile"). Questa proprietà viene ereditata da [**CIM \_ LogicalDevice.**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)

<dl> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1 (0x1))
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

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della classe di creazione del sistema di ambito.

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del sistema di ambito.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Server 2012 Solo app desktop R2 \[\]<br/>                                                 |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> <dt>

[**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 


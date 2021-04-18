---
description: Rappresenta le impostazioni per il servizio di virtualizzazione presenti in un singolo sistema host.
ms.assetid: E3265AFE-0117-4F59-9A6B-34CEA7A61EDD
title: Classe Msvm_VirtualSystemManagementServiceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementServiceSettingData
- Msvm_VirtualSystemManagementServiceSettingData.InstanceID
- Msvm_VirtualSystemManagementServiceSettingData.Caption
- Msvm_VirtualSystemManagementServiceSettingData.Description
- Msvm_VirtualSystemManagementServiceSettingData.ElementName
- Msvm_VirtualSystemManagementServiceSettingData.BiosLockString
- Msvm_VirtualSystemManagementServiceSettingData.DefaultExternalDataRoot
- Msvm_VirtualSystemManagementServiceSettingData.DefaultVirtualHardDiskPath
- Msvm_VirtualSystemManagementServiceSettingData.MaximumMacAddress
- Msvm_VirtualSystemManagementServiceSettingData.MinimumMacAddress
- Msvm_VirtualSystemManagementServiceSettingData.NumaSpanningEnabled
- Msvm_VirtualSystemManagementServiceSettingData.PrimaryOwnerContact
- Msvm_VirtualSystemManagementServiceSettingData.PrimaryOwnerName
- Msvm_VirtualSystemManagementServiceSettingData.HbaLunTimeout
- Msvm_VirtualSystemManagementServiceSettingData.MaximumWWPNAddress
- Msvm_VirtualSystemManagementServiceSettingData.MinimumWWPNAddress
- Msvm_VirtualSystemManagementServiceSettingData.CurrentWWNNAddress
- Msvm_VirtualSystemManagementServiceSettingData.DefaultVirtualHardDiskCachingMode
- Msvm_VirtualSystemManagementServiceSettingData.HypervisorRootSchedulerEnabled
- Msvm_VirtualSystemManagementServiceSettingData.EnhancedSessionModeEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 782f196fdbd3a09126a7b4d14be6789bb633f043
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305997"
---
# <a name="msvm_virtualsystemmanagementservicesettingdata-class"></a>\_Classe MSVM VirtualSystemManagementServiceSettingData

Rappresenta le impostazioni per il servizio di virtualizzazione presenti in un singolo sistema host. Non è possibile modificare direttamente le proprietà di questa classe. Il client deve chiamare il metodo [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) per modificare una di queste proprietà.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemManagementServiceSettingData : CIM_SettingData
{
  string  InstanceID = "Microsoft:host";
  string  Caption = "Hyper-V Virtual System Management Service";
  string  Description = "Settings for the Virtual System Management Service";
  string  ElementName = "Hyper-V Virtual System Management Service";
  string  BiosLockString;
  string  DefaultExternalDataRoot = "root\ProgramData\Microsoft\Windows\Virtualization";
  string  DefaultVirtualHardDiskPath = "root\Users\Public\Documents\Virtual Hard Disks";
  string  MaximumMacAddress;
  string  MinimumMacAddress;
  boolean NumaSpanningEnabled;
  string  PrimaryOwnerContact = "";
  string  PrimaryOwnerName = "Administrators";
  uint32  HbaLunTimeout;
  string  MaximumWWPNAddress;
  string  MinimumWWPNAddress;
  string  CurrentWWNNAddress;
  uint16  DefaultVirtualHardDiskCachingMode;
  boolean HypervisorRootSchedulerEnabled;
  boolean EnhancedSessionModeEnabled;
};
```

## <a name="members"></a>Members

La **classe \_ VirtualSystemManagementServiceSettingData di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ VirtualSystemManagementServiceSettingData di MSVM** dispone di queste proprietà.

<dl> <dt>

**BiosLockString**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32)
</dt> </dl>

Utilizzato dagli OEM per consentire l'esecuzione dei sistemi operativi Windows bloccati dal BIOS nella macchina virtuale. La lunghezza della stringa deve corrispondere esattamente a 32 caratteri.

Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Hyper-V Virtual System Management Service".

</dd> <dt>

**CurrentWWNNAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo del nome del nodo universale (WWNN) per gli indirizzi del nome universale generati dinamicamente utilizzati per le schede del bus host sintetico.

Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

</dd> <dt>

**DefaultExternalDataRoot**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md).**ConfigurationDataRoot**")
</dt> </dl>

Radice dati esterna predefinita. Per impostazione predefinita, "*root* \\ ProgramData \\ Microsoft \\ Windows \\ Virtualization".

Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

</dd> <dt>

**DefaultVirtualHardDiskCachingMode**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la memorizzazione nella cache dei file in memoria deve essere utilizzata per i dischi per impostazione predefinita. È possibile eseguire l'override di questo valore in base al disco nel campo **CachingMode** della classe [**\_ StorageAllocationSettingData di MSVM**](msvm-storageallocationsettingdata.md) .

> [!Note]  
> Aggiunta in Windows 10 e Windows Server 2016.

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="No_Caching"></span><span id="no_caching"></span><span id="NO_CACHING"></span>

**Nessuna memorizzazione nella cache** (3)


</dt> <dd></dd> <dt>

<span id="Cache_Sharable_Parents"></span><span id="cache_sharable_parents"></span><span id="CACHE_SHARABLE_PARENTS"></span>

**Memorizzare nella cache elementi padre condivisibili** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**DefaultVirtualHardDiskPath**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso predefinito del disco rigido virtuale. Per impostazione predefinita, "utenti *radice* \\ \\ \\ documenti pubblici \\ dischi rigidi virtuali".

Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Settings for the Virtual System Management Service".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per l'oggetto. Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Hyper-V Virtual System Management Service". La modifica di questa proprietà comporterà la modifica della proprietà **ElementName** del derivato [**\_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) associato.

</dd> <dt>

**EnhancedSessionModeEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se nel server è consentita la modalità sessione avanzata. **True** indica consentito, in caso contrario **false**.

**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.

</dd> <dt>

**HbaLunTimeout**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica il periodo di tempo durante il quale il dispositivo virtuale Fibre Channel sintetico attenderà che venga visualizzato un numero di unità logica (LUN) prima di avviare una macchina virtuale.

Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

</dd> <dt>

**HypervisorRootSchedulerEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se l'utilità di pianificazione radice dell'hypervisor è abilitata o meno.

> [!Note]  
> Aggiunta in Windows 10, versione 1709.

 

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Identifica in modo univoco un'istanza di questa classe. Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))ed è sempre impostata su "Microsoft:*host*", dove *host* è il nome NetBIOS del sistema di hosting del computer.

</dd> <dt>

**MaximumMacAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo MAC massimo per gli indirizzi MAC generati dinamicamente.

Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

</dd> <dt>

**MaximumWWPNAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo WWPN (World Wide Port Name) per gli indirizzi del nome universale generati dinamicamente utilizzati per le schede del bus host sintetico.

Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

</dd> <dt>

**MinimumMacAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo MAC minimo per gli indirizzi MAC generati dinamicamente.

Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

</dd> <dt>

**MinimumWWPNAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo del nome della porta universale minimo per gli indirizzi del nome universale generati dinamicamente utilizzati per le schede del bus host sintetico.

Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

</dd> <dt>

**NumaSpanningEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se è possibile allocare memoria dai nodi NUMA (non-Uniform Memory Access) remoti quando si avvia una macchina virtuale o quando si assegna memoria a una macchina virtuale tramite la memoria dinamica. Può corrispondere a uno dei valori seguenti.



| Valore                                                                                | Significato                                                                                     |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**Vero**</dt> </dl>  | La memoria può essere allocata dai nodi NUMA locali e remoti.<br/>                   |
| <dl> <dt>**False**</dt> </dl> | La memoria può essere allocata solo dal nodo NUMA assegnato alla macchina virtuale.<br/> |



 

Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

</dd> <dt>

**PrimaryOwnerContact**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| informazioni generali \| 001,4 ")
</dt> </dl>

Viene descritto come è possibile raggiungere il proprietario del sistema primario, ad esempio il numero di telefono o l'indirizzo di posta elettronica. Per impostazione predefinita, è vuoto. Il nome non può superare i 256 caratteri.

Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

</dd> <dt>

**PrimaryOwnerName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| informazioni generali \| 001,3 ")
</dt> </dl>

Nome del proprietario del sistema primario. Per impostazione predefinita, "Administrators". Questo valore non può superare i 64 caratteri.

Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe \_ VirtualSystemManagementServiceSettingData di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETTINGDATA CIM**](cim-settingdata.md)
</dt> <dt>

[**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)
</dt> <dt>

[**\_SETTINGDATA CIM**](/previous-versions//cc136911(v=vs.85))
</dt> <dt>

[Classi di gestione del sistema virtuale](virtual-system-management-classes.md)
</dt> </dl>

 


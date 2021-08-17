---
description: Rappresenta le impostazioni per il servizio di virtualizzazione presente in un singolo sistema host.
ms.assetid: E3265AFE-0117-4F59-9A6B-34CEA7A61EDD
title: Msvm_VirtualSystemManagementServiceSettingData classe
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
ms.openlocfilehash: 3ccb0a1a9bc4a10ec7f8a366f012446e0374dab299f8ee779f16cfeb38fb005b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147974"
---
# <a name="msvm_virtualsystemmanagementservicesettingdata-class"></a>Classe Msvm \_ VirtualSystemManagementServiceSettingData

Rappresenta le impostazioni per il servizio di virtualizzazione presente in un singolo sistema host. Le proprietà per questa classe non possono essere modificate direttamente. Il client deve chiamare il [**metodo ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) della [**classe Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) per modificare una di queste proprietà.

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

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

La **classe Msvm \_ VirtualSystemManagementServiceSettingData** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ VirtualSystemManagementServiceSettingData** ha queste proprietà.

<dl> <dt>

**BiosLockString**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32)
</dt> </dl>

Usato dagli OEM per consentire l'esecuzione di sistemi operativi Windows bioS bloccati nella macchina virtuale. La lunghezza di questa stringa deve essere esattamente di 32 caratteri.

Si tratta di una proprietà di sola lettura, ma può essere modificata usando il [**metodo ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) della [**classe Msvm \_ VirtualSystemManagementService.**](msvm-virtualsystemmanagementservice.md)

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Servizio di gestione del sistema virtuale Hyper-V".

</dd> <dt>

**CurrentWWNNAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo WWNN (World Wide Node Name) per gli indirizzi world wide name generati dinamicamente usati per le schede bus host sintetiche.

Si tratta di una proprietà di sola lettura, ma può essere modificata usando il [**metodo ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) della [**classe Msvm \_ VirtualSystemManagementService.**](msvm-virtualsystemmanagementservice.md)

</dd> <dt>

**DefaultExternalDataRoot**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md).**ConfigurationDataRoot**")
</dt> </dl>

Radice dei dati esterni predefinita. Per impostazione predefinita,*"root* \\ ProgramData Microsoft Windows \\ \\ \\ Virtualization".

Si tratta di una proprietà di sola lettura, ma può essere modificata usando il [**metodo ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) della [**classe Msvm \_ VirtualSystemManagementService.**](msvm-virtualsystemmanagementservice.md)

</dd> <dt>

**DefaultVirtualHardDiskCachingMode**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la memorizzazione nella cache dei file in memoria deve essere usata per i dischi per impostazione predefinita. Questo valore può essere sottoposto a override per ogni disco nel campo **CachingMode** della [**classe Msvm \_ StorageAllocationSettingData.**](msvm-storageallocationsettingdata.md)

> [!Note]  
> Aggiunta in Windows 10 e Windows Server 2016.

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="No_Caching"></span><span id="no_caching"></span><span id="NO_CACHING"></span>

**Nessuna Caching** (3)


</dt> <dd></dd> <dt>

<span id="Cache_Sharable_Parents"></span><span id="cache_sharable_parents"></span><span id="CACHE_SHARABLE_PARENTS"></span>

**Cache Sharable Parents** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**DefaultVirtualHardDiskPath**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso predefinito del disco rigido virtuale. Per impostazione predefinita,*"root* \\ Users Public Documents Virtual Hard \\ \\ \\ Disks".

Si tratta di una proprietà di sola lettura, ma può essere modificata usando il [**metodo ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) della [**classe Msvm \_ VirtualSystemManagementService.**](msvm-virtualsystemmanagementservice.md)

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Impostazioni per il servizio Virtual System Management".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per l'oggetto . Questa proprietà viene ereditata da [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Servizio di gestione del sistema virtuale Hyper-V". La modifica di questa proprietà modificherà **la proprietà ElementName** del derivato [**\_ CiM LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) associato.

</dd> <dt>

**EnhancedSessionModeEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la modalità sessione avanzata è consentita nel server. **True** indica consentito, in caso contrario **False.**

**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.

</dd> <dt>

**HbaLunTimeout**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica per quanto tempo il dispositivo Fibre Channel virtuale attenderà la visualizzazione di un numero di unità logica (LUN) prima di avviare una macchina virtuale.

Si tratta di una proprietà di sola lettura, ma può essere modificata usando il [**metodo ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) della [**classe Msvm \_ VirtualSystemManagementService.**](msvm-virtualsystemmanagementservice.md)

</dd> <dt>

**HypervisorRootSchedulerEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se l'utilità di pianificazione radice dell'hypervisor è abilitata o meno.

> [!Note]  
> Aggiunta in Windows 10, versione 1709.

 

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Chiave**
</dt> </dl>

Identifica in modo univoco un'istanza di questa classe. Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))ed è sempre impostata su "Microsoft:*host",* dove *host* è il nome NetBIOS del computer host.

</dd> <dt>

**MaximumMacAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo MAC massimo per gli indirizzi MAC generati dinamicamente.

Si tratta di una proprietà di sola lettura, ma può essere modificata usando il [**metodo ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) della [**classe Msvm \_ VirtualSystemManagementService.**](msvm-virtualsystemmanagementservice.md)

</dd> <dt>

**MaximumWWPNAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo WWPN (World Wide Port Name) massimo per gli indirizzi world wide name generati dinamicamente usati per le schede bus host sintetiche.

Si tratta di una proprietà di sola lettura, ma può essere modificata usando il [**metodo ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) della [**classe Msvm \_ VirtualSystemManagementService.**](msvm-virtualsystemmanagementservice.md)

</dd> <dt>

**MinimumMacAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo MAC minimo per gli indirizzi MAC generati dinamicamente.

Si tratta di una proprietà di sola lettura, ma può essere modificata usando il [**metodo ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) della [**classe Msvm \_ VirtualSystemManagementService.**](msvm-virtualsystemmanagementservice.md)

</dd> <dt>

**MinimumWWPNAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo minimo del nome della porta a livello mondiale per gli indirizzi world wide name generati dinamicamente usati per le schede bus host sintetiche.

Si tratta di una proprietà di sola lettura, ma può essere modificata usando il [**metodo ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) della [**classe Msvm \_ VirtualSystemManagementService.**](msvm-virtualsystemmanagementservice.md)

</dd> <dt>

**NumaSpanningEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se la memoria può essere allocata da nodi NUMA (Remote NonUniform Memory Access) quando si avvia una macchina virtuale o quando si assegna memoria a una macchina virtuale tramite memoria dinamica. Può essere uno dei valori seguenti.



| Valore                                                                                | Significato                                                                                     |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**Vero**</dt> </dl>  | La memoria può essere allocata da nodi NUMA locali e remoti.<br/>                   |
| <dl> <dt>**Falso**</dt> </dl> | La memoria può essere allocata solo dal nodo NUMA assegnato alla macchina virtuale.<br/> |



 

Si tratta di una proprietà di sola lettura, ma può essere modificata usando il [**metodo ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) della [**classe Msvm \_ VirtualSystemManagementService.**](msvm-virtualsystemmanagementservice.md)

</dd> <dt>

**PrimaryOwnerContact**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. INFORMAZIONI \| GENERALI DMTF \| 001.4")
</dt> </dl>

Descrive come è possibile raggiungere il proprietario del sistema primario, ad esempio il numero di telefono o l'indirizzo di posta elettronica. Per impostazione predefinita, vuoto. Questo nome non può superare i 256 caratteri.

Si tratta di una proprietà di sola lettura, ma può essere modificata usando il [**metodo ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) della [**classe Msvm \_ VirtualSystemManagementService.**](msvm-virtualsystemmanagementservice.md)

</dd> <dt>

**PrimaryOwnerName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DmTF \| General Information \| 001.3")
</dt> </dl>

Nome del proprietario del sistema primario. Per impostazione predefinita, "Administrators". Questo valore non può superare i 64 caratteri.

Si tratta di una proprietà di sola lettura, ma può essere modificata usando il [**metodo ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) della [**classe Msvm \_ VirtualSystemManagementService.**](msvm-virtualsystemmanagementservice.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe Msvm \_ VirtualSystemManagementServiceSettingData** potrebbe essere limitato dal filtro del controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> <dt>

[**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)
</dt> <dt>

[**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))
</dt> <dt>

[Classi di gestione del sistema virtuale](virtual-system-management-classes.md)
</dt> </dl>

 


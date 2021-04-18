---
description: Fornisce informazioni aggiuntive da utilizzare con il metodo ExportSystemDefinition della \_ classe VirtualSystemManagementService di MSVM.
ms.assetid: 86396A76-83EC-476E-86A9-83861A002152
title: Classe Msvm_VirtualSystemExportSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemExportSettingData
- Msvm_VirtualSystemExportSettingData.CaptureLiveState
- Msvm_VirtualSystemExportSettingData.InstanceID
- Msvm_VirtualSystemExportSettingData.Caption
- Msvm_VirtualSystemExportSettingData.Description
- Msvm_VirtualSystemExportSettingData.ElementName
- Msvm_VirtualSystemExportSettingData.CopySnapshotConfiguration
- Msvm_VirtualSystemExportSettingData.CopyVmRuntimeInformation
- Msvm_VirtualSystemExportSettingData.CopyVmStorage
- Msvm_VirtualSystemExportSettingData.CreateVmExportSubdirectory
- Msvm_VirtualSystemExportSettingData.SnapshotVirtualSystem
- Msvm_VirtualSystemExportSettingData.BackupIntent
- Msvm_VirtualSystemExportSettingData.ExportForLiveMigration
- Msvm_VirtualSystemExportSettingData.DisableDifferentialOfIgnoredStorage
- Msvm_VirtualSystemExportSettingData.ExcludedVirtualHardDisks
- Msvm_VirtualSystemExportSettingData.DifferentialBackupBase
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 77bd451912063ec1164abf14247d81e1d258f56f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306016"
---
# <a name="msvm_virtualsystemexportsettingdata-class"></a>\_Classe MSVM VirtualSystemExportSettingData

Fornisce informazioni aggiuntive da utilizzare con il metodo [**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) della classe [**\_ VirtualSystemManagementService di MSVM**](msvm-virtualsystemmanagementservice.md) .

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemExportSettingData : CIM_SettingData
{
  uint8   CaptureLiveState;
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  uint8   CopySnapshotConfiguration;
  boolean CopyVmRuntimeInformation;
  boolean CopyVmStorage;
  boolean CreateVmExportSubdirectory;
  string  SnapshotVirtualSystem;
  uint8   BackupIntent;
  boolean ExportForLiveMigration;
  boolean DisableDifferentialOfIgnoredStorage;
  string  ExcludedVirtualHardDisks[];
  string  DifferentialBackupBase;
};
```

## <a name="members"></a>Members

La **classe \_ VirtualSystemExportSettingData di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ VirtualSystemExportSettingData di MSVM** dispone di queste proprietà.

<dl> <dt>

**BackupIntent**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indica l'intenzione di utilizzare i set di backup esportati.

> [!Note]  
> Questa proprietà è stata aggiunta in Windows 10 e Windows Server 2016.

 

<dt>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>**BackupIntentPreserveChain** (0)


</dt> <dd>

Tutti i set di backup completi e differenziali esportati verranno conservati così come sono.

</dd> <dt>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>**BackupIntentMerge** (1)


</dt> <dd>

I set di backup completi e differenziali esportati verranno uniti per sintetizzare set di backup completi.

</dd> </dl>

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **maxlen** (64)
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**CaptureLiveState**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indica lo stato da acquisire se la destinazione dell'esportazione è una macchina virtuale in esecuzione.

<dt>

<span id="CaptureCrashConsistentState"></span><span id="capturecrashconsistentstate"></span><span id="CAPTURECRASHCONSISTENTSTATE"></span>

<span id="CaptureCrashConsistentState"></span><span id="capturecrashconsistentstate"></span><span id="CAPTURECRASHCONSISTENTSTATE"></span>**CaptureCrashConsistentState** (0)


</dt> <dd>

Nessun file di stato salvato verrà esportato per la macchina virtuale in esecuzione, inserendolo in uno stato di arresto anomalo.

</dd> <dt>

<span id="CaptureSavedState"></span><span id="capturesavedstate"></span><span id="CAPTURESAVEDSTATE"></span>

<span id="CaptureSavedState"></span><span id="capturesavedstate"></span><span id="CAPTURESAVEDSTATE"></span>**CaptureSavedState** (1)


</dt> <dd>

I file di stato salvati per la macchina virtuale in esecuzione verranno esportati insieme alla configurazione della macchina virtuale.

</dd> <dt>

<span id="CaptureAppConsistentState"></span><span id="captureappconsistentstate"></span><span id="CAPTUREAPPCONSISTENTSTATE"></span>

<span id="CaptureAppConsistentState"></span><span id="captureappconsistentstate"></span><span id="CAPTUREAPPCONSISTENTSTATE"></span>**CaptureAppConsistentState** (2)


</dt> <dd>

Viene esportato lo stato coerente con l'applicazione della macchina virtuale in esecuzione.

> [!Note]  
> Aggiunta in Windows 10 e Windows Server 2016.

 

</dd> </dl>

</dd> <dt>

**CopySnapshotConfiguration**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indica quali snapshot devono essere esportati con la macchina virtuale.

<dt>

<span id="ExportAllSnapshots"></span><span id="exportallsnapshots"></span><span id="EXPORTALLSNAPSHOTS"></span>

<span id="ExportAllSnapshots"></span><span id="exportallsnapshots"></span><span id="EXPORTALLSNAPSHOTS"></span>**ExportAllSnapshots** (0)


</dt> <dd>

Tutti gli snapshot verranno esportati con la macchina virtuale.

</dd> <dt>

<span id="ExportNoSnapshots"></span><span id="exportnosnapshots"></span><span id="EXPORTNOSNAPSHOTS"></span>

<span id="ExportNoSnapshots"></span><span id="exportnosnapshots"></span><span id="EXPORTNOSNAPSHOTS"></span>**ExportNoSnapshots** (1)


</dt> <dd>

Non verranno esportati snapshot con la macchina virtuale.

</dd> <dt>

<span id="ExportOneSnapshot"></span><span id="exportonesnapshot"></span><span id="EXPORTONESNAPSHOT"></span>

<span id="ExportOneSnapshot"></span><span id="exportonesnapshot"></span><span id="EXPORTONESNAPSHOT"></span>**ExportOneSnapshot** (2)


</dt> <dd>

Gli snapshot identificati dalla proprietà **SnapshotVirtualSystem** verranno esportati con la macchina virtuale. Le proprietà **CopyVmStorage** e **CopyVmRuntimeInformation** vengono ignorate, le informazioni sull'archiviazione e la fase di esecuzione vengono esportate con la macchina virtuale e tutti i dischi differenze VHD verranno uniti in un nuovo disco rigido virtuale.

</dd> <dt>

<span id="ExportOneSnapshotForBackup"></span><span id="exportonesnapshotforbackup"></span><span id="EXPORTONESNAPSHOTFORBACKUP"></span>

<span id="ExportOneSnapshotForBackup"></span><span id="exportonesnapshotforbackup"></span><span id="EXPORTONESNAPSHOTFORBACKUP"></span>**ExportOneSnapshotForBackup** (3)


</dt> <dd>

Lo snapshot identificato dalla proprietà **SnapshotVirtualSystem** verrà esportato allo scopo di eseguire il backup della macchina virtuale. La configurazione esportata userà l'ID della macchina virtuale.

> [!Note]  
> Aggiunta in Windows 10 e Windows Server 2016.

 

</dd> </dl>

</dd> <dt>

**CopyVmRuntimeInformation**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indica se le informazioni di runtime della macchina virtuale verranno copiate quando viene esportata la macchina virtuale.



| Valore                                                                                | Significato                                                                 |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**Vero**</dt> </dl>  | Verranno copiate le informazioni sulla fase di esecuzione della macchina virtuale.<br/>     |
| <dl> <dt>**False**</dt> </dl> | Le informazioni di run-time della macchina virtuale non verranno copiate.<br/> |



 

</dd> <dt>

**CopyVmStorage**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indica se lo spazio di archiviazione della macchina virtuale verrà copiato quando viene esportata la macchina virtuale.



| Valore                                                                                | Significato                                                    |
|--------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**Vero**</dt> </dl>  | Verrà copiato lo spazio di archiviazione della macchina virtuale.<br/>     |
| <dl> <dt>**False**</dt> </dl> | L'archiviazione della macchina virtuale non verrà copiata.<br/> |



 

</dd> <dt>

**CreateVmExportSubdirectory**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indica se verrà creata una sottodirectory con il nome della macchina virtuale quando viene esportata la macchina virtuale.



| Valore                                                                                | Significato                                        |
|--------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**Vero**</dt> </dl>  | Verrà creata una sottodirectory.<br/>     |
| <dl> <dt>**False**</dt> </dl> | Non verrà creata una sottodirectory.<br/> |



 

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**DifferentialBackupBase**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Base per l'esportazione differenziale. Si tratta del percorso di un'istanza di [**\_ VirtualSystemReferencePoint MSVM**](msvm-virtualsystemreferencepoint.md) che rappresenta il punto di riferimento o il percorso di un'istanza di [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) che rappresenta lo snapshot da utilizzare come base per l'esportazione differenziale. Se la proprietà **CopySnapshotConfiguration** non è impostata su 3 (**ExportOneSnapshotForBackup**), questa proprietà viene ignorata.

> [!Note]  
> Aggiunta in Windows 10 e Windows Server 2016.

 

</dd> <dt>

**DisableDifferentialOfIgnoredStorage**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indica se i dischi differenze verranno creati o meno per l'archiviazione ignorata durante l'esportazione. Per impostazione predefinita, questo valore è impostato su false, il che significa che i dischi differenze vengono creati per l'archiviazione che non verrà copiata nella destinazione di esportazione.

> [!Note]  
> Aggiunta in Windows 10, versione 1709.

 

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per questa istanza. Inoltre, il nome visualizzato può essere utilizzato come proprietà di indice per una ricerca o una query. Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).

</dd> <dt>

**ExcludedVirtualHardDisks**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Matrice di ID di istanza [**MSVM \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) (RASD) che rappresentano i dischi rigidi virtuali che devono essere esclusi dall'operazione di esportazione. Se almeno uno degli ID specificati non è un disco rigido virtuale collegato valido, l'operazione avrà esito negativo.

I dischi rigidi virtuali a cui fa riferimento questa proprietà possono provenire dalla macchina virtuale e/o da uno qualsiasi dei relativi snapshot. L'esclusione di dischi rigidi virtuali non è supportata quando la proprietà **CopySnapshotConfiguration** è impostata su 0 (ExportAllSnapshots).

Si noti che l'ID dell'istanza di RASD per i dischi rigidi virtuali rappresenta il percorso a cui sono collegati ed escludendo questo ID esclude tutti i dischi rigidi virtuali collegati in tale posizione nell'albero degli snapshot della macchina virtuale, indipendentemente dal fatto che siano effettivamente una catena di dischi rigidi virtuali valida.

> [!Note]  
> Aggiunta in Windows 10, versione 1709.

 

</dd> <dt>

**ExportForLiveMigration**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indica se la macchina virtuale esportata deve essere utilizzata nella migrazione in tempo reale.

> [!Note]  
> Aggiunta in Windows 10, versione 1703 e Windows Server 2016.

 

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

All'interno dell'ambito dello spazio dei nomi di creazione di istanze, in modo opaco e univoco identifica un'istanza di questa classe. Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).

</dd> <dt>

**SnapshotVirtualSystem**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Percorso di un'istanza di [**\_ VirtualSystemSettingData MSVM**](msvm-virtualsystemsettingdata.md) che rappresenta lo snapshot da esportare con la macchina virtuale. Se la proprietà **CopySnapshotConfiguration** non è impostata su 2 (ExportOneSnapshot), questa proprietà viene ignorata.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe \_ VirtualSystemExportSettingData di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[Classi di gestione del sistema virtuale](virtual-system-management-classes.md)
</dt> <dt>

[**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 


---
description: Fornisce informazioni aggiuntive da usare con il metodo ExportSystemDefinition della classe Msvm \_ VirtualSystemManagementService.
ms.assetid: 86396A76-83EC-476E-86A9-83861A002152
title: Msvm_VirtualSystemExportSettingData classe
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
ms.openlocfilehash: 6760fb671e9e06ea603f86c944cf45a8637d1a811a8c8a0743946a88f25d5a06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117810496"
---
# <a name="msvm_virtualsystemexportsettingdata-class"></a>Classe Msvm \_ VirtualSystemExportSettingData

Fornisce informazioni aggiuntive da usare con il [**metodo ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) della [**classe Msvm \_ VirtualSystemManagementService.**](msvm-virtualsystemmanagementservice.md)

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

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

La **classe Msvm \_ VirtualSystemExportSettingData** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ VirtualSystemExportSettingData** ha queste proprietà.

<dl> <dt>

**BackupIntent**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Indica la finalità di utilizzo dei set di backup esportati.

> [!Note]  
> Questa proprietà è stata aggiunta in Windows 10 e Windows Server 2016.

 

<dt>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>**BackupIntentPreserveChain** (0)


</dt> <dd>

Tutti i set di backup completi e differenziali esportati verranno mantenuti così come sono.

</dd> <dt>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>**BackupIntentMerge** (1)


</dt> <dd>

I set di backup completi e differenziali esportati verranno uniti per sintetizzare i set di backup completi.

</dd> </dl>

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **MaxLen** (64)
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**CaptureLiveState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Indica lo stato da acquisire se la destinazione dell'esportazione è una macchina virtuale in esecuzione.

<dt>

<span id="CaptureCrashConsistentState"></span><span id="capturecrashconsistentstate"></span><span id="CAPTURECRASHCONSISTENTSTATE"></span>

<span id="CaptureCrashConsistentState"></span><span id="capturecrashconsistentstate"></span><span id="CAPTURECRASHCONSISTENTSTATE"></span>**CaptureCrashConsistentState** (0)


</dt> <dd>

Nessun file di stato salvato verrà esportato per la macchina virtuale in esecuzione, posizionandola in uno stato coerente con l'arresto anomalo del sistema.

</dd> <dt>

<span id="CaptureSavedState"></span><span id="capturesavedstate"></span><span id="CAPTURESAVEDSTATE"></span>

<span id="CaptureSavedState"></span><span id="capturesavedstate"></span><span id="CAPTURESAVEDSTATE"></span>**CaptureSavedState** (1)


</dt> <dd>

I file di stato salvati per la macchina virtuale in esecuzione verranno esportati insieme alla configurazione della macchina virtuale.

</dd> <dt>

<span id="CaptureAppConsistentState"></span><span id="captureappconsistentstate"></span><span id="CAPTUREAPPCONSISTENTSTATE"></span>

<span id="CaptureAppConsistentState"></span><span id="captureappconsistentstate"></span><span id="CAPTUREAPPCONSISTENTSTATE"></span>**CaptureAppConsistentState** (2)


</dt> <dd>

Verrà esportato lo stato coerente con l'applicazione della macchina virtuale in esecuzione.

> [!Note]  
> Aggiunta in Windows 10 e Windows Server 2016.

 

</dd> </dl>

</dd> <dt>

**CopySnapshotConfiguration**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Indica gli snapshot da esportare con la macchina virtuale.

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

Gli snapshot identificati dalla **proprietà SnapshotVirtualSystem** verranno esportati con la macchina virtuale. Le **proprietà CopyVmStorage** e **CopyVmRuntimeInformation** vengono ignorate, le informazioni sull'archiviazione e sulla fase di esecuzione vengono esportate con la macchina virtuale e tutti i dischi con differenze tra dischi rigidi virtuali verranno uniti in un nuovo disco rigido virtuale.

</dd> <dt>

<span id="ExportOneSnapshotForBackup"></span><span id="exportonesnapshotforbackup"></span><span id="EXPORTONESNAPSHOTFORBACKUP"></span>

<span id="ExportOneSnapshotForBackup"></span><span id="exportonesnapshotforbackup"></span><span id="EXPORTONESNAPSHOTFORBACKUP"></span>**ExportOneSnapshotForBackup** (3)


</dt> <dd>

Lo snapshot identificato dalla **proprietà SnapshotVirtualSystem** verrà esportato allo scopo di eseguire il backup della macchina virtuale. La configurazione esportata userà l'ID della macchina virtuale.

> [!Note]  
> Aggiunta in Windows 10 e Windows Server 2016.

 

</dd> </dl>

</dd> <dt>

**CopyVmRuntimeInformation**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Indica se le informazioni di run-time della macchina virtuale verranno copiate quando la macchina virtuale viene esportata.



| Valore                                                                                | Significato                                                                 |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**Vero**</dt> </dl>  | Verranno copiate le informazioni di run-time della macchina virtuale.<br/>     |
| <dl> <dt>**Falso**</dt> </dl> | Le informazioni di run-time della macchina virtuale non verranno copiate.<br/> |



 

</dd> <dt>

**CopyVmStorage**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Indica se l'archiviazione della macchina virtuale verrà copiata quando la macchina virtuale viene esportata.



| Valore                                                                                | Significato                                                    |
|--------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**Vero**</dt> </dl>  | L'archiviazione della macchina virtuale verrà copiata.<br/>     |
| <dl> <dt>**Falso**</dt> </dl> | L'archiviazione della macchina virtuale non verrà copiata.<br/> |



 

</dd> <dt>

**CreateVmExportSubdirectory**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Indica se verrà creata una sottodirectory con il nome della macchina virtuale quando la macchina virtuale viene esportata.



| Valore                                                                                | Significato                                        |
|--------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**Vero**</dt> </dl>  | Verrà creata una sottodirectory.<br/>     |
| <dl> <dt>**Falso**</dt> </dl> | Non verrà creata una sottodirectory.<br/> |



 

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**DifferenzialalBackupBase**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Base per l'esportazione differenziale. Percorso di un'istanza [**di Msvm \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) che rappresenta il punto di riferimento o il percorso di un'istanza [**di Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) che rappresenta lo snapshot da usare come base per l'esportazione differenziale. Se la **proprietà CopySnapshotConfiguration** non è impostata su 3(**ExportOneSnapshotForBackup**), questa proprietà viene ignorata.

> [!Note]  
> Aggiunta in Windows 10 e Windows Server 2016.

 

</dd> <dt>

**DisableDifferentialOfIgnoredStorage**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Indica se i dischi differenze verranno creati o meno per l'archiviazione ignorati durante l'esportazione. Per impostazione predefinita, questa opzione è impostata su false, il che significa che vengono creati dischi differenze per l'archiviazione che non verrà copiata nella destinazione di esportazione.

> [!Note]  
> Aggiunta in Windows 10, versione 1709.

 

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per questa istanza. Inoltre, il nome visualizzato può essere usato come proprietà di indice per una ricerca o una query. Questa proprietà viene ereditata da [**CIM \_ SettingData.**](/previous-versions//cc136911(v=vs.85))

</dd> <dt>

**ExcludedVirtualHardDisks**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Matrice di ID istanza [**RASD \_ (Msvm StorageAllocationSettingData)**](msvm-storageallocationsettingdata.md) che rappresentano i dischi rigidi virtuali che devono essere esclusi dall'operazione di esportazione. Se almeno uno degli ID forniti non è un disco rigido virtuale collegato valido, l'operazione avrà esito negativo.

I dischi rigidi virtuali a cui fa riferimento questa proprietà possono essere dalla macchina virtuale e/o da uno dei relativi snapshot. L'esclusione dei dischi rigidi virtuali non è supportata quando la **proprietà CopySnapshotConfiguration** è impostata su 0(ExportAllSnapshots).

Si noti che l'ID istanza RASD per i dischi rigidi virtuali rappresenta la posizione a cui sono collegati ed escludendo tramite questo ID tutti i dischi rigidi virtuali collegati in tale posizione nell'albero degli snapshot della macchina virtuale, indipendentemente dal fatto che siano effettivamente una catena di dischi rigidi virtuali valida.

> [!Note]  
> Aggiunta in Windows 10, versione 1709.

 

</dd> <dt>

**ExportForLiveMigration**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Indica se la macchina virtuale esportata deve essere usata nella migrazione in tempo reale.

> [!Note]  
> Aggiunta in Windows 10, versione 1703 e Windows Server 2016.

 

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Nell'ambito dello spazio dei nomi che crea un'istanza, identifica in modo opaco e univoco un'istanza di questa classe. Questa proprietà viene ereditata da [**CIM \_ SettingData.**](/previous-versions//cc136911(v=vs.85))

</dd> <dt>

**SnapshotVirtualSystem**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Percorso di [**un'istanza di Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) che rappresenta lo snapshot da esportare con la macchina virtuale. Se la **proprietà CopySnapshotConfiguration** non è impostata su 2 (ExportOneSnapshot), questa proprietà viene ignorata.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe Msvm \_ VirtualSystemExportSettingData** potrebbe essere limitato dal filtro del controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[Classi di gestione del sistema virtuale](virtual-system-management-classes.md)
</dt> <dt>

[**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 


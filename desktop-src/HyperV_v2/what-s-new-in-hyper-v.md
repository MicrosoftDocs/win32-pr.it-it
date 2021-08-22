---
description: La versione 2 del provider WMI Hyper-V è una novità per Windows 8 e Windows Server 2012.
ms.assetid: A91ACF7A-AFE6-45B6-960C-C4AAA0083735
title: Novità del provider WMI Hyper-V
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbaab65c08031c291eb11e8f865b77e256e5600deba060e0f8176ec8d13c3714
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754931"
---
# <a name="whats-new-in-hyper-v-wmi-provider"></a>Novità del provider WMI Hyper-V

La versione 2 del provider WMI Hyper-V è una novità per Windows 8 e Windows Server 2012.

## <a name="windows-10-version-1709"></a>Windows 10, versione 1709

Nuove classi:

-   [**Batteria \_ Msvm**](msvm-battery.md)
-   [**Msvm \_ BatterySettingData**](msvm-batterysettingdata.md)
-   [**Msvm \_ PersistentMemoryController**](msvm-persistentmemorycontroller.md)

Proprietà nuove:

-   [**Msvm \_ CollectionReferencePointExportJob:**](msvm-collectionreferencepointexportjob.md) **ExportedGuestStateFilePaths**
-   [**Msvm \_ EthernetSwitchHardwareOffloadData:**](msvm-ethernetswitchhardwareoffloaddata.md) **DefaultQueueVrssIndependentHostSpreading,** **DefaultQueueVrssExcludePrimaryProcessor,** **DefaultQueueVrssQueueSchedulingMode** e **DefaultQueueVrssMinQueuePairs**
-   [**Msvm \_ EthernetSwitchHardwareOffloadSettingData:**](msvm-ethernetswitchhardwareoffloadsettingdata.md) **DefaultQueueVrssIndependentHostSpreading**, **DefaultQueueVrssExcludePrimaryProcessor**, **DefaultQueueVrssQueueSchedulingMode**, **DefaultQueueVrssMinQueuePairs**, ,
-   [**Msvm \_ EthernetSwitchPortOffloadData:**](msvm-ethernetswitchportoffloaddata.md) **VrssVmbusChannelAffinityPolicy**, **VrssIndependentHostSpreading**, **VrssExcludePrimaryProcessor**, **VrssQueueSchedulingModes** e **VrssMinQueuePairs**
-   [**Msvm \_ VirtualHardDiskSettingData:**](msvm-virtualharddisksettingdata.md) **DataAlignment**, **PmemAddressAbstractionType** e **IsPmemCompatible**
-   [**Msvm \_ VirtualSystemExportSettingData:**](msvm-virtualsystemexportsettingdata.md) **DisableDifferentialOfIgnoredStorage** e **ExcludedVirtualHardDisks**
-   [**Msvm \_ VirtualSystemManagementServiceSettingData:**](msvm-virtualsystemmanagementservicesettingdata.md) **HypervisorRootSchedulerEnabled**
-   [**Msvm \_ VirtualSystemMigrationSettingData:**](msvm-virtualsystemmigrationsettingdata.md) **CPUCappingMagnitude** e **CancelIfBlackoutThresholdExceeded**
-   [**Msvm \_ VirtualSystemReferencePointExportJob:**](msvm-virtualsystemreferencepointexportjob.md) **ExportedGuestStateFilePath**
-   [**Msvm \_ VirtualSystemSettingData:**](msvm-virtualsystemsettingdata.md) **Architecture,** **AutomaticSnapshotsEnabled,** **IsAutomaticSnapshot,** **GuestStateFile** e **GuestStateDataRoot**

## <a name="windows-10-version-1703"></a>Windows 10 versione 1703

Nuove classi:

-   [**Msvm \_ AssignableDeviceDismountSettingData**](msvm-assignabledevicedismountsettingdata.md)
-   [**Msvm \_ AssignableDeviceService**](msvm-assignabledeviceservice.md)
-   [**Msvm \_ CollectionReferencePointExportJob**](msvm-collectionreferencepointexportjob.md)
-   [**Msvm \_ EthernetSwitchHardwareOffloadSettingData**](msvm-ethernetswitchhardwareoffloadsettingdata.md)
-   [**Msvm \_ EthernetSwitchPortMigrationQosSettingData**](msvm-ethernetswitchportmigrationqossettingdata.md)
-   [**Msvm \_ EthernetSwitchPortRdmaSettingData**](msvm-ethernetswitchportrdmasettingdata.md)
-   [**Msvm \_ EthernetSwitchPortTeamMappingSettingData**](msvm-ethernetswitchportteammappingsettingdata.md)
-   [**Msvm \_ GpuPartition**](msvm-gpupartition.md)
-   [**Msvm \_ GpuPartitionSettingData**](msvm-gpupartitionsettingdata.md)
-   [**Msvm \_ NetworkConnectionDiagnosticInformation**](msvm-networkconnectiondiagnosticinformation.md)
-   [**Msvm \_ NetworkConnectionDiagnosticSettingData**](msvm-networkconnectiondiagnosticsettingdata.md)
-   [**Msvm \_ PartitionableGpu**](msvm-partitionablegpu.md)
-   [**Msvm \_ PciExpress**](msvm-pciexpress.md)
-   [**Msvm \_ PciExpressSettingData**](msvm-pciexpresssettingdata.md)
-   [**Msvm \_ SecurityElement**](msvm-securityelement.md)
-   [**Msvm \_ SecurityService**](msvm-securityservice.md)
-   [**Msvm \_ SecuritySettingData**](msvm-securitysettingdata.md)
-   [**Msvm \_ StorageSettingData**](msvm-storagesettingdata.md)
-   [**Msvm \_ SummaryInformationBase**](msvm-summaryinformationbase.md)
-   [**Msvm \_ SystemComponentSettingData**](msvm-systemcomponentsettingdata.md)
-   [**Msvm \_ VirtualSystemReferencePointExportJob**](msvm-virtualsystemreferencepointexportjob.md)
-   [**Msvm \_ VirtualSystemReferencePointSettingData**](msvm-virtualsystemreferencepointsettingdata.md)

Classi rimosse:

-   [**Msvm \_ TPMSettingData**](msvm-tpmsettingdata.md)

Nuovi metodi:

-   [**Msvm \_ Classe CollectionSnapshotService:**](msvm-collectionsnapshotservice.md) [ **ApplySnapshot**](msvm-collectionsnapshotservice-applysnapshot.md)
-   [**Msvm \_ Classe VirtualSystemManagementService:**](msvm-virtualsystemmanagementservice.md) [**AddSystemComponentSetting,**](msvm-virtualsystemmanagementservice-addsystemcomponentsettings.md) [**DiagnoseNetworkConnection,**](msvm-virtualsystemmanagementservice-diagnosenetworkconnection.md) [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md)e [**RemoveSystemComponentSettings**](msvm-virtualsystemmanagementservice-removesystemcomponentsettings.md)
-   [**Msvm \_ Classe VirtualSystemReferencePointService:**](msvm-virtualsystemreferencepointservice.md) [ **ImportReferencePointMetadata**](msvm-virtualsystemreferencepointservice-importreferencepointmetadata.md)

Proprietà nuove:

-   [**Msvm \_ EthernetSwitchHardwareOffloadData:**](msvm-ethernetswitchhardwareoffloaddata.md) **DefaultQueueVmmqQueuePairs,** **DefaultQueueVmmqEnabled** e **DefaultQueueVrssEnabled**
-   [**Msvm \_ EthernetSwitchPortOffloadData:**](msvm-ethernetswitchportoffloaddata.md) **VmmqQueuePairs,** **VmmqEnabled** e **VrssEnabled**
-   [**Msvm \_ EthernetSwitchPortOffloadSettingData:**](msvm-ethernetswitchportoffloadsettingdata.md) **VmmqQueuePairs**, **VmmqEnabled** e **VrssEnabled**
-   [**Msvm \_ GuestClusterInformation:**](msvm-guestclusterinformation.md) **LastResourceMoveTime**
-   [**Msvm \_ KvpExchangeComponentSettingData:**](msvm-kvpexchangecomponentsettingdata.md) **DisableHostKVPItems**
-   [**Msvm \_ MemorySettingData:**](msvm-memorysettingdata.md) **SgxSize** e **SgxEnabled**
-   [**Msvm \_ Physical3dGraphicsProcessor:**](msvm-physical3dgraphicsprocessor.md) **CompatibleForVirtualization** e **DriverModelVersion**
-   [**Msvm \_ ProcessorSettingData:**](msvm-processorsettingdata.md) **HwThreadsPerCoreCpuGroupId,** **HideHypervisorPresent** ed **ExposeVirtualizationExtensions**
-   [**Msvm \_ SettingsDefineCapabilities:**](msvm-settingsdefinecapabilities.md) **SupportStatement**
-   [**Msvm \_ StorageAllocationSettingData:**](msvm-storageallocationsettingdata.md) **WriteHardeningMethod**
-   [**Msvm \_ SummaryInformation:**](msvm-summaryinformation.md) **schermata**
-   [**Msvm \_ SyntheticEthernetPortSettingData:**](msvm-syntheticethernetportsettingdata.md) **AllowPacketDirect**
-   [**Msvm \_ VirtualSystemCollection:**](msvm-virtualsystemcollection.md) **LastApplyConsistencyLevel,** **LastApplyVirtualMachineIds,** **LastApplyTime,** **FailedOverReplicationType,** **ReplicationMode** e **ReplicationState**
-   [**Msvm \_ VirtualSystemExportSettingData:**](msvm-virtualsystemexportsettingdata.md) **ExportForLiveMigration**
-   [**Msvm \_ VirtualSystemMigrationSettingData:**](msvm-virtualsystemmigrationsettingdata.md) **AvoidRemovingVHDs** e **AllowOverwriteExistingFile**
-   [**Msvm \_ VirtualSystemSettingData:**](msvm-virtualsystemsettingdata.md) **HighMmioGapSize**
-   [**Msvm \_ VirtualSystemSnapshotSettingData:**](msvm-virtualsystemsnapshotsettingdata.md) **GuestBackupType**

Proprietà rimosse:

-   [**Msvm \_ VirtualSystemSettingData:**](msvm-virtualsystemsettingdata.md) **ParentPackage**

## <a name="windows-10"></a>Windows 10

Nuove classi:

-   [**CIM \_ CollectedMSEs**](cim-collectedmses.md)
-   [**Raccolta \_ CIM**](cim-collection.md)
-   [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md)
-   [**CIM \_ ElementView**](cim-elementview.md)
-   [**CIM \_ MemberOfCollection**](cim-memberofcollection.md)
-   [**CIM \_ TPM**](cim-tpm.md)
-   [**Visualizzazione \_ CIM**](cim-view.md)
-   [**Msvm \_ CollectedCollections**](msvm-collectedcollections.md)
-   [**Msvm \_ CollectedReferencePoints**](msvm-collectedreferencepoints.md)
-   [**Msvm \_ CollectedSnapshots**](msvm-collectedsnapshots.md)
-   [**Msvm \_ CollectedVirtualSystems**](msvm-collectedvirtualsystems.md)
-   [**Msvm \_ CollectionManagementService**](msvm-collectionmanagementservice.md)
-   [**Msvm \_ CollectionReferencePointExportSettingData**](msvm-collectionreferencepointexportsettingdata.md)
-   [**Msvm \_ CollectionReferencePointService**](msvm-collectionreferencepointservice.md)
-   [**Msvm \_ CollectionReferencePointSettingData**](msvm-collectionreferencepointsettingdata.md)
-   [**Msvm \_ CollectionSettingData**](msvm-collectionsettingdata.md)
-   [**Msvm \_ CollectionSnapshotExportSettingData**](msvm-collectionsnapshotexportsettingdata.md)
-   [**Msvm \_ CollectionSnapshotService**](msvm-collectionsnapshotservice.md)
-   [**Msvm \_ ComputerSystemSummaryInformation**](msvm-computersystemsummaryinformation.md)
-   [**Msvm \_ EthernetSwitchPortVfpSettingData**](msvm-ethernetswitchportvfpsettingdata.md)
-   [**Msvm \_ GuestClusterInformation**](msvm-guestclusterinformation.md)
-   [**Msvm \_ GuestCommunicationService**](msvm-guestcommunicationservice.md)
-   [**Msvm \_ GuestCommunicationServiceSettingData**](msvm-guestcommunicationservicesettingdata.md)
-   [**Msvm \_ GuestServiceInterfaceSettingDataComponent**](msvm-guestserviceinterfacesettingdatacomponent.md)
-   [**Msvm \_ ManagementCollection**](msvm-managementcollection.md)
-   [**Msvm \_ MoveUnmanagedVhd**](msvm-moveunmanagedvhd.md)
-   [**Raccolta \_ ReferencePointCollection di Msvm**](msvm-referencepointcollection.md)
-   [**Msvm \_ ReferencePointOfVirtualSystem**](msvm-referencepointofvirtualsystem.md)
-   [**Msvm \_ ReferencePointOfVirtualSystemCollection**](msvm-referencepointofvirtualsystemcollection.md)
-   [**Msvm \_ ResourceDependentOnResource**](msvm-resourcedependentonresource.md)
-   [**Msvm \_ SerialPortSettingData**](msvm-serialportsettingdata.md)
-   [**Msvm \_ ServiceOfVssComponent**](msvm-serviceofvsscomponent.md)
-   [**Msvm \_ SnapshotCollection**](msvm-snapshotcollection.md)
-   [**Msvm \_ SnapshotOfVirtualSystemCollection**](msvm-snapshotofvirtualsystemcollection.md)
-   [**Msvm \_ StandaloneV2ElementConformsToProfile**](msvm-standalonev2elementconformstoprofile.md)
-   [**Msvm \_ SyntheticDisplayControllerSettingData**](msvm-syntheticdisplaycontrollersettingdata.md)
-   [**Msvm \_ SyntheticKeyboard**](msvm-synthetickeyboard.md)
-   [**Msvm \_ TPM**](msvm-tpm.md)
-   [**Msvm \_ TPMSettingData**](msvm-tpmsettingdata.md)
-   [**Msvm \_ VHDSetInformation**](msvm-vhdsetinformation.md)
-   [**Msvm \_ VHDSnapshotInformation**](msvm-vhdsnapshotinformation.md)
-   [**Msvm \_ VirtualEthernetSwitchNicTeamingMember**](msvm-virtualethernetswitchnicteamingmember.md)
-   [**Msvm \_ VirtualEthernetSwitchNicTeamingSettingData**](msvm-virtualethernetswitchnicteamingsettingdata.md)
-   [**Msvm \_ VirtualMachineToDisks**](msvm-virtualmachinetodisks.md)
-   [**Msvm \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md)
-   [**Msvm \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md)
-   [**Msvm \_ VirtualSystemReferencePointExportSettingData**](msvm-virtualsystemreferencepointexportsettingdata.md)
-   [**Msvm \_ VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md)
-   [**Msvm \_ VirtualSystemReferencePointSettingData**](msvm-virtualsystemreferencepointsettingdata.md)
-   [**Msvm \_ VirtualSystemSnapshotSettingData**](msvm-virtualsystemsnapshotsettingdata.md)
-   [**Msvm \_ VssService**](msvm-vssservice.md)

Classe rimossa:

-   [**Msvm \_ ResourcePoolComponent**](msvm-resourcepoolcomponent.md)
-   [**Msvm \_ ResourcePoolRegistration**](msvm-resourcepoolregistration.md)
-   [**Msvm \_ ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md)
-   [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)
-   [**Msvm \_ VirtualizationComponentRegistration**](msvm-virtualizationcomponentregistration.md)

Proprietà nuove:

-   [**Msvm \_ BootSourceSettingData:**](msvm-bootsourcesettingdata.md) **OptionalData**
-   [**Msvm \_ EthernetPortAllocationSettingData:**](msvm-ethernetportallocationsettingdata.md) **LastKnownSwitchName** e **CompartmentGuid**
-   [**Msvm \_ EthernetSwitchHardwareOffloadData:**](msvm-ethernetswitchhardwareoffloaddata.md) **PacketDirectInUse**
-   [**Msvm \_ EthernetSwitchPortOffloadSettingData:**](msvm-ethernetswitchportoffloadsettingdata.md) **PacketDirectModerationInterval,** **PacketDirectModerationCount,** **PacketDirectNumProcs**,
-   [**Msvm \_ EthernetSwitchPortSecuritySettingData:**](msvm-ethernetswitchportsecuritysettingdata.md) **EnableFixSpeed10G** e **Riservato**
-   [**Msvm \_ GuestServiceInterfaceComponentSettingData:**](msvm-guestserviceinterfacecomponentsettingdata.md) **DefaultEnabledStatePolicy**
-   [**Msvm \_ ProcessorSettingData:**](msvm-processorsettingdata.md) **EnableHostResourceProtection**
-   [**Msvm \_ StorageAllocationSettingData:**](msvm-storageallocationsettingdata.md) **StorageQoSPolicyID,** **CachingMode** e **SnapshotId**
-   [**Msvm \_ SummaryInformation:**](msvm-summaryinformation.md) **InstanceID,** **Version,** **ThumbnailImageHeight,** **ThumbnailImageWidth** e **HostComputerSystemName**
-   [**Msvm \_ Synthetic3DDisplayControllerSettingData:**](msvm-synthetic3ddisplaycontrollersettingdata.md) **VRAMSizeBytes**
-   [**Msvm \_ VirtualEthernetSwitchSettingData:**](msvm-virtualethernetswitchsettingdata.md) **TeamingEnabled** e **PacketDirectEnabled**
-   [**Msvm \_ VirtualHardDiskSettingData:**](msvm-virtualharddisksettingdata.md) **ParentTimestamp** e **ParentIdentifier**
-   [**Msvm \_ VirtualHardDiskState:**](msvm-virtualharddiskstate.md) **timestamp**
-   [**Msvm \_ VirtualSystemExportSettingData:**](msvm-virtualsystemexportsettingdata.md) **BackupIntent** e **DifferentialBackupBase**
-   [**Msvm \_ VirtualSystemManagementServiceSettingData:**](msvm-virtualsystemmanagementservicesettingdata.md) **DefaultVirtualHardDiskCachingMode**
-   [**Msvm \_ VirtualSystemMigrationSettingData:**](msvm-virtualsystemmigrationsettingdata.md) **RemoveSourceUnmanagedVhds** e **UnmanagedVhds**
-   [**Msvm \_ VirtualSystemSettingData:**](msvm-virtualsystemsettingdata.md) **UserSnapshotType,** **GuestControlledCacheTypes,** **LockOnDisconnect,** **ParentPackage,** **AutomaticCriticalErrorActionTimeout,** **AutomaticCriticalErrorAction,** **ConsoleMode** e **SecureBootTemplateId**

Nuovi metodi:

-   [**Msvm \_ Classe ImageManagementService:**](msvm-imagemanagementservice.md) [**ConvertVirtualHardDiskToVHDSet,**](msvm-imagemanagementservice-convertvirtualharddisktovhdset.md) [**DeleteVHDSnapshot,**](msvm-imagemanagementservice-deletevhdsnapshot.md) [**FindMountedStorageImageInstance,**](msvm-imagemanagementservice-findmountedstorageimageinstance.md) [**GetVHDSetInformation,**](msvm-imagemanagementservice-getvhdsetinformation.md) [**GetVHDSnapshotInformation,**](msvm-imagemanagementservice-getvhdsnapshotinformation.md) [**GetVirtualDiskChanges,**](msvm-imagemanagementservice-getvirtualdiskchanges.md) [**OptimizeVHDSet**](msvm-imagemanagementservice-optimizevhdset.md)e [**SetVHDSnapshotInformation**](msvm-imagemanagementservice-setvhdsnapshotinformation.md)
-   [**Msvm \_ Classe ShutdownComponent:**](msvm-shutdowncomponent.md) [ **InitiateReboot**](msvm-shutdowncomponent-initiatereboot.md)
-   [**Msvm \_ VirtualSystemManagementService:**](msvm-virtualsystemmanagementservice.md) [**AddBootSourceSettings,**](msvm-virtualsystemmanagementservice-addbootsourcesettings.md) [**AddGuestServiceSettings,**](msvm-virtualsystemmanagementservice-addguestservicesettings.md) [**DefinePlannedSystem,**](msvm-virtualsystemmanagementservice-defineplannedsystem.md) [**ModifyGuestServiceSettings,**](msvm-virtualsystemmanagementservice-modifyguestservicesettings.md) [**RemoveBootSourceSettings,**](msvm-virtualsystemmanagementservice-removebootsourcesettings.md) [**RemoveGuesServiceSettings,**](msvm-virtualsystemmanagementservice-removeguestservicesettings.md) [**SetInitialMachineConfigurationData**](msvm-virtualsystemmanagementservice-setinitialmachineconfigurationdata.md)e [**UpgradeSystemVersion**](msvm-virtualsystemmanagementservice-upgradesystemversion.md)
-   [**Msvm \_ Classe VirtualSystemSnapshotService:**](msvm-virtualsystemsnapshotservice.md) [ **ConvertToReferencePoint**](msvm-virtualsystemsnapshotservice-converttoreferencepoint.md)

## <a name="windows-81-and-windows-server-2012-r2"></a>Windows 8.1 e Windows Server 2012 R2

Windows 8.1 e Windows Server 2012 R2 includono nuove funzionalità per la versione 2 del provider WMI Hyper-V.

-   Le **proprietà IOPSAllocationUnits,** **IOPSLimit,** **IOPSReservation** e **PersistentReservationsSupported** sono state aggiunte alla [**classe Msvm \_ StorageAllocationSettingData.**](msvm-storageallocationsettingdata.md)
-   La **proprietà VirtualDiskId** è stata aggiunta alla [**classe Msvm \_ VirtualHardDiskSettingData.**](msvm-virtualharddisksettingdata.md)
-   Sono state aggiunte informazioni sulla QoS di archiviazione alla proprietà **OperationalStatus** delle [**classi \_ Msvm LogicalDisk**](msvm-logicaldisk.md) [**e Msvm \_ ResourcePool.**](msvm-resourcepool.md)
-   [**Msvm \_ Classe StorageAlert**](msvm-storagealert.md)
-   La **proprietà ClusterMonitored** è stata aggiunta alle [**classi Msvm \_ EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) e [**Msvm \_ SyntheticEthernetPortSettingData.**](msvm-syntheticethernetportsettingdata.md)
-   Le **proprietà EnableCompression** e **EnableSmbTransport** sono state aggiunte alla [**classe Msvm \_ VirtualSystemMigrationServiceSettingData.**](msvm-virtualsystemmigrationservicesettingdata.md)
-   La **proprietà EnableCompression** è stata aggiunta alla [**classe Msvm \_ VirtualSystemMigrationSettingData.**](msvm-virtualsystemmigrationsettingdata.md) La **proprietà TransportType** include informazioni sulla migrazione in tempo reale.
-   [**Msvm \_ Classe CopyFileToGuestJob**](msvm-copyfiletoguestjob.md)
-   [**Msvm \_ Classe CopyFileToGuestSettingData**](msvm-copyfiletoguestsettingdata.md)
-   [**Msvm \_ Classe GuestFileService**](msvm-guestfileservice.md)
-   [**Msvm \_ Classe GuestService**](msvm-guestservice.md)
-   [**Msvm \_ Classe GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md)
-   [**Msvm \_ Classe GuestServiceInterfaceComponentSettingData**](msvm-guestserviceinterfacecomponentsettingdata.md)
-   [**Msvm \_ Classe RegisteredGuestService**](msvm-registeredguestservice.md)
-   La **proprietà EnhancedSessionModeEnabled** è stata aggiunta alla [**classe Msvm \_ VirtualSystemManagementServiceSettingData.**](msvm-virtualsystemmanagementservicesettingdata.md)
-   La **proprietà EnhancedModeState** e il [**metodo InjectNonMaskableInterrupt**](injectnonmaskableinterrupt-msvm-computersystem.md) sono stati aggiunti alla [**classe Msvm \_ ComputerSystem.**](msvm-computersystem.md)
-   Le proprietà **BootSourceOrder,** **LowMmioGapSize,** **NetworkBootPreferredProtocol,** **PauseAfterBootFailure,** **SecureBootEnabled** e **VirtualSystemSubType** sono state aggiunte alla [**classe Msvm \_ VirtualSystemSettingData.**](msvm-virtualsystemsettingdata.md)
-   [**Msvm \_ Classe BootSourceSettingData**](msvm-bootsourcesettingdata.md)
-   [**Msvm \_ Classe BootSourceComponent**](msvm-bootsourcecomponent.md)
-   [**Msvm \_ Classe LogicalIdentity**](msvm-logicalidentity.md)
-   [**Msvm \_ Classe CompatibilityVector**](msvm-compatibilityvector.md)
-   Il [**metodo GetSystemCompatibilityVectors**](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md) è stato aggiunto alla [**classe Msvm \_ VirtualSystemMigrationService.**](msvm-virtualsystemmigrationservice.md)
-   Le **proprietà ReplicationStateEx,** **ReplicationHealthEx,** **EnhancedSessionModeState,** **VirtualSwitchNames** e **VirtualSystemSubType** sono state aggiunte alla [**classe Msvm \_ SummaryInformation.**](msvm-summaryinformation.md) Le **proprietà ReplicationState** e **ReplicationHealth** sono deprecate e sostituite dalle **proprietà ReplicationStateEx** e **ReplicationHealthEx.**
-   La **proprietà PnpDevicePath** è stata aggiunta alla [**classe Msvm \_ MountedStorageImage.**](msvm-mountedstorageimage.md)
-   Le **proprietà AllowedHashAlgorithms** e **TrustedIssuerCertificateHashes** sono state aggiunte alla [**classe Msvm \_ TerminalServiceSettingData.**](msvm-terminalservicesettingdata.md)

Windows 8.1 e Windows Server 2012 R2 includono nuove funzionalità per la replica delle macchine virtuali e il ripristino del failover.

-   [**Msvm \_ Classe ReplicationProvider**](msvm-replicationprovider.md)
-   [**Msvm \_ Classe ReplicationRelationship**](msvm-replicationrelationship.md)
-   I [**metodi ChangeReplicationModeToPrimary,**](changereplicationmodetoprimary-msvm-replicationservice.md) [**GetReplicationStatisticsEx,**](getreplicationstatisticsex-msvm-replicationservice.md) [**InitiateFailback,**](initiatefailback-msvm-replicationservice.md) [**RemoveReplicationRelationshipEx**](removereplicationrelationshipex-msvm-replicationservice.md)e [**ResetReplicationStatisticsEx**](resetreplicationstatisticsex-msvm-replicationservice.md) sono stati aggiunti alla [**classe Msvm \_ ReplicationService.**](msvm-replicationservice.md) I metodi **GetReplicationStatisticsEx**, **RemoveReplicationRelationshipEx** e **ResetReplicationStatisticsEx** sostituiscono i metodi [**GetReplicationStatistics**](getreplicationstatistics-msvm-replicationservice.md), [**RemoveReplicationRelationship**](removereplicationrelationship-msvm-replicationservice.md)e [**ResetReplicationStatistics.**](resetreplicationstatistics-msvm-replicationservice.md)
-   La [**classe Msvm \_ SystemReplicationRelationship**](msvm-systemreplicationrelationship.md) mostra un'associazione tra una macchina virtuale e molte relazioni di replica.
-   Le **proprietà AdditionalSettings** **e ReplicationProvider** sono state aggiunte alla [**classe Msvm \_ ReplicationSettingData.**](msvm-replicationsettingdata.md)
-   Sono state aggiunte informazioni sul provider da host a host ai metodi [**CreateReplicationRelationship**](createreplicationrelationship-msvm-replicationservice.md) e [**ModifyReplicationSettings**](modifyreplicationsettings-msvm-replicationservice.md) della [**classe Msvm \_ ReplicationService.**](msvm-replicationservice.md)
-   Il [**metodo RequestReplicationStateChangeEx**](msvm-requestreplicationstatechangeex-computersystem.md) è stato aggiunto alla [**classe Msvm \_ ComputerSystem**](msvm-computersystem.md) e sostituisce il [**metodo RequestReplicationStateChange.**](msvm-computersystem-requestreplicationstatechange.md) La **proprietà InstanceID** può ora indicare la replica estesa. Per altre informazioni sulla replica estesa, vedere [**Msvm \_ ReplicationRelationship.**](msvm-replicationrelationship.md)
-   [**Msvm \_ Le istanze ReplicationSettingData**](msvm-replicationsettingdata.md) [**e Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) hanno una relazione 1:1 che è possibile rappresentare con un'associazione [**Msvm \_ SettingsDefineState.**](msvm-settingsdefinestate.md)

    | [**Msvm \_ ImpostazioniNomi della proprietà SettingsDefineState**](msvm-settingsdefinestate.md) | Valore                                                                                                |
    |-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
    | **ManagedElement**                                                          | Rappresenta [**l'oggetto Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md)          |
    | **Impostazione dei dati**                                                             | Rappresenta [**l'oggetto Msvm \_ ReplicationSettingData**](msvm-replicationsettingdata.md) associato |

    

     

-   [**Msvm \_ ReplicationSettingData può**](msvm-replicationsettingdata.md) distinguere tra l'impostazione di istanze per la relazione di replica in base alla **proprietà InstanceId** o **ReplicationRelationship.** Di conseguenza, questi metodi che si occupano di una singola relazione non modificano la firma:

    -   [**Msvm \_ ReplicationService::CreateReplicationRelationship**](createreplicationrelationship-msvm-replicationservice.md)
    -   [**Msvm \_ ReplicationService::ModifyReplicationSettings**](modifyreplicationsettings-msvm-replicationservice.md)
    -   [**Msvm \_ ReplicationService::Resync**](resynchronize-msvm-replicationservice.md)
    -   [**Msvm \_ ReplicationService::StartReplication**](startreplication-msvm-replicationservice.md)

-   Sebbene sia possibile usare [**sempre GetReplicationStatistics**](getreplicationstatistics-msvm-replicationservice.md), [**RemoveReplicationRelationship**](removereplicationrelationship-msvm-replicationservice.md)e [**RequestReplicationStateChange**](msvm-computersystem-requestreplicationstatechange.md) per la relazione primaria, è consigliabile usare invece [**GetReplicationStatisticsEx**](getreplicationstatisticsex-msvm-replicationservice.md), [**RemoveReplicationRelationshipEx**](removereplicationrelationshipex-msvm-replicationservice.md)e [**RequestReplicationStateChangeEx**](msvm-requestreplicationstatechangeex-computersystem.md) perché possono elaborare la relazione di replica primaria ed estesa. Per altre informazioni sulla replica estesa, vedere [**Msvm \_ ReplicationRelationship.**](msvm-replicationrelationship.md)
-   Sebbene queste proprietà della classe [**Msvm \_ ComputerSystem**](msvm-computersystem.md) continuino a indicare lo stato della relazione di replica primaria, usare invece queste proprietà di un oggetto [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) per determinare lo stato corrente per la relazione di replica primaria ed estesa.

    | Nome proprietà                                | Type        |
    |----------------------------------------------|-------------|
    | **Stato replica**                         | Uint16 (RO) |
    | **Replicationhealth**                        | Uint16 (RO) |
    | **LastReplicationTime**                      | Datetime    |
    | **FailedOverReplicationType**                | Uint16      |
    | **LastApplicationConsistentReplicationTime** | Datetime    |
    | **LastReplicationType**                      | Uint16      |

    

     

 

 




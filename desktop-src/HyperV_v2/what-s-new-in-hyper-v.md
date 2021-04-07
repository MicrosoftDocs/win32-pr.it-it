---
description: La versione 2 del provider WMI Hyper-V è una novità per Windows 8 e Windows Server 2012.
ms.assetid: A91ACF7A-AFE6-45B6-960C-C4AAA0083735
title: Novità del provider WMI Hyper-V
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce222fd18955e88b9e33e1b706cf81ef5a806917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883025"
---
# <a name="whats-new-in-hyper-v-wmi-provider"></a>Novità del provider WMI Hyper-V

La versione 2 del provider WMI Hyper-V è una novità per Windows 8 e Windows Server 2012.

## <a name="windows-10-version-1709"></a>Windows 10, versione 1709

Nuove classi:

-   [**\_Batteria MSVM**](msvm-battery.md)
-   [**\_BatterySettingData MSVM**](msvm-batterysettingdata.md)
-   [**\_PersistentMemoryController MSVM**](msvm-persistentmemorycontroller.md)

Proprietà nuove:

-   [**MSVM \_ CollectionReferencePointExportJob**](msvm-collectionreferencepointexportjob.md): **ExportedGuestStateFilePaths**
-   [**MSVM \_ EthernetSwitchHardwareOffloadData**](msvm-ethernetswitchhardwareoffloaddata.md): **DefaultQueueVrssIndependentHostSpreading**, **DefaultQueueVrssExcludePrimaryProcessor**, **DefaultQueueVrssQueueSchedulingMode** e **DefaultQueueVrssMinQueuePairs**
-   [**MSVM \_ EthernetSwitchHardwareOffloadSettingData**](msvm-ethernetswitchhardwareoffloadsettingdata.md): **DefaultQueueVrssIndependentHostSpreading**, **DefaultQueueVrssExcludePrimaryProcessor**, **DefaultQueueVrssQueueSchedulingMode**, **DefaultQueueVrssMinQueuePairs**,
-   [**MSVM \_ EthernetSwitchPortOffloadData**](msvm-ethernetswitchportoffloaddata.md): **VrssVmbusChannelAffinityPolicy**, **VrssIndependentHostSpreading**, **VrssExcludePrimaryProcessor**, **VrssQueueSchedulingModes** e **VrssMinQueuePairs**
-   [**MSVM \_ VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md): **dataalignment**, **PmemAddressAbstractionType** e **IsPmemCompatible**
-   [**MSVM \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md): **DisableDifferentialOfIgnoredStorage** e **ExcludedVirtualHardDisks**
-   [**MSVM \_ VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md): **HypervisorRootSchedulerEnabled**
-   [**MSVM \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md): **CPUCappingMagnitude** e **CancelIfBlackoutThresholdExceeded**
-   [**MSVM \_ VirtualSystemReferencePointExportJob**](msvm-virtualsystemreferencepointexportjob.md): **ExportedGuestStateFilePath**
-   [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md): **Architecture**, **AutomaticSnapshotsEnabled**, **IsAutomaticSnapshot**, **GuestStateFile** e **GuestStateDataRoot**

## <a name="windows-10-version-1703"></a>Windows 10 versione 1703

Nuove classi:

-   [**\_AssignableDeviceDismountSettingData MSVM**](msvm-assignabledevicedismountsettingdata.md)
-   [**\_AssignableDeviceService MSVM**](msvm-assignabledeviceservice.md)
-   [**\_CollectionReferencePointExportJob MSVM**](msvm-collectionreferencepointexportjob.md)
-   [**\_EthernetSwitchHardwareOffloadSettingData MSVM**](msvm-ethernetswitchhardwareoffloadsettingdata.md)
-   [**\_EthernetSwitchPortMigrationQosSettingData MSVM**](msvm-ethernetswitchportmigrationqossettingdata.md)
-   [**\_EthernetSwitchPortRdmaSettingData MSVM**](msvm-ethernetswitchportrdmasettingdata.md)
-   [**\_EthernetSwitchPortTeamMappingSettingData MSVM**](msvm-ethernetswitchportteammappingsettingdata.md)
-   [**\_GpuPartition MSVM**](msvm-gpupartition.md)
-   [**\_GpuPartitionSettingData MSVM**](msvm-gpupartitionsettingdata.md)
-   [**\_NetworkConnectionDiagnosticInformation MSVM**](msvm-networkconnectiondiagnosticinformation.md)
-   [**\_NetworkConnectionDiagnosticSettingData MSVM**](msvm-networkconnectiondiagnosticsettingdata.md)
-   [**\_PartitionableGpu MSVM**](msvm-partitionablegpu.md)
-   [**\_Per MSVM**](msvm-pciexpress.md)
-   [**\_PciExpressSettingData MSVM**](msvm-pciexpresssettingdata.md)
-   [**MSVM \_ SecurityElement**](msvm-securityelement.md)
-   [**\_SecurityService MSVM**](msvm-securityservice.md)
-   [**\_SecuritySettingData MSVM**](msvm-securitysettingdata.md)
-   [**\_StorageSettingData MSVM**](msvm-storagesettingdata.md)
-   [**\_SummaryInformationBase MSVM**](msvm-summaryinformationbase.md)
-   [**\_SystemComponentSettingData MSVM**](msvm-systemcomponentsettingdata.md)
-   [**\_VirtualSystemReferencePointExportJob MSVM**](msvm-virtualsystemreferencepointexportjob.md)
-   [**\_VirtualSystemReferencePointSettingData MSVM**](msvm-virtualsystemreferencepointsettingdata.md)

Classi rimosse:

-   [**\_TPMSettingData MSVM**](msvm-tpmsettingdata.md)

Nuovi metodi:

-   [**MSVM \_ Classe CollectionSnapshotService**](msvm-collectionsnapshotservice.md) : [ **ApplySnapshot**](msvm-collectionsnapshotservice-applysnapshot.md)
-   [**MSVM \_ Classe VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) : [**AddSystemComponentSetting**](msvm-virtualsystemmanagementservice-addsystemcomponentsettings.md), [**DiagnoseNetworkConnection**](msvm-virtualsystemmanagementservice-diagnosenetworkconnection.md), [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md)e [**RemoveSystemComponentSettings**](msvm-virtualsystemmanagementservice-removesystemcomponentsettings.md)
-   [**MSVM \_ Classe VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md) : [ **ImportReferencePointMetadata**](msvm-virtualsystemreferencepointservice-importreferencepointmetadata.md)

Proprietà nuove:

-   [**MSVM \_ EthernetSwitchHardwareOffloadData**](msvm-ethernetswitchhardwareoffloaddata.md): **DefaultQueueVmmqQueuePairs**, **DefaultQueueVmmqEnabled** e **DefaultQueueVrssEnabled**
-   [**MSVM \_ EthernetSwitchPortOffloadData**](msvm-ethernetswitchportoffloaddata.md): **VmmqQueuePairs**, **VmmqEnabled** e **VrssEnabled**
-   [**MSVM \_ EthernetSwitchPortOffloadSettingData**](msvm-ethernetswitchportoffloadsettingdata.md): **VmmqQueuePairs**, **VmmqEnabled** e **VrssEnabled**
-   [**MSVM \_ GuestClusterInformation**](msvm-guestclusterinformation.md): **LastResourceMoveTime**
-   [**MSVM \_ KvpExchangeComponentSettingData**](msvm-kvpexchangecomponentsettingdata.md): **DisableHostKVPItems**
-   [**MSVM \_ MemorySettingData**](msvm-memorysettingdata.md): **SgxSize** e **SgxEnabled**
-   [**MSVM \_ Physical3dGraphicsProcessor**](msvm-physical3dgraphicsprocessor.md): **CompatibleForVirtualization** e **DriverModelVersion**
-   [**MSVM \_ ProcessorSettingData**](msvm-processorsettingdata.md): **HwThreadsPerCoreCpuGroupId**, **HideHypervisorPresent** e **ExposeVirtualizationExtensions**
-   [**MSVM \_ SettingsDefineCapabilities**](msvm-settingsdefinecapabilities.md): **SupportStatement**
-   [**MSVM \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md): **WriteHardeningMethod**
-   [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md): **schermate**
-   [**MSVM \_ SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md): **AllowPacketDirect**
-   [**MSVM \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md): **LastApplyConsistencyLevel**, **LastApplyVirtualMachineIds**, **LastApplyTime**, **FailedOverReplicationType**, **ReplicationMode** e **ReplicationState**
-   [**MSVM \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md): **ExportForLiveMigration**
-   [**MSVM \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md): **AvoidRemovingVHDs** e **AllowOverwriteExistingFile**
-   [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md): **HighMmioGapSize**
-   [**MSVM \_ VirtualSystemSnapshotSettingData**](msvm-virtualsystemsnapshotsettingdata.md): **GuestBackupType**

Proprietà rimosse:

-   [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md): **ParentPackage**

## <a name="windows-10"></a>Windows 10

Nuove classi:

-   [**\_COLLECTEDMSES CIM**](cim-collectedmses.md)
-   [**\_Raccolta CIM**](cim-collection.md)
-   [**\_COLLECTIONOFMSES CIM**](cim-collectionofmses.md)
-   [**\_ELEMENTVIEW CIM**](cim-elementview.md)
-   [**\_MEMBEROFCOLLECTION CIM**](cim-memberofcollection.md)
-   [**\_TPM CIM**](cim-tpm.md)
-   [**\_Visualizzazione CIM**](cim-view.md)
-   [**\_CollectedCollections MSVM**](msvm-collectedcollections.md)
-   [**\_CollectedReferencePoints MSVM**](msvm-collectedreferencepoints.md)
-   [**\_CollectedSnapshots MSVM**](msvm-collectedsnapshots.md)
-   [**\_CollectedVirtualSystems MSVM**](msvm-collectedvirtualsystems.md)
-   [**\_CollectionManagementService MSVM**](msvm-collectionmanagementservice.md)
-   [**\_CollectionReferencePointExportSettingData MSVM**](msvm-collectionreferencepointexportsettingdata.md)
-   [**\_CollectionReferencePointService MSVM**](msvm-collectionreferencepointservice.md)
-   [**\_CollectionReferencePointSettingData MSVM**](msvm-collectionreferencepointsettingdata.md)
-   [**\_CollectionSettingData MSVM**](msvm-collectionsettingdata.md)
-   [**\_CollectionSnapshotExportSettingData MSVM**](msvm-collectionsnapshotexportsettingdata.md)
-   [**\_CollectionSnapshotService MSVM**](msvm-collectionsnapshotservice.md)
-   [**\_ComputerSystemSummaryInformation MSVM**](msvm-computersystemsummaryinformation.md)
-   [**\_EthernetSwitchPortVfpSettingData MSVM**](msvm-ethernetswitchportvfpsettingdata.md)
-   [**\_GuestClusterInformation MSVM**](msvm-guestclusterinformation.md)
-   [**\_GuestCommunicationService MSVM**](msvm-guestcommunicationservice.md)
-   [**\_GuestCommunicationServiceSettingData MSVM**](msvm-guestcommunicationservicesettingdata.md)
-   [**\_GuestServiceInterfaceSettingDataComponent MSVM**](msvm-guestserviceinterfacesettingdatacomponent.md)
-   [**MSVM \_ managementcollection**](msvm-managementcollection.md)
-   [**\_MoveUnmanagedVhd MSVM**](msvm-moveunmanagedvhd.md)
-   [**\_ReferencePointCollection MSVM**](msvm-referencepointcollection.md)
-   [**\_ReferencePointOfVirtualSystem MSVM**](msvm-referencepointofvirtualsystem.md)
-   [**\_ReferencePointOfVirtualSystemCollection MSVM**](msvm-referencepointofvirtualsystemcollection.md)
-   [**\_ResourceDependentOnResource MSVM**](msvm-resourcedependentonresource.md)
-   [**\_SerialPortSettingData MSVM**](msvm-serialportsettingdata.md)
-   [**\_ServiceOfVssComponent MSVM**](msvm-serviceofvsscomponent.md)
-   [**MSVM \_ snapshotcollection**](msvm-snapshotcollection.md)
-   [**\_SnapshotOfVirtualSystemCollection MSVM**](msvm-snapshotofvirtualsystemcollection.md)
-   [**\_StandaloneV2ElementConformsToProfile MSVM**](msvm-standalonev2elementconformstoprofile.md)
-   [**\_SyntheticDisplayControllerSettingData MSVM**](msvm-syntheticdisplaycontrollersettingdata.md)
-   [**\_SyntheticKeyboard MSVM**](msvm-synthetickeyboard.md)
-   [**\_TPM MSVM**](msvm-tpm.md)
-   [**\_TPMSettingData MSVM**](msvm-tpmsettingdata.md)
-   [**\_VHDSetInformation MSVM**](msvm-vhdsetinformation.md)
-   [**\_VHDSnapshotInformation MSVM**](msvm-vhdsnapshotinformation.md)
-   [**\_VirtualEthernetSwitchNicTeamingMember MSVM**](msvm-virtualethernetswitchnicteamingmember.md)
-   [**\_VirtualEthernetSwitchNicTeamingSettingData MSVM**](msvm-virtualethernetswitchnicteamingsettingdata.md)
-   [**\_VirtualMachineToDisks MSVM**](msvm-virtualmachinetodisks.md)
-   [**\_VirtualSystemCollection MSVM**](msvm-virtualsystemcollection.md)
-   [**\_VirtualSystemReferencePoint MSVM**](msvm-virtualsystemreferencepoint.md)
-   [**\_VirtualSystemReferencePointExportSettingData MSVM**](msvm-virtualsystemreferencepointexportsettingdata.md)
-   [**\_VirtualSystemReferencePointService MSVM**](msvm-virtualsystemreferencepointservice.md)
-   [**\_VirtualSystemReferencePointSettingData MSVM**](msvm-virtualsystemreferencepointsettingdata.md)
-   [**\_VirtualSystemSnapshotSettingData MSVM**](msvm-virtualsystemsnapshotsettingdata.md)
-   [**\_VssService MSVM**](msvm-vssservice.md)

Classe rimossa:

-   [**\_ResourcePoolComponent MSVM**](msvm-resourcepoolcomponent.md)
-   [**\_ResourcePoolRegistration MSVM**](msvm-resourcepoolregistration.md)
-   [**\_ResourcePoolSettingData MSVM**](msvm-resourcepoolsettingdata.md)
-   [**\_VirtualizationComponent MSVM**](msvm-virtualizationcomponent.md)
-   [**\_VirtualizationComponentRegistration MSVM**](msvm-virtualizationcomponentregistration.md)

Proprietà nuove:

-   [**MSVM \_ BootSourceSettingData**](msvm-bootsourcesettingdata.md): **OptionalData**
-   [**MSVM \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md): **LastKnownSwitchName** e **CompartmentGuid**
-   [**MSVM \_ EthernetSwitchHardwareOffloadData**](msvm-ethernetswitchhardwareoffloaddata.md): **PacketDirectInUse**
-   [**MSVM \_ EthernetSwitchPortOffloadSettingData**](msvm-ethernetswitchportoffloadsettingdata.md): **PacketDirectModerationInterval**, **PacketDirectModerationCount**, **PacketDirectNumProcs**,
-   [**MSVM \_ EthernetSwitchPortSecuritySettingData**](msvm-ethernetswitchportsecuritysettingdata.md): **EnableFixSpeed10G** e **riservato**
-   [**MSVM \_ GuestServiceInterfaceComponentSettingData**](msvm-guestserviceinterfacecomponentsettingdata.md): **DefaultEnabledStatePolicy**
-   [**MSVM \_ ProcessorSettingData**](msvm-processorsettingdata.md): **EnableHostResourceProtection**
-   [**MSVM \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md): **StorageQoSPolicyID**, **CachingMode** e **snapshotID**
-   [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md): **InstanceID**, **Version**, **ThumbnailImageHeight**, **ThumbnailImageWidth** e **HostComputerSystemName**
-   [**MSVM \_ Synthetic3DDisplayControllerSettingData**](msvm-synthetic3ddisplaycontrollersettingdata.md): **VRAMSizeBytes**
-   [**MSVM \_ VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md): **TeamingEnabled** e **PacketDirectEnabled**
-   [**MSVM \_ VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md): **ParentTimestamp** e **ParentIdentifier**
-   [**MSVM \_ VirtualHardDiskState**](msvm-virtualharddiskstate.md): **timestamp**
-   [**MSVM \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md): **BackupIntent** e **DifferentialBackupBase**
-   [**MSVM \_ VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md): **DefaultVirtualHardDiskCachingMode**
-   [**MSVM \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md): **RemoveSourceUnmanagedVhds** e **UnmanagedVhds**
-   [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md): **UserSnapshotType**, **GuestControlledCacheTypes**, **LockOnDisconnect**, **ParentPackage**, **AutomaticCriticalErrorActionTimeout**, **AutomaticCriticalErrorAction**, **ConsoleMode** e **SecureBootTemplateId**

Nuovi metodi:

-   [**MSVM \_ Classe servizio**](msvm-imagemanagementservice.md) : [**ConvertVirtualHardDiskToVHDSet**](msvm-imagemanagementservice-convertvirtualharddisktovhdset.md), [**DeleteVHDSnapshot**](msvm-imagemanagementservice-deletevhdsnapshot.md), [**FindMountedStorageImageInstance**](msvm-imagemanagementservice-findmountedstorageimageinstance.md), [**GetVHDSetInformation**](msvm-imagemanagementservice-getvhdsetinformation.md), [**GetVHDSnapshotInformation**](msvm-imagemanagementservice-getvhdsnapshotinformation.md), [**GetVirtualDiskChanges**](msvm-imagemanagementservice-getvirtualdiskchanges.md), [**OptimizeVHDSet**](msvm-imagemanagementservice-optimizevhdset.md)e [**SetVHDSnapshotInformation**](msvm-imagemanagementservice-setvhdsnapshotinformation.md)
-   [**MSVM \_ Classe ShutdownComponent**](msvm-shutdowncomponent.md) : [ **InitiateReboot**](msvm-shutdowncomponent-initiatereboot.md)
-   [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md): [**AddBootSourceSettings**](msvm-virtualsystemmanagementservice-addbootsourcesettings.md), [**AddGuestServiceSettings**](msvm-virtualsystemmanagementservice-addguestservicesettings.md), [**DefinePlannedSystem**](msvm-virtualsystemmanagementservice-defineplannedsystem.md), [**ModifyGuestServiceSettings**](msvm-virtualsystemmanagementservice-modifyguestservicesettings.md), [**RemoveBootSourceSettings**](msvm-virtualsystemmanagementservice-removebootsourcesettings.md), [**RemoveGuesServiceSettings**](msvm-virtualsystemmanagementservice-removeguestservicesettings.md), [**SetInitialMachineConfigurationData**](msvm-virtualsystemmanagementservice-setinitialmachineconfigurationdata.md)e [**UpgradeSystemVersion**](msvm-virtualsystemmanagementservice-upgradesystemversion.md)
-   [**MSVM \_ Classe VirtualSystemSnapshotService**](msvm-virtualsystemsnapshotservice.md) : [ **ConvertToReferencePoint**](msvm-virtualsystemsnapshotservice-converttoreferencepoint.md)

## <a name="windows-81-and-windows-server-2012-r2"></a>Windows 8.1 e Windows Server 2012 R2

Windows 8.1 e Windows Server 2012 R2 includono nuove funzionalità per la versione 2 del provider WMI Hyper-V.

-   Le proprietà **IOPSAllocationUnits**, **IOPSLimit**, **IOPSReservation** e **PersistentReservationsSupported** sono state aggiunte alla classe MSVM [**\_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) .
-   La proprietà **VirtualDiskId** è stata aggiunta alla classe [**\_ VirtualHardDiskSettingData di MSVM**](msvm-virtualharddisksettingdata.md) .
-   Informazioni su QoS di archiviazione sono state aggiunte alla proprietà **OperationalStatus** delle classi [**MSVM \_ disco logico**](msvm-logicaldisk.md) e [**MSVM \_ ResourcePool**](msvm-resourcepool.md) .
-   [**MSVM \_ Classe StorageAlert**](msvm-storagealert.md)
-   È stata aggiunta la proprietà **ClusterMonitored** alle classi [**MSVM \_ EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) e [**MSVM \_ SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) .
-   Sono state aggiunte le proprietà **EnableCompression** e **EnableSmbTransport** alla classe [**MSVM \_ VirtualSystemMigrationServiceSettingData**](msvm-virtualsystemmigrationservicesettingdata.md) .
-   La proprietà **EnableCompression** è stata aggiunta alla classe [**\_ VirtualSystemMigrationSettingData di MSVM**](msvm-virtualsystemmigrationsettingdata.md) . La proprietà **TransportType** include informazioni sulla migrazione in tempo reale.
-   [**MSVM \_ Classe CopyFileToGuestJob**](msvm-copyfiletoguestjob.md)
-   [**MSVM \_ Classe CopyFileToGuestSettingData**](msvm-copyfiletoguestsettingdata.md)
-   [**MSVM \_ Classe GuestFileService**](msvm-guestfileservice.md)
-   [**MSVM \_ Classe GuestService**](msvm-guestservice.md)
-   [**MSVM \_ Classe GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md)
-   [**MSVM \_ Classe GuestServiceInterfaceComponentSettingData**](msvm-guestserviceinterfacecomponentsettingdata.md)
-   [**MSVM \_ Classe RegisteredGuestService**](msvm-registeredguestservice.md)
-   La proprietà **EnhancedSessionModeEnabled** è stata aggiunta alla classe [**\_ VirtualSystemManagementServiceSettingData di MSVM**](msvm-virtualsystemmanagementservicesettingdata.md) .
-   La proprietà **EnhancedModeState** e il metodo [**InjectNonMaskableInterrupt**](injectnonmaskableinterrupt-msvm-computersystem.md) sono stati aggiunti alla classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) .
-   Le proprietà **BootSourceOrder**, **LowMmioGapSize**, **NetworkBootPreferredProtocol**, **PauseAfterBootFailure** , **della securebootenabled** e **VirtualSystemSubType** sono state aggiunte alla classe [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) .
-   [**MSVM \_ Classe BootSourceSettingData**](msvm-bootsourcesettingdata.md)
-   [**MSVM \_ Classe BootSourceComponent**](msvm-bootsourcecomponent.md)
-   [**MSVM \_ Classe LogicalIdentity**](msvm-logicalidentity.md)
-   [**MSVM \_ Classe CompatibilityVector**](msvm-compatibilityvector.md)
-   Il metodo [**GetSystemCompatibilityVectors**](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md) è stato aggiunto alla classe [**\_ VirtualSystemMigrationService di MSVM**](msvm-virtualsystemmigrationservice.md) .
-   Le proprietà **ReplicationStateEx**, **ReplicationHealthEx**, **EnhancedSessionModeState**, **VirtualSwitchNames** e **VirtualSystemSubType** sono state aggiunte alla classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) . Le proprietà **ReplicationState** e **ReplicationHealth** sono deprecate e sostituite dalle proprietà **ReplicationStateEx** e **ReplicationHealthEx** .
-   La proprietà **PnpDevicePath** è stata aggiunta alla classe [**\_ MountedStorageImage di MSVM**](msvm-mountedstorageimage.md) .
-   Sono state aggiunte le proprietà **AllowedHashAlgorithms** e **TrustedIssuerCertificateHashes** alla classe [**MSVM \_ TerminalServiceSettingData**](msvm-terminalservicesettingdata.md) .

Windows 8.1 e Windows Server 2012 R2 includono nuove funzionalità per la replica delle macchine virtuali e il ripristino del failover.

-   [**MSVM \_ Classe ReplicationProvider**](msvm-replicationprovider.md)
-   [**MSVM \_ Classe ReplicationRelationship**](msvm-replicationrelationship.md)
-   I metodi [**ChangeReplicationModeToPrimary**](changereplicationmodetoprimary-msvm-replicationservice.md), [**GetReplicationStatisticsEx**](getreplicationstatisticsex-msvm-replicationservice.md), [**InitiateFailback**](initiatefailback-msvm-replicationservice.md), [**RemoveReplicationRelationshipEx**](removereplicationrelationshipex-msvm-replicationservice.md)e [**ResetReplicationStatisticsEx**](resetreplicationstatisticsex-msvm-replicationservice.md) sono stati aggiunti alla classe [**MSVM \_ ReplicationService**](msvm-replicationservice.md) . I metodi **GetReplicationStatisticsEx**, **RemoveReplicationRelationshipEx** e **ResetReplicationStatisticsEx** sostituiscono i metodi [**GetReplicationStatistics**](getreplicationstatistics-msvm-replicationservice.md), [**RemoveReplicationRelationship**](removereplicationrelationship-msvm-replicationservice.md)e [**ResetReplicationStatistics**](resetreplicationstatistics-msvm-replicationservice.md) .
-   La classe [**MSVM \_ SystemReplicationRelationship**](msvm-systemreplicationrelationship.md) Mostra un'associazione tra una macchina virtuale e molte relazioni di replica.
-   Sono state aggiunte le proprietà **AdditionalSettings** e **ReplicationProvider** alla classe [**MSVM \_ ReplicationSettingData**](msvm-replicationsettingdata.md) .
-   Informazioni sul provider da host a host sono state aggiunte ai metodi [**CreateReplicationRelationship**](createreplicationrelationship-msvm-replicationservice.md) e [**ModifyReplicationSettings**](modifyreplicationsettings-msvm-replicationservice.md) della classe [**MSVM \_ ReplicationService**](msvm-replicationservice.md) .
-   Il metodo [**RequestReplicationStateChangeEx**](msvm-requestreplicationstatechangeex-computersystem.md) è stato aggiunto alla classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) e sostituisce il metodo [**RequestReplicationStateChange**](msvm-computersystem-requestreplicationstatechange.md) . La proprietà **InstanceID** può ora indicare la replica estesa. Per ulteriori informazioni sulla replica estesa, vedere [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).
-   [**MSVM \_**](msvm-replicationsettingdata.md) Le istanze di ReplicationSettingData e [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) hanno una relazione 1:1 che è possibile rappresentare con un'associazione [**MSVM \_ SettingsDefineState**](msvm-settingsdefinestate.md) .

    | [**MSVM \_**](msvm-settingsdefinestate.md) Nome della proprietà SettingsDefineState | Valore                                                                                                |
    |-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
    | **ManagedElement**                                                          | Rappresenta l'oggetto [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md)          |
    | **SettingData**                                                             | Rappresenta l'oggetto [**\_ ReplicationSettingData MSVM**](msvm-replicationsettingdata.md) associato |

    

     

-   [**MSVM \_ ReplicationSettingData**](msvm-replicationsettingdata.md) può distinguere tra le istanze dell'impostazione per la relazione di replica in base alla proprietà **InstanceID** o **ReplicationRelationship** . Pertanto, questi metodi che gestiscono una singola relazione non hanno modificato la firma:

    -   [**MSVM \_ ReplicationService:: CreateReplicationRelationship**](createreplicationrelationship-msvm-replicationservice.md)
    -   [**MSVM \_ ReplicationService:: ModifyReplicationSettings**](modifyreplicationsettings-msvm-replicationservice.md)
    -   [**MSVM \_ ReplicationService:: Resync**](resynchronize-msvm-replicationservice.md)
    -   [**MSVM \_ ReplicationService:: StartReplication**](startreplication-msvm-replicationservice.md)

-   Sebbene sia possibile utilizzare [**GetReplicationStatistics**](getreplicationstatistics-msvm-replicationservice.md), [**RemoveReplicationRelationship**](removereplicationrelationship-msvm-replicationservice.md)e [**RequestReplicationStateChange**](msvm-computersystem-requestreplicationstatechange.md) sempre per la relazione primaria, è consigliabile utilizzare invece [**GetReplicationStatisticsEx**](getreplicationstatisticsex-msvm-replicationservice.md), [**RemoveReplicationRelationshipEx**](removereplicationrelationshipex-msvm-replicationservice.md)e [**RequestReplicationStateChangeEx**](msvm-requestreplicationstatechangeex-computersystem.md) , perché possono elaborare la relazione di replica primaria ed estesa. Per ulteriori informazioni sulla replica estesa, vedere [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).
-   Sebbene queste proprietà della classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) continuino a indicare lo stato per la relazione di replica primaria, usare invece queste proprietà di un oggetto [**\_ ReplicationRelationship MSVM**](msvm-replicationrelationship.md) per determinare lo stato corrente per la relazione di replica primaria e estesa.

    | Nome proprietà                                | Type        |
    |----------------------------------------------|-------------|
    | **ReplicationState**                         | UInt16 (RO) |
    | **ReplicationHealth**                        | UInt16 (RO) |
    | **LastReplicationTime**                      | Datetime    |
    | **FailedOverReplicationType**                | UInt16      |
    | **LastApplicationConsistentReplicationTime** | Datetime    |
    | **LastReplicationType**                      | UInt16      |

    

     

 

 




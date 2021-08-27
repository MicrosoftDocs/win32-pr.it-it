---
title: MDM_Policy_Config01_Defender02 classe
description: La classe MDM \_ Policy \_ Config01 \_ Defender02class rappresenta i criteri correlati Windows Defender.
ms.assetid: 6d9d4edd-fcb6-45ea-bc5d-1bffb9cf8740
keywords:
- MDM_Policy_Config01_Defender02 classe
- MDM_Policy_Config01_Defender02 classe , descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Defender02
- MDM_Policy_Config01_Defender02.InstanceID
- MDM_Policy_Config01_Defender02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a9ae2c86b030c936f3dec88f8f48f806f0dd1d5d8430b7610ee51f567898c8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104261"
---
# <a name="mdm_policy_config01_defender02-class"></a>Classe MDM \_ Policy \_ Config01 \_ Defender02

\[Alcune informazioni riguardano un prodotto pre-rilasciato che può essere modificato sostanzialmente prima del rilascio in commercio. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La **classe MDM Policy \_ \_ Config01 \_ Defender02** rappresenta i criteri correlati Windows Defender

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Defender02
{
  string InstanceID;
  string ParentID;
  sint32 AllowArchiveScanning;
  sint32 AllowBehaviorMonitoring;
  sint32 AllowCloudProtection;
  sint32 AllowEmailScanning;
  sint32 AllowFullScanOnMappedNetworkDrives;
  sint32 AllowFullScanRemovableDriveScanning;
  sint32 AllowIntrusionPreventionSystem;
  sint32 AllowIOAVProtection;
  sint32 AllowOnAccessProtection;
  sint32 AllowRealtimeMonitoring;
  sint32 AllowScanningNetworkFiles;
  sint32 AllowScriptScanning;
  sint32 AllowUserUIAccess;
  string AttackSurfaceReductionRules;
  string AttackSurfaceReductionOnlyExclusions;
  sint32 AVGCPULoadFactor;
  sint32 CloudExtendedTimeout;
  string ControlledFolderAccessProtectedFolders;
  string ControlledFolderAccessAllowedApplications;
  sint32 CloudBlockLevel;
  sint32 DaysToRetainCleanedMalware;
  sint32 EnableControlledFolderAccess;
  sint32 EnableNetworkProtection;
  sint32 PUAProtection;
  string ExcludedProcesses;
  string ExcludedPaths;
  string ExcludedExtensions;
  sint32 RealTimeScanDirection;
  sint32 ScanParameter;
  sint32 ScheduleQuickScanTime;
  sint32 ScheduleScanDay;
  sint32 ScheduleScanTime;
  sint32 SignatureUpdateInterval;
  sint32 SubmitSamplesConsent;
  string ThreatSeverityDefaultAction;
};
```

## <a name="members"></a>Members

La **classe MDM Policy \_ \_ Config01 \_ Defender02** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe MDM Policy \_ \_ Config01 \_ Defender02** ha queste proprietà.

<dl> <dt>

[AllowArchiveScanning](/windows/client-management/mdm/policy-csp-defender#defender-allowarchivescanning)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

[AllowBehaviorMonitoring](/windows/client-management/mdm/policy-csp-defender#defender-allowbehaviormonitoring)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

[AllowCloudProtection](/windows/client-management/mdm/policy-csp-defender#defender-allowcloudprotection)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

[AllowEmailScanning](/windows/client-management/mdm/policy-csp-defender#defender-allowemailscanning)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

[AllowFullScanOnMappedNetworkDrives](/windows/client-management/mdm/policy-csp-defender#defender-allowfullscanonmappednetworkdrives)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

[AllowFullScanRemovableDriveScanning](/windows/client-management/mdm/policy-csp-defender#defender-allowfullscanremovabledrivescanning)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

[AllowIntrusionPreventionSystem](/windows/client-management/mdm/policy-csp-defender#defender-allowintrusionpreventionsystem)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

[AllowIOAVProtection](/windows/client-management/mdm/policy-csp-defender#defender-allowioavprotection)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

[AllowOnAccessProtection](/windows/client-management/mdm/policy-csp-defender#defender-allowonaccessprotection)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

[AllowRealtimeMonitoring](/windows/client-management/mdm/policy-csp-defender#defender-allowrealtimemonitoring)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

[AllowScanningNetworkFiles](/windows/client-management/mdm/policy-csp-defender#defender-allowscanningnetworkfiles)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

[AllowScriptScanning](/windows/client-management/mdm/policy-csp-defender#defender-allowscriptscanning)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

[AllowUserUIAccess](/windows/client-management/mdm/policy-csp-defender#defender-allowuseruiaccess)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

[AttackSurfaceReductionOnlyExclusions](/windows/client-management/mdm/policy-csp-defender#defender-attacksurfacereductiononlyexclusions)
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

[AttackSurfaceReductionRules](/windows/client-management/mdm/policy-csp-defender#defender-attacksurfacereductionrules)
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

[AVGCPULoadFactor](/windows/client-management/mdm/policy-csp-defender#defender-avgcpuloadfactor)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

[CloudBlockLevel](/windows/client-management/mdm/policy-csp-defender#defender-cloudblocklevel)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

[CloudExtendedTimeout](/windows/client-management/mdm/policy-csp-defender#defender-cloudextendedtimeout)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

[ControlledFolderAccessAllowedApplications](/windows/client-management/mdm/policy-csp-defender#defender-controlledfolderaccessallowedapplications)
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

[ControlledFolderAccessProtectedFolders](/windows/client-management/mdm/policy-csp-defender#defender-controlledfolderaccessprotectedfolders)
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

[DaysToRetainCleanedMalware](/windows/client-management/mdm/policy-csp-defender#defender-daystoretaincleanedmalware)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

[EnableControlledFolderAccess](/windows/client-management/mdm/policy-csp-defender#defender-enablecontrolledfolderaccess)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

[EnableNetworkProtection](/windows/client-management/mdm/policy-csp-defender#defender-enablenetworkprotection)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

[ExcludedExtensions](/windows/client-management/mdm/policy-csp-defender#defender-excludedextensions)
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

[ExcludedPaths](/windows/client-management/mdm/policy-csp-defender#defender-excludedpaths)
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

[ExcludedProcesses](/windows/client-management/mdm/policy-csp-defender#defender-excludedprocesses)
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifica il nome del nodo padre. Per questa classe, la stringa è "Defender".

</dd> <dt>

**Parentid**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Descrive il percorso completo del nodo padre. Per questa classe, la stringa è "./Vendor/MSFT/Policy/Config"

</dd> <dt>

[PUAProtection](/windows/client-management/mdm/policy-csp-defender#defender-puaprotection)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

</dd> <dt>

[RealTimeScanDirection](/windows/client-management/mdm/policy-csp-defender#defender-realtimescandirection)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

</dd> <dt>

[ScanParameter](/windows/client-management/mdm/policy-csp-defender#defender-scanparameter)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

</dd> <dt>

[ScheduleQuickScanTime](/windows/client-management/mdm/policy-csp-defender#defender-schedulequickscantime)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

</dd> <dt>

[ScheduleScanDay](/windows/client-management/mdm/policy-csp-defender#defender-schedulescanday)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

</dd> <dt>

[ScheduleScanTime](/windows/client-management/mdm/policy-csp-defender#defender-schedulescantime)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

</dd> <dt>

[SignatureUpdateInterval](/windows/client-management/mdm/policy-csp-defender#defender-signatureupdateinterval)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

</dd> <dt>

[SubmitSamplesConsent](/windows/client-management/mdm/policy-csp-defender#defender-submitsamplesconsent)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

</dd> <dt>

[ThreatSeverityDefaultAction](/windows/client-management/mdm/policy-csp-defender#defender-threatseveritydefaultaction)
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                      |
| Spazio dei nomi<br/>                | DMMap \\ MDM CIMv2 \\ \\ radice<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso di script di PowerShell con il provider bridge WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 


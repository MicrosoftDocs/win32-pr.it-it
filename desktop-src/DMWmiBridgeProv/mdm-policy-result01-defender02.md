---
title: Classe MDM_Policy_Result01_Defender02
description: Il \_ criterio MDM \_ Result01 \_ Defender02class rappresenta i criteri correlati a Windows Defender.
ms.assetid: 82c8a7a2-8369-46c4-aa87-b44b742a274d
keywords:
- Classe MDM_Policy_Result01_Defender02
- Classe MDM_Policy_Result01_Defender02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Defender02
- MDM_Policy_Result01_Defender02.InstanceID
- MDM_Policy_Result01_Defender02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae898751a9f15af1c945efd3e6a473dfe07c7cd7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475892"
---
# <a name="mdm_policy_result01_defender02-class"></a>\_ \_ Classe Result01 Defender02 di criteri \_ MDM

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La **classe \_ \_ Result01 \_ Defender02 dei criteri MDM** rappresenta i criteri correlati a Windows Defender

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Defender02
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
  sint32 ScheduleQuickScanTime;
  sint32 ScheduleScanDay;
  sint32 ScheduleScanTime;
  sint32 SignatureUpdateInterval;
  sint32 SubmitSamplesConsent;
  string ThreatSeverityDefaultAction;
  sint32 ScanParameter;
};
```

## <a name="members"></a>Members

La **classe \_ \_ Result01 \_ Defender02 dei criteri MDM** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ \_ \_ Defender02 dei criteri MDM Result01** ha queste proprietà.

<dl> <dt>

[AllowArchiveScanning](/windows/client-management/mdm/policy-csp-defender#defender-allowarchivescanning)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[AllowBehaviorMonitoring](/windows/client-management/mdm/policy-csp-defender#defender-allowbehaviormonitoring)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[AllowCloudProtection](/windows/client-management/mdm/policy-csp-defender#defender-allowcloudprotection)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[AllowEmailScanning](/windows/client-management/mdm/policy-csp-defender#defender-allowemailscanning)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[AllowFullScanOnMappedNetworkDrives](/windows/client-management/mdm/policy-csp-defender#defender-allowfullscanonmappednetworkdrives)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[AllowFullScanRemovableDriveScanning](/windows/client-management/mdm/policy-csp-defender#defender-allowfullscanremovabledrivescanning)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[AllowIntrusionPreventionSystem](/windows/client-management/mdm/policy-csp-defender#defender-allowintrusionpreventionsystem)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[AllowIOAVProtection](/windows/client-management/mdm/policy-csp-defender#defender-allowioavprotection)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[AllowOnAccessProtection](/windows/client-management/mdm/policy-csp-defender#defender-allowonaccessprotection)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[AllowRealtimeMonitoring](/windows/client-management/mdm/policy-csp-defender#defender-allowrealtimemonitoring)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[AllowScanningNetworkFiles](/windows/client-management/mdm/policy-csp-defender#defender-allowscanningnetworkfiles)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[AllowScriptScanning](/windows/client-management/mdm/policy-csp-defender#defender-allowscriptscanning)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[AllowUserUIAccess](/windows/client-management/mdm/policy-csp-defender#defender-allowuseruiaccess)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[AttackSurfaceReductionOnlyExclusions](/windows/client-management/mdm/policy-csp-defender#defender-attacksurfacereductiononlyexclusions)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[AttackSurfaceReductionRules](/windows/client-management/mdm/policy-csp-defender#defender-attacksurfacereductionrules)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[AVGCPULoadFactor](/windows/client-management/mdm/policy-csp-defender#defender-avgcpuloadfactor)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[CloudBlockLevel](/windows/client-management/mdm/policy-csp-defender#defender-cloudblocklevel)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[CloudExtendedTimeout](/windows/client-management/mdm/policy-csp-defender#defender-cloudextendedtimeout)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[ControlledFolderAccessAllowedApplications](/windows/client-management/mdm/policy-csp-defender#defender-controlledfolderaccessallowedapplications)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[ControlledFolderAccessProtectedFolders](/windows/client-management/mdm/policy-csp-defender#defender-controlledfolderaccessprotectedfolders)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[DaysToRetainCleanedMalware](/windows/client-management/mdm/policy-csp-defender#defender-daystoretaincleanedmalware)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[EnableControlledFolderAccess](/windows/client-management/mdm/policy-csp-defender#defender-enablecontrolledfolderaccess)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[EnableNetworkProtection](/windows/client-management/mdm/policy-csp-defender#defender-enablenetworkprotection)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[ExcludedExtensions](/windows/client-management/mdm/policy-csp-defender#defender-excludedextensions)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[ExcludedPaths](/windows/client-management/mdm/policy-csp-defender#defender-excludedpaths)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[ExcludedProcesses](/windows/client-management/mdm/policy-csp-defender#defender-excludedprocesses)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifica il nome del nodo padre. Per questa classe la stringa è "Defender".

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Descrive il percorso completo del nodo padre. Per questa classe la stringa è "./Vendor/MSFT/Policy/Result"

</dd> <dt>

[PUAProtection](/windows/client-management/mdm/policy-csp-defender#defender-puaprotection)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[RealTimeScanDirection](/windows/client-management/mdm/policy-csp-defender#defender-realtimescandirection)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[ScanParameter](/windows/client-management/mdm/policy-csp-defender#defender-scanparameter)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[ScheduleQuickScanTime](/windows/client-management/mdm/policy-csp-defender#defender-schedulequickscantime)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[ScheduleScanDay](/windows/client-management/mdm/policy-csp-defender#defender-schedulescanday)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[ScheduleScanTime](/windows/client-management/mdm/policy-csp-defender#defender-schedulescantime)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[SignatureUpdateInterval](/windows/client-management/mdm/policy-csp-defender#defender-signatureupdateinterval)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[SubmitSamplesConsent](/windows/client-management/mdm/policy-csp-defender#defender-submitsamplesconsent)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[ThreatSeverityDefaultAction](/windows/client-management/mdm/policy-csp-defender#defender-threatseveritydefaultaction)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                      |
| Spazio dei nomi<br/>                | \\ \\ DMMap MDM CIMv2 \\ radice<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilizzo di script di PowerShell con il provider del Bridge WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 


---
title: Classe MDM_Policy_Result01_Privacy02
description: La \_ classe Update02 dei criteri MDM \_ Result01 \_ rappresenta i criteri di aggiornamento disponibili.
ms.assetid: 06604da6-5298-4273-a030-529491c2823c
keywords:
- Classe MDM_Policy_Result01_Privacy02
- Classe MDM_Policy_Result01_Update02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Update02
- MDM_Policy_Result01_Update02.InstanceID
- MDM_Policy_Result01_Update02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0be844bb4ef8fc20e7ab5bbc8b7709cdfde4034
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963796"
---
# <a name="mdm_policy_result01_update02-class"></a>\_ \_ Classe Result01 Update02 di criteri \_ MDM

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La **classe \_ \_ \_ Update02 dei criteri MDM Result01** rappresenta i criteri di aggiornamento disponibili.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Update02
{
  string InstanceID;
  string ParentID;
  sint32 RequireUpdateApproval;
  sint32 AllowAutoUpdate;
  sint32 AllowAutoWindowsUpdateDownloadOverMeteredNetwork;
  sint32 AllowMUUpdateService;
  sint32 ScheduledInstallDay;
  sint32 ScheduledInstallThirdWeek;
  sint32 ScheduledInstallSecondWeek;
  sint32 ScheduledInstallFourthWeek;
  sint32 ScheduledInstallFirstWeek;
  sint32 ScheduledInstallEveryWeek;
  sint32 ScheduledInstallTime;
  sint32 AllowUpdateService;
  sint32 DeferQualityUpdatesPeriodInDays;
  sint32 DeferFeatureUpdatesPeriodInDays;
  sint32 BranchReadinessLevel;
  string UpdateServiceUrl;
  sint32 SetEDURestart;
  sint32 AutoRestartDeadlinePeriodInDays;
  string UpdateServiceUrlAlternate;
  sint32 FillEmptyContentUrls;
  sint32 AllowNonMicrosoftSignedUpdate;
  sint32 RequireDeferUpgrade;
  sint32 PauseDeferrals;
  sint32 PauseQualityUpdates;
  sint32 PhoneUpdateRestrictions;
  string PauseQualityUpdatesStartTime;
  sint32 PauseFeatureUpdates;
  string PauseFeatureUpdatesStartTime;
  sint32 DeferUpgradePeriod;
  sint32 ExcludeWUDriversInQualityUpdate;
  sint32 IgnoreMOUpdateDownloadLimit;
  sint32 ManagePreviewBuilds;
  sint32 IgnoreMOAppDownloadLimit;
  sint32 DeferUpdatePeriod;
  sint32 ActiveHoursEnd;
  sint32 ActiveHoursStart;
  sint32 DetectionFrequency;
  sint32 DisableDualScan;
  sint32 EngagedRestartDeadline;
  sint32 EngagedRestartSnoozeSchedule;
  sint32 EngagedRestartTransitionSchedule;
  sint32 ScheduleImminentRestartWarning;
  sint32 ScheduleRestartWarning;
  sint32 SetAutoRestartNotificationDisable;
  sint32 AutoRestartNotificationSchedule;
  sint32 AutoRestartRequiredNotificationDismissal;
  sint32 ActiveHoursMaxRange;
};
```

## <a name="members"></a>Members

La **classe \_ \_ Result01 \_ Update02 dei criteri MDM** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ \_ \_ Update02 dei criteri MDM Result01** ha queste proprietà.

<dl> <dt>

[ActiveHoursEnd](/windows/client-management/mdm/policy-csp-update#update-activehoursend)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[ActiveHoursMaxRange](/windows/client-management/mdm/policy-csp-update#update-activehoursmaxrange)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[ActiveHoursStart](/windows/client-management/mdm/policy-csp-update#update-activehoursstart)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[AllowAutoUpdate](/windows/client-management/mdm/policy-csp-update#update-allowautoupdate)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[AllowAutoWindowsUpdateDownloadOverMeteredNetwork](/windows/client-management/mdm/policy-csp-update#update-allowautowindowsupdatedownloadovermeterednetwork)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[AllowMUUpdateService](/windows/client-management/mdm/policy-csp-update#update-allowmuupdateservice)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[AllowNonMicrosoftSignedUpdate](/windows/client-management/mdm/policy-csp-update#update-allownonmicrosoftsignedupdate)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[AllowUpdateService](/windows/client-management/mdm/policy-csp-update#update-allowupdateservice)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[AutoRestartDeadlinePeriodInDays](/windows/client-management/mdm/policy-csp-update#update-autorestartdeadlineperiodindays)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[AutoRestartNotificationSchedule](/windows/client-management/mdm/policy-csp-update#update-autorestartnotificationschedule)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[AutoRestartRequiredNotificationDismissal](/windows/client-management/mdm/policy-csp-update#update-autorestartrequirednotificationdismissal)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[BranchReadinessLevel](/windows/client-management/mdm/policy-csp-update#update-branchreadinesslevel)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[DeferFeatureUpdatesPeriodInDays](/windows/client-management/mdm/policy-csp-update#update-deferfeatureupdatesperiodindays)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[DeferQualityUpdatesPeriodInDays](/windows/client-management/mdm/policy-csp-update#update-deferqualityupdatesperiodindays)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[DeferUpdatePeriod](/windows/client-management/mdm/policy-csp-update#update-deferupdateperiod)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[DeferUpgradePeriod](/windows/client-management/mdm/policy-csp-update#update-deferupgradeperiod)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[DetectionFrequency](/windows/client-management/mdm/policy-csp-update#update-detectionfrequency)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[DisableDualScan](/windows/client-management/mdm/policy-csp-update#update-disabledualscan)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[EngagedRestartDeadline](/windows/client-management/mdm/policy-csp-update#update-engagedrestartdeadline)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[EngagedRestartSnoozeSchedule](/windows/client-management/mdm/policy-csp-update#update-engagedrestartsnoozeschedule)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[EngagedRestartTransitionSchedule](/windows/client-management/mdm/policy-csp-update#update-engagedrestarttransitionschedule)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[ExcludeWUDriversInQualityUpdate](/windows/client-management/mdm/policy-csp-update#update-excludewudriversinqualityupdate)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[FillEmptyContentUrls](/windows/client-management/mdm/policy-csp-update#update-fillemptycontenturls)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[IgnoreMOAppDownloadLimit](/windows/client-management/mdm/policy-csp-update#update-ignoremoappdownloadlimit)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[IgnoreMOUpdateDownloadLimit](/windows/client-management/mdm/policy-csp-update#update-ignoremoupdatedownloadlimit)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
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

Identifica il nome del nodo padre. Per questa classe la stringa è "Update".

</dd> <dt>

[ManagePreviewBuilds](/windows/client-management/mdm/policy-csp-update#update-managepreviewbuilds)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

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

[PauseDeferrals](/windows/client-management/mdm/policy-csp-update#update-pausedeferrals)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[PauseFeatureUpdates](/windows/client-management/mdm/policy-csp-update#update-pausefeatureupdates)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[PauseFeatureUpdatesStartTime](/windows/client-management/mdm/policy-csp-update#update-pausefeatureupdatesstarttime)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[PauseQualityUpdates](/windows/client-management/mdm/policy-csp-update#update-pausequalityupdates)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[PauseQualityUpdatesStartTime](/windows/client-management/mdm/policy-csp-update#update-pausequalityupdatesstarttime)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[PhoneUpdateRestrictions](/windows/client-management/mdm/policy-csp-update#update-phoneupdaterestrictions)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[RequireDeferUpgrade](/windows/client-management/mdm/policy-csp-update#update-requiredeferupgrade)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[RequireUpdateApproval](/windows/client-management/mdm/policy-csp-update#update-requireupdateapproval)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[ScheduledInstallDay](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallday)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[ScheduledInstallEveryWeek](/windows/client-management/mdm/policy-csp-update#update-scheduledinstalleveryweek)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[ScheduledInstallFirstWeek](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallfirstweek)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[ScheduledInstallFourthWeek](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallfourthweek)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[ScheduledInstallSecondWeek](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallsecondweek)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[ScheduledInstallThirdWeek](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallthirdweek)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[ScheduledInstallTime](/windows/client-management/mdm/policy-csp-update#update-scheduledinstalltime)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[ScheduleImminentRestartWarning](/windows/client-management/mdm/policy-csp-update#update-scheduleimminentrestartwarning)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[ScheduleRestartWarning](/windows/client-management/mdm/policy-csp-update#update-schedulerestartwarning)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[SetAutoRestartNotificationDisable](/windows/client-management/mdm/policy-csp-update#update-setautorestartnotificationdisable)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[SetEDURestart](/windows/client-management/mdm/policy-csp-update#update-setedurestart)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[UpdateServiceUrl](/windows/client-management/mdm/policy-csp-update#update-updateserviceurl)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[UpdateServiceUrlAlternate](/windows/client-management/mdm/policy-csp-update#update-updateserviceurlalternate)
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

 


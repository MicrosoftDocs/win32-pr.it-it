---
title: Classe MDM_Policy_Result01_DeviceLock02
description: La \_ \_ classe Result01 DeviceLock02 dei criteri MDM \_ rappresenta i criteri di blocco del dispositivo disponibili.
ms.assetid: 9aac25a8-8502-468f-9478-1ac4ccccaf0b
keywords:
- Classe MDM_Policy_Result01_DeviceLock02
- Classe MDM_Policy_Result01_DeviceLock02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_DeviceLock02
- MDM_Policy_Result01_DeviceLock02.InstanceID
- MDM_Policy_Result01_DeviceLock02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa93236b99add5cb49e0b54aa10eab9e959ab01a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873862"
---
# <a name="mdm_policy_result01_devicelock02-class"></a>\_ \_ Classe Result01 DeviceLock02 di criteri \_ MDM

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La **classe \_ \_ Result01 \_ DeviceLock02 dei criteri MDM** rappresenta i criteri di blocco del dispositivo disponibili.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_DeviceLock02
{
  string InstanceID;
  string ParentID;
  sint32 AllowScreenTimeoutWhileLockedUserConfig;
  sint32 AllowSimpleDevicePassword;
  sint32 AlphanumericDevicePasswordRequired;
  sint32 DevicePasswordEnabled;
  sint32 DevicePasswordExpiration;
  sint32 DevicePasswordHistory;
  string EnforceLockScreenAndLogonImage;
  string EnforceLockScreenProvider;
  sint32 MinimumPasswordAge;
  sint32 MaxDevicePasswordFailedAttempts;
  sint32 MaxInactivityTimeDeviceLock;
  sint32 MinDevicePasswordComplexCharacters;
  sint32 MinDevicePasswordLength;
  sint32 ScreenTimeoutWhileLocked;
  string PreventLockScreenSlideShow;
};
```

## <a name="members"></a>Members

La **classe \_ \_ Result01 \_ DeviceLock02 dei criteri MDM** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ \_ \_ DeviceLock02 dei criteri MDM Result01** ha queste proprietà.

<dl> <dt>

AllowScreenTimeoutWhileLockedUserConfig
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[AllowSimpleDevicePassword](/windows/client-management/mdm/policy-csp-devicelock#devicelock-allowsimpledevicepassword)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[AlphanumericDevicePasswordRequired](/windows/client-management/mdm/policy-csp-devicelock#devicelock-alphanumericdevicepasswordrequired)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[DevicePasswordEnabled](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordenabled)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[DevicePasswordExpiration](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordexpiration)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[DevicePasswordHistory](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordhistory)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[EnforceLockScreenAndLogonImage](/windows/client-management/mdm/policy-csp-devicelock#devicelock-enforcelockscreenandlogonimage)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

EnforceLockScreenProvider
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

Identifica il nome del nodo padre. Per questa classe la stringa è "DeviceLock".

</dd> <dt>

[MaxDevicePasswordFailedAttempts](/windows/client-management/mdm/policy-csp-devicelock#devicelock-maxdevicepasswordfailedattempts)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[MaxInactivityTimeDeviceLock](/windows/client-management/mdm/policy-csp-devicelock#devicelock-maxinactivitytimedevicelock)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[MinDevicePasswordComplexCharacters consente](/windows/client-management/mdm/policy-csp-devicelock#devicelock-mindevicepasswordcomplexcharacters)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[MinDevicePasswordLength](/windows/client-management/mdm/policy-csp-devicelock#devicelock-mindevicepasswordlength)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[MinimumPasswordAge](/windows/client-management/mdm/policy-csp-devicelock#devicelock-minimumpasswordage)
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

[PreventLockScreenSlideShow](/windows/client-management/mdm/policy-csp-devicelock#devicelock-preventlockscreenslideshow)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

ScreenTimeoutWhileLocked
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
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

 


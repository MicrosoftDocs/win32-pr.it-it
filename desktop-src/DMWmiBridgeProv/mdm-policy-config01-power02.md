---
title: Classe MDM_Policy_Config01_Power02
description: La \_ \_ classe Config01 Power02 dei criteri MDM \_ Configura i criteri di risparmio energia.
ms.assetid: 8913c38c-0d8d-456f-a412-d47c2ccd5d13
keywords:
- Classe MDM_Policy_Config01_Power02
- Classe MDM_Policy_Config01_Power02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Power02
- MDM_Policy_Config01_Power02.InstanceID
- MDM_Policy_Config01_Power02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c9bdda57bbd85100e8bccb87990d928f448a972
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119722"
---
# <a name="mdm_policy_config01_power02-class"></a>\_ \_ Classe Config01 Power02 di criteri \_ MDM

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La \_ \_ classe Config01 Power02 dei criteri MDM \_ Configura i criteri di risparmio energia.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Power02
{
  string InstanceID;
  string ParentID;
  string AllowStandbyWhenSleepingPluggedIn;
  string HibernateTimeoutPluggedIn;
  string HibernateTimeoutOnBattery;
  string DisplayOffTimeoutPluggedIn;
  string DisplayOffTimeoutOnBattery;
  string RequirePasswordWhenComputerWakesOnBattery;
  string RequirePasswordWhenComputerWakesPluggedIn;
  string StandbyTimeoutPluggedIn;
  string StandbyTimeoutOnBattery;
};
```

## <a name="members"></a>Members

La **classe \_ \_ Config01 \_ Power02 dei criteri MDM** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ \_ \_ Power02 dei criteri MDM Config01** ha queste proprietà.

<dl> <dt>

[AllowStandbyWhenSleepingPluggedIn](/windows/client-management/mdm/policy-csp-power#power-allowstandbywhensleepingpluggedin)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[DisplayOffTimeoutOnBattery](/windows/client-management/mdm/policy-csp-power#power-displayofftimeoutonbattery)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[DisplayOffTimeoutPluggedIn](/windows/client-management/mdm/policy-csp-power#power-displayofftimeoutpluggedin)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[HibernateTimeoutOnBattery](/windows/client-management/mdm/policy-csp-power#power-hibernatetimeoutonbattery)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[HibernateTimeoutPluggedIn](/windows/client-management/mdm/policy-csp-power#power-hibernatetimeoutpluggedin)
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

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

</dd> <dt>

[RequirePasswordWhenComputerWakesOnBattery](/windows/client-management/mdm/policy-csp-power#power-requirepasswordwhencomputerwakesonbattery)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[RequirePasswordWhenComputerWakesPluggedIn](/windows/client-management/mdm/policy-csp-power#power-requirepasswordwhencomputerwakespluggedin)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[StandbyTimeoutOnBattery](/windows/client-management/mdm/policy-csp-power#power-standbytimeoutonbattery)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[StandbyTimeoutPluggedIn](/windows/client-management/mdm/policy-csp-power#power-standbytimeoutpluggedin)
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
| Spazio dei nomi<br/>                | \\ \\ Dmmap MDM CIMV2 \\ radice<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 


---
title: Classe MDM_WindowsAdvancedThreatProtection_HealthState01
description: La \_ classe MDM WindowsAdvancedThreatProtection \_ HealthState01 viene usata per determinare lo stato di integrità degli endpoint di Windows Defender Advanced Threat Protection (WDATP).
ms.assetid: 8d630b95-9895-4cb8-99f2-8f869c4dfd18
keywords:
- Classe MDM_WindowsAdvancedThreatProtection_HealthState01
- Classe MDM_WindowsAdvancedThreatProtection_HealthState01, descritta
topic_type:
- apiref
api_name:
- MDM_WindowsAdvancedThreatProtection_HealthState01
- MDM_WindowsAdvancedThreatProtection_HealthState01.InstanceID
- MDM_WindowsAdvancedThreatProtection_HealthState01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5519b731cf54a633a659ec865e7a1f0e12deda75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964609"
---
# <a name="mdm_windowsadvancedthreatprotection_healthstate01-class"></a>\_Classe MDM WindowsAdvancedThreatProtection \_ HealthState01

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La classe **MDM \_ WindowsAdvancedThreatProtection \_ HealthState01** viene usata per determinare lo stato di integrità degli endpoint di Windows Defender Advanced Threat Protection (WDATP).

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_WindowsAdvancedThreatProtection_HealthState01
{
  string   InstanceID;
  string   ParentID;
  datetime LastConnected;
  boolean  SenseIsRunning;
  sint32   OnboardingState;
  string   OrgId;
};
```

## <a name="members"></a>Members

La classe **MDM \_ WindowsAdvancedThreatProtection \_ HealthState01** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **MDM \_ WindowsAdvancedThreatProtection \_ HealthState01** dispone di queste proprietà.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifica il nome del nodo padre. Per questa classe la stringa è "HealthState".

</dd> <dt>

[LastConnected](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#healthstate-lastconnected)
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[OnboardingState](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#healthstate-onboardingstate)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[OrgId](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#healthstate-orgid)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
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

Descrive il percorso completo del nodo padre. Per questa classe la stringa è "./Vendor/MSFT/WindowsAdvancedThreatProtection"

</dd> <dt>

[SenseIsRunning](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#healthstate-senseisrunning)
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                            |
| Spazio dei nomi<br/>                | \\ \\ Dmmap MDM CIMV2 \\ radice<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1. mof</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>\\DMWmiBridgeProv.dllfile MOF</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilizzo di script di PowerShell con il provider del Bridge WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 


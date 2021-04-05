---
title: Classe MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03
description: La \_ classe MDM AppLocker \_ ApplicationLaunchRestrictions01 \_ EXE03 consente di specificare quali applicazioni exe possono essere avviate.
ms.assetid: 27f10b5c-bc3b-4344-afcf-5718ea13e909
keywords:
- Classe MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03
- Classe MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03, descritta
topic_type:
- apiref
api_name:
- MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03
- MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03.InstanceID
- MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58aeb86edc21fec974c099fd8d25bd2e3fb244ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873649"
---
# <a name="mdm_applocker_applicationlaunchrestrictions01_exe03-class"></a>MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ classe EXE03

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La classe **MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ EXE03** consente di specificare quali applicazioni exe possono essere avviate.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03
{
  string InstanceID;
  string ParentID;
  string Policy;
  string EnforcementMode;
  string NonInteractiveProcessEnforcement;
};
```

## <a name="members"></a>Members

La classe **MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ EXE03** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ EXE03** dispone di queste proprietà.

<dl> <dt>

[**EnforcementMode**](/windows/client-management/mdm/applocker-csp)
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

Definisce le restrizioni per l'avvio di applicazioni eseguibili.

</dd> <dt>

[**NonInteractiveProcessEnforcement**](/windows/client-management/mdm/applocker-csp)
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

Descrive il percorso completo del nodo padre. Per questa classe la stringa è "*grouping*./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions/"

</dd> <dt>

[**Criteri**](/windows/client-management/mdm/applocker-csp)
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

 


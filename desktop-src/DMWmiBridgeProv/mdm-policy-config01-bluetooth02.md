---
title: Classe MDM_Policy_Config01_Bluetooth02
description: La \_ classe Bluetooth02 dei criteri MDM \_ Config01 \_ rappresenta i criteri di gestione Bluetooth disponibili.
ms.assetid: 8544c8df-a57b-4e21-87ee-f819aeddc071
keywords:
- Classe MDM_Policy_Config01_Bluetooth02
- Classe MDM_Policy_Config01_Bluetooth02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Bluetooth02
- MDM_Policy_Config01_Bluetooth02.InstanceID
- MDM_Policy_Config01_Bluetooth02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceeea1cd099fa00d6138a0ff1d37123725f0be2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119423"
---
# <a name="mdm_policy_config01_bluetooth02-class"></a>\_ \_ Classe Config01 Bluetooth02 di criteri \_ MDM

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La **classe \_ \_ \_ Bluetooth02 dei criteri MDM Config01** rappresenta i criteri di gestione Bluetooth disponibili.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Bluetooth02
{
  string InstanceID;
  string ParentID;
  sint32 AllowDiscoverableMode;
  string LocalDeviceName;
  sint32 AllowAdvertising;
  string ServicesAllowedList;
  sint32 AllowPrepairing;
};
```

## <a name="members"></a>Members

La **classe \_ \_ Config01 \_ Bluetooth02 dei criteri MDM** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ \_ \_ Bluetooth02 dei criteri MDM Config01** ha queste proprietà.

<dl> <dt>

[AllowAdvertising](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-allowadvertising)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[AllowDiscoverableMode](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-allowdiscoverablemode)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[AllowPrepairing](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-allowprepairing)
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

Identifica il nome del nodo padre. Per questa classe la stringa è "Bluetooth".

</dd> <dt>

[LocalDeviceName](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-localdevicename)
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

Descrive il percorso completo del nodo padre. Per questa classe la stringa è "./Vendor/MSFT/Policy/Config"

</dd> <dt>

[ServicesAllowedList](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-servicesallowedlist)
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

 


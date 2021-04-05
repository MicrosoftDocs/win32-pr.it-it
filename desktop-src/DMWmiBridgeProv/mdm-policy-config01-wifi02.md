---
title: Classe MDM_Policy_Config01_WiFi02
description: La \_ classe WiFi02 dei criteri MDM \_ Config01 \_ rappresenta i criteri di Wi-Fi disponibili.
ms.assetid: 68CFBB5E-F365-4D1A-8EF1-CC070E9A7982
keywords:
- Classe MDM_Policy_Config01_WiFi02
- Classe MDM_Policy_Config01_WiFi02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_WiFi02
- MDM_Policy_Config01_WiFi02.InstanceID
- MDM_Policy_Config01_WiFi02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00848613f1f0e9fd4ab6db9dc4afdabe54ce538c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873873"
---
# <a name="mdm_policy_config01_wifi02-class"></a>\_ \_ Classe Config01 WiFi02 di criteri \_ MDM

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La **classe \_ \_ \_ WiFi02 dei criteri MDM Config01** rappresenta i criteri di Wi-Fi disponibili. Questi criteri determinano Wi-Fi configurazioni consentite.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_WiFi02
{
  string InstanceID;
  string ParentID;
  sint32 AllowInternetSharing;
  sint32 AllowWiFi;
  sint32 AllowWiFiDirect;
  sint32 AllowManualWiFiConfiguration;
  sint32 AllowAutoConnectToWiFiSenseHotspots;
  sint32 WLANScanMode;
};
```

## <a name="members"></a>Members

La **classe \_ \_ Config01 \_ WiFi02 dei criteri MDM** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ \_ \_ WiFi02 dei criteri MDM Config01** ha queste proprietà.

<dl> <dt>

[AllowAutoConnectToWiFiSenseHotspots](/windows/client-management/mdm/policy-csp-wifi#wifi-allowautoconnecttowifisensehotspots)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[AllowInternetSharing](/windows/client-management/mdm/policy-csp-wifi#wifi-allowinternetsharing)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[AllowManualWiFiConfiguration](/windows/client-management/mdm/policy-csp-wifi#wifi-allowmanualwificonfiguration)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[AllowWiFi consente](/windows/client-management/mdm/policy-csp-wifi#wifi-allowwifi)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[AllowWiFiDirect](/windows/client-management/mdm/policy-csp-wifi#wifi-allowwifidirect)
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

Identifica il nome del nodo padre. Per questa classe la stringa è "WiFi".

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

[WLANScanMode](/windows/client-management/mdm/policy-csp-wifi#wifi-wlanscanmode)
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

 


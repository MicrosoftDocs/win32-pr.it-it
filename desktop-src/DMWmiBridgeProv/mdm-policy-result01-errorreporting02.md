---
title: Classe MDM_Policy_Result01_ErrorReporting02
description: La \_ classe ErrorReporting02 dei criteri MDM \_ Result01 \_ rappresenta i criteri di segnalazione degli errori.
ms.assetid: 8cc8c570-70d7-4dcb-a558-122604a14110
keywords:
- Classe MDM_Policy_Result01_ErrorReporting02
- Classe MDM_Policy_Result01_ErrorReporting02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_ErrorReporting02
- MDM_Policy_Result01_ErrorReporting02.InstanceID
- MDM_Policy_Result01_ErrorReporting02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1435e86f4e957a420a76c79f574939cb45df2a4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104225211"
---
# <a name="mdm_policy_result01_errorreporting02-class"></a>\_ \_ Classe Result01 ErrorReporting02 di criteri \_ MDM

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La \_ classe ErrorReporting02 dei criteri MDM \_ Result01 \_ rappresenta i criteri di segnalazione degli errori.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_ErrorReporting02
{
  string InstanceID;
  string ParentID;
  string CustomizeConsentSettings;
  string DisableWindowsErrorReporting;
  string DisplayErrorNotification;
  string DoNotSendAdditionalData;
  string PreventCriticalErrorDisplay;
};
```

## <a name="members"></a>Members

La **classe \_ \_ Result01 \_ ErrorReporting02 dei criteri MDM** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ \_ \_ ErrorReporting02 dei criteri MDM Result01** ha queste proprietà.

<dl> <dt>

[CustomizeConsentSettings](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-customizeconsentsettings)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[DisableWindowsErrorReporting](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-disablewindowserrorreporting)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[DisplayErrorNotification](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-displayerrornotification)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[DoNotSendAdditionalData](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-donotsendadditionaldata)
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

[PreventCriticalErrorDisplay](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-preventcriticalerrordisplay)
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



 


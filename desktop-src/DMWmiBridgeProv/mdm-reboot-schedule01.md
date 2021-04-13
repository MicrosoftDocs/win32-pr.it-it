---
title: Classe MDM_Reboot_Schedule01
description: Il \_ Schedule01class di riavvio MDM \_ viene usato per configurare un momento specifico per il riavvio di un dispositivo.
ms.assetid: d865609a-9f17-4256-9c69-4fea75011c1f
keywords:
- Classe MDM_Reboot_Schedule01
- Classe MDM_Reboot_Schedule01, descritta
topic_type:
- apiref
api_name:
- MDM_Reboot_Schedule01
- MDM_Reboot_Schedule01.InstanceID
- MDM_Reboot_Schedule01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7229aca469ee83d9ac2e4b29f6d6b7c54875120
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475292"
---
# <a name="mdm_reboot_schedule01-class"></a>\_Classe Schedule01 di riavvio MDM \_

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La **classe \_ \_ Schedule01 di riavvio MDM** viene usata per configurare un momento specifico per il riavvio di un dispositivo.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reboot_Schedule01
{
  string InstanceID;
  string ParentID;
  string Single;
  string DailyRecurrent;
};
```

## <a name="members"></a>Members

La **classe \_ \_ Schedule01 di riavvio MDM** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ \_ Schedule01 per il riavvio MDM** ha queste proprietà.

<dl> <dt>

[DailyRecurrent](/windows/client-management/mdm/reboot-csp#schedule-dailyrecurrent)
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

Identifica il nome del nodo padre. Per questa classe la stringa è "Schedule".

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Descrive il percorso completo del nodo padre. Per questa classe la stringa è "./Vendor/MSFT/Reboot"

</dd> <dt>

[Singolo](/windows/client-management/mdm/reboot-csp#schedule-single)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
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



 


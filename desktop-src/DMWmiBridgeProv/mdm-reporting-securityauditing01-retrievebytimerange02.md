---
title: Classe MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02
description: La \_ \_ \_ classe SecurityAuditing01 RETRIEVEBYTIMERANGE02 di Reporting MDM viene usata per recuperare i log presenti all'interno di StartTime e StopTime.
ms.assetid: e360bc76-f006-45e1-b78a-29125fbcd5ae
keywords:
- Classe MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02
- Classe MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02, descritta
topic_type:
- apiref
api_name:
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02.InstanceID
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abbbe47dfb3ff23c1d1bd891053375e19d6e503e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740063"
---
# <a name="mdm_reporting_securityauditing01_retrievebytimerange02-class"></a>MDM \_ Reporting \_ SecurityAuditing01 \_ classe RetrieveByTimeRange02

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La **classe \_ \_ SecurityAuditing01 \_ RetrieveByTimeRange02 di Reporting MDM** viene utilizzata per recuperare i log presenti all'interno di StartTime e StopTime. i StartTime e StopTime sono espressi in formato ISO 8601. Se i valori di StartTime e StopTime non sono specificati, i valori vengono interpretati come prima esistente o ultima ora esistente.

Ecco gli altri scenari possibili:

-   Se StartTime e StopTime non sono specificati, vengono restituiti tutti i log esistenti.
-   Se il StopTime è specificato, ma il StartTime non è specificato, vengono restituiti tutti i log esistenti prima di StopTime.
-   Se viene specificato StartTime, ma StopTime non è specificato, vengono restituiti tutti i log esistenti dall'oggetto StartTime.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02
{
  string InstanceID;
  string ParentID;
  string Logs;
  string StartTime;
  string StopTime;
};
```

## <a name="members"></a>Members

La **classe \_ \_ SecurityAuditing01 \_ RetrieveByTimeRange02 di Reporting MDM** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe RetrieveByTimeRange02 per la **\_ creazione di report MDM \_ \_ SecurityAuditing01** ha queste proprietà.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifica il nome del nodo padre. Per questa classe la stringa è "RetrieveByTimeRange".

</dd> <dt>

[Log](/windows/client-management/mdm/reporting-csp#logs)
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

Descrive il percorso completo del nodo padre. Per questa classe la stringa è "./Vendor/MSFT/SecurityAuditing"

</dd> <dt>

[StartTime](/windows/client-management/mdm/reporting-csp#starttime)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[StopTime](/windows/client-management/mdm/reporting-csp#stoptime)
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



 


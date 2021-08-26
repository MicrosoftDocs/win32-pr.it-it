---
title: MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02 classe
description: La classe MDM \_ Reporting \_ SecurityAuditing01 RetrieveByTimeRange02 viene usata per recuperare i log esistenti all'interno di \_ StartTime e StopTime.
ms.assetid: e360bc76-f006-45e1-b78a-29125fbcd5ae
keywords:
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02 classe
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02 classe , descritta
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
ms.openlocfilehash: c307f2b5ddcad1631cd5981a0ea25d8b9fb43566a482de20a2d050a0f3e8db57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913574"
---
# <a name="mdm_reporting_securityauditing01_retrievebytimerange02-class"></a>Mdm \_ Reporting \_ SecurityAuditing01 \_ RetrieveByTimeRange02 class

\[Alcune informazioni riguardano un prodotto pre-rilasciato che può essere modificato sostanzialmente prima del rilascio in commercio. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La classe **MDM \_ Reporting \_ SecurityAuditing01 \_ RetrieveByTimeRange02** viene usata per recuperare i log esistenti all'interno di StartTime e StopTime. StartTime e StopTime sono espressi in formato ISO 8601. Se startTime e StopTime non sono specificati, i valori vengono interpretati come la prima ora esistente o l'ultima ora esistente.

Ecco gli altri possibili scenari:

-   Se startTime e StopTime non sono specificati, vengono restituiti tutti i log esistenti.
-   Se si specifica StopTime, ma startTime non è specificato, vengono restituiti tutti i log esistenti prima di StopTime.
-   Se viene specificato StartTime, ma stopTime non è specificato, vengono restituiti tutti i log esistenti da StartTime.

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

La **classe MDM Reporting \_ \_ SecurityAuditing01 \_ RetrieveByTimeRange02** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe MDM Reporting \_ \_ SecurityAuditing01 \_ RetrieveByTimeRange02** ha queste proprietà.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifica il nome del nodo padre. Per questa classe, la stringa è "RetrieveByTimeRange".

</dd> <dt>

[Log](/windows/client-management/mdm/reporting-csp#logs)
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

**Parentid**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Descrive il percorso completo del nodo padre. Per questa classe, la stringa è "./Vendor/MSFT/SecurityAuditing"

</dd> <dt>

[StartTime](/windows/client-management/mdm/reporting-csp#starttime)
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

[StopTime](/windows/client-management/mdm/reporting-csp#stoptime)
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                            |
| Spazio dei nomi<br/>                | Dmmap \\ mdm cimv2 \\ \\ radice<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1.mof</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>File mofs \\DMWmiBridgeProv.dll</dt> </dl> |



 


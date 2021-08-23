---
title: MDM_Update_InstallableUpdates01_01 classe
description: La classe \_ InstallableUpdates01 01 dell'aggiornamento MDM viene usata per gestire e controllare \_ \_ l'implementazione degli aggiornamenti approvati.
ms.assetid: 53ca2291-a92a-46ed-948d-6d2a2dddd296
keywords:
- MDM_Update_InstallableUpdates01_01 classe
- MDM_Update_InstallableUpdates01_01 classe, descritta
topic_type:
- apiref
api_name:
- MDM_Update_InstallableUpdates01_01
- MDM_Update_InstallableUpdates01_01.InstanceID
- MDM_Update_InstallableUpdates01_01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a1e8989a261ef57025210ddf15ef265df436c1a5a94166c43db38d09068ff19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795871"
---
# <a name="mdm_update_installableupdates01_01-class"></a>Classe \_ \_ InstallableUpdates01 \_ 01 dell'aggiornamento MDM

\[Alcune informazioni riguardano prodotti pre-rilasciati che possono essere modificati in modo sostanziale prima che venga rilasciato commercialmente. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La **classe Mdm Update \_ \_ InstallableUpdates01 \_ 01** viene usata per gestire e controllare l'implementazione degli aggiornamenti approvati.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Update_InstallableUpdates01_01
{
  string InstanceID;
  string ParentID;
  sint32 Type;
  sint32 RevisionNumber;
};
```

## <a name="members"></a>Members

La **classe MDM Update \_ \_ InstallableUpdates01 \_ 01** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Mdm Update \_ \_ InstallableUpdates01 \_ 01** ha queste proprietà.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifica il nome del nodo padre. Per questa classe, la stringa è il GUID dell'aggiornamento approvato.

</dd> <dt>

**Parentid**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Descrive il percorso completo del nodo padre. Per questa classe, la stringa è "./Vendor/MSFT/Update/InstallableUpdates"

</dd> <dt>

[RevisionNumber](/windows/client-management/mdm/update-csp#failedupdates-failed-update-guid-revisionnumber)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

</dd> <dt>

[Tipo](/windows/client-management/mdm/update-csp#installableupdates-installable-update-guid-type)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                            |
| Spazio dei nomi<br/>                | Dmmap \\ mdm cimv2 \\ \\ radice<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1.mof</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>Mofs \\DMWmiBridgeProv.dll</dt> </dl> |



 


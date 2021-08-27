---
title: MDM_Update_PendingRebootUpdates01_01 classe
description: La classe MDM \_ Update \_ PendingRebootUpdates01 01 viene usata per gestire gli aggiornamenti \_ in sospeso al riavvio.
ms.assetid: 752cdaaa-7883-43d4-be7d-7da9ad15d041
keywords:
- MDM_Update_PendingRebootUpdates01_01 classe
- MDM_Update_PendingRebootUpdates01_01 classe, descritta
topic_type:
- apiref
api_name:
- MDM_Update_PendingRebootUpdates01_01
- MDM_Update_PendingRebootUpdates01_01.InstanceID
- MDM_Update_PendingRebootUpdates01_01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86a1cc421f4bd423137ff5699ebaf2412952e5f0f741952f91be15738b19b7ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109261"
---
# <a name="mdm_update_pendingrebootupdates01_01-class"></a>Classe Mdm \_ Update \_ PendingRebootUpdates01 \_ 01

\[Alcune informazioni riguardano prodotti pre-rilasciati che possono essere modificati in modo sostanziale prima che venga rilasciato commercialmente. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La **classe MDM Update \_ \_ PendingRebootUpdates01 \_ 01** viene usata per gestire gli aggiornamenti in sospeso al riavvio.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Update_PendingRebootUpdates01_01
{
  string   InstanceID;
  string   ParentID;
  datetime InstalledTime;
};
```

## <a name="members"></a>Members

La **classe MDM Update \_ \_ PendingRebootUpdates01 \_ 01** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe MDM Update \_ \_ PendingRebootUpdates01 \_ 01** ha queste proprietà.

<dl> <dt>

[InstalledTime](/windows/client-management/mdm/update-csp#pendingrebootupdates-pending-reboot-update-guid-installedtime)
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifica il nome del nodo padre. Per questa classe, la stringa è il GUID dell'aggiornamento in sospeso.

</dd> <dt>

**Parentid**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Descrive il percorso completo del nodo padre. Per questa classe, la stringa è "./Vendor/MSFT/Update/PendingRebootUpdates"

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                            |
| Spazio dei nomi<br/>                | Dmmap \\ mdm cimv2 \\ \\ radice<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1.mof</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>Mofs \\DMWmiBridgeProv.dll</dt> </dl> |



 


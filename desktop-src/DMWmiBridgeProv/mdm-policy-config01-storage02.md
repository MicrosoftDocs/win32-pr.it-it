---
title: MDM_Policy_Config01_Storage02 classe
description: La classe MDM \_ Policy \_ Config01 \_ Storage02 configura i criteri di archiviazione.
ms.assetid: 5c58e6d4-dfc6-4467-9a86-08eb31ccf28d
keywords:
- MDM_Policy_Config01_Storage02 classe
- MDM_Policy_Config01_Storage02 classe, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Storage02
- MDM_Policy_Config01_Storage02.InstanceID
- MDM_Policy_Config01_Storage02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 252824118d447af5faea6164de213ca162e3abfd389b96129958c2a03f3eb3cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588071"
---
# <a name="mdm_policy_config01_storage02-class"></a>Classe \_ Mdm Policy \_ Config01 \_ Storage02

\[Alcune informazioni riguardano prodotti pre-rilasciati che possono essere modificati in modo sostanziale prima che venga rilasciato commercialmente. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La classe MDM \_ Policy \_ Config01 \_ Storage02 configura i criteri di archiviazione.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Storage02
{
  string InstanceID;
  string ParentID;
  sint32 AllowDiskHealthModelUpdates;
  string EnhancedStorageDevices;
};
```

## <a name="members"></a>Members

La **classe MDM Policy \_ \_ Config01 \_ Storage02** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe MDM Policy \_ \_ Config01 \_ Storage02** ha queste proprietà.

<dl> <dt>

[AllowDiskHealthModelUpdates](/windows/client-management/mdm/policy-csp-storage#storage-allowdiskhealthmodelupdates)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

</dd> <dt>

[EnhancedStorageDevices](/windows/client-management/mdm/policy-csp-storage#storage-enhancedstoragedevices)
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
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

</dd> <dt>

**Parentid**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                      |
| Spazio dei nomi<br/>                | Dmmap \\ mdm cimv2 \\ \\ radice<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 


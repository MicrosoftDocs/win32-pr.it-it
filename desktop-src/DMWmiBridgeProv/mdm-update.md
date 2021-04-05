---
title: Classe MDM_Update
description: La \_ classe di aggiornamento MDM viene utilizzata per gestire e controllare l'implementazione di nuovi aggiornamenti.
ms.assetid: 503884fd-190c-482d-b600-1a15363891f3
keywords:
- Classe MDM_Update
- Classe MDM_Update, descritta
topic_type:
- apiref
api_name:
- MDM_Update
- MDM_Update.InstanceID
- MDM_Update.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2735b5eaaef4abc468586cb7608be7969a1eab3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873641"
---
# <a name="mdm_update-class"></a>\_Classe di aggiornamento MDM

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La classe di **\_ aggiornamento MDM** viene utilizzata per gestire e controllare l'implementazione di nuovi aggiornamenti.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Update
{
  string   InstanceID;
  string   ParentID;
  datetime LastSuccessfulScanTime;
  sint32   DeferUpgrade;
};
```

## <a name="members"></a>Members

La classe di **\_ aggiornamento MDM** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe di **\_ aggiornamento MDM** presenta queste proprietà.

<dl> <dt>

[DeferUpgrade](/windows/client-management/mdm/update-csp#deferupgrade)
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

Identifica il nome del nodo padre. Per questa classe la stringa è "Update".

</dd> <dt>

[LastSuccessfulScanTime](/windows/client-management/mdm/update-csp#lastsuccessfulscantime)
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
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

Descrive il percorso completo del nodo padre. Per questa classe la stringa è "./Vendor/MSFT/"

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                            |
| Spazio dei nomi<br/>                | \\ \\ Dmmap MDM CIMV2 \\ radice<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1. mof</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>\\DMWmiBridgeProv.dllfile MOF</dt> </dl> |



 


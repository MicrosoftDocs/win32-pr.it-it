---
title: MDM_Update classe
description: La classe \_ Update MDM viene usata per gestire e controllare l'implementazione di nuovi aggiornamenti.
ms.assetid: 503884fd-190c-482d-b600-1a15363891f3
keywords:
- MDM_Update classe
- MDM_Update classe, descritta
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
ms.openlocfilehash: c8c3b2c03d9ffcea84b21c1d135388141c26b24bbe2fdcc6973ae33fa74d71fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077035"
---
# <a name="mdm_update-class"></a>Classe \_ Di aggiornamento MDM

\[Alcune informazioni riguardano prodotti pre-rilasciati che possono essere modificati in modo sostanziale prima che venga rilasciato commercialmente. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La **classe \_ Update MDM** viene usata per gestire e controllare l'implementazione di nuovi aggiornamenti.

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

La **classe \_ Mdm Update** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ Mdm Update** ha queste proprietà.

<dl> <dt>

[DeferUpgrade](/windows/client-management/mdm/update-csp#deferupgrade)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
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

Identifica il nome del nodo padre. Per questa classe, la stringa è "Update".

</dd> <dt>

[LastSuccessfulScanTime](/windows/client-management/mdm/update-csp#lastsuccessfulscantime)
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
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

Descrive il percorso completo del nodo padre. Per questa classe, la stringa è "./Vendor/MSFT/"

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                            |
| Spazio dei nomi<br/>                | Dmmap \\ mdm cimv2 \\ \\ radice<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1.mof</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>Mofs \\DMWmiBridgeProv.dll</dt> </dl> |



 


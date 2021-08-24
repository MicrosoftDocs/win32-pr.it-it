---
title: MDM_EnterpriseDataProtection classe
description: La classe MDM EnterpriseDataProtection viene usata per determinare lo stato corrente delle impostazioni specifiche di \_ Windows Information Protection (WIP) (in precedenza Enterprise Data Protection).
ms.assetid: 2b97de12-76d1-4b74-a979-f0484807b840
keywords:
- MDM_EnterpriseDataProtection classe
- MDM_EnterpriseDataProtection classe , descritta
topic_type:
- apiref
api_name:
- MDM_EnterpriseDataProtection
- MDM_EnterpriseDataProtection.InstanceID
- MDM_EnterpriseDataProtection.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c9ab641873f95f3b7d7b60772dd10ed0a38c12f57497304478a4c469ee1c645
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694881"
---
# <a name="mdm_enterprisedataprotection-class"></a>Classe \_ MDM EnterpriseDataProtection

\[Alcune informazioni riguardano un prodotto pre-rilasciato che può essere modificato sostanzialmente prima del rilascio in commercio. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La **classe \_ MDM EnterpriseDataProtection** viene usata per determinare lo stato corrente delle impostazioni specifiche di Windows Information Protection (WIP) (in precedenza Enterprise Data Protection).

Per altre informazioni su WIP, vedere Proteggere i dati aziendali usando la protezione dei dati [aziendali ( EDP).](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip)

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_EnterpriseDataProtection
{
  string InstanceID;
  string ParentID;
  sint32 Status;
};
```

## <a name="members"></a>Members

La **classe \_ MDM EnterpriseDataProtection** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe MDM \_ EnterpriseDataProtection** ha queste proprietà.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifica il nome del nodo padre. Per questa classe, la stringa è "EnterpriseDataProtection".

</dd> <dt>

**Parentid**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Descrive il percorso completo del nodo padre. Per questa classe, la stringa è "./Vendor/MSFT/"

</dd> <dt>

[Status](/windows/client-management/mdm/enterprisedataprotection-csp#status)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
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



 


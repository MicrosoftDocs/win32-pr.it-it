---
title: MSAD_NamingContext classe
description: Rappresenta un particolare contesto dei nomi (NC) nel controller di dominio.
ms.assetid: 67dd6c68-6c67-40b4-a20a-c6c312d23441
ms.tgt_platform: multiple
keywords:
- MSAD_NamingContext classe Active Directory
- MSAD_NamingContext classe Active Directory , descritto
topic_type:
- apiref
api_name:
- MSAD_NamingContext
- MSAD_NamingContext.DistinguishedName
- MSAD_NamingContext.IsFullReplica
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 571f13642116be0e846fe1350cd932d52087d9f0422b8f40d695e4fef99df5cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025779"
---
# <a name="msad_namingcontext-class"></a>Classe \_ NamingContext di MSAD

Rappresenta un particolare contesto dei nomi (NC) nel controller di dominio.

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_NamingContext
{
  String  DistinguishedName;
  boolean IsFullReplica = FALSE;
};
```

## <a name="members"></a>Members

La **classe \_ NAMINGContext di MSAD** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ NAMINGContext di MSAD** ha queste proprietà.

<dl> <dt>

**Distinguishedname**
</dt> <dd> <dl> <dt>

Tipo di dati: **Stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ottiene il percorso X.500 del NC.

</dd> <dt>

**IsFullReplica**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ottiene il valore che indica se il NC è di lettura/scrittura. **TRUE** se il NC è di lettura/scrittura; **FALSE** se il NC è di sola lettura.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ MicrosoftActiveDirectory<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



 


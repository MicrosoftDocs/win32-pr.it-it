---
description: Controlla l'accesso remoto alle versioni non supportate di Windows.
ms.assetid: eb326bba-a011-4b9c-b4ee-fc08ae364f6f
ms.tgt_platform: multiple
title: Classe __NTLMUser9X
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NTLMUser9X
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 79aa5153869c7337b6849e8c465dbbf8b36a0f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317582"
---
# <a name="__ntlmuser9x-class"></a>\_\_Classe NTLMUser9X

La classe di sistema **\_ \_ NTLMUser9X** controlla l'accesso remoto alle versioni non supportate di Windows. La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class __NTLMUser9X : __SecurityRelatedClass
{
  string Authority;
  sint32 Flags;
  sint32 Mask;
  string Name;
  sint32 Type;
};
```

## <a name="members"></a>Members

La classe **\_ \_ NTLMUser9X** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **\_ \_ NTLMUser9X** dispone di queste proprietà.

<dl> <dt>

**Authority**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Dominio a cui si applica un nome utente.

</dd> <dt>

**Flag**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Flag di ereditarietà.

<dt>

0
</dt> <dd>

Nessuna ereditarietà.

</dd> <dt>

2
</dt> <dd>

Si applicano agli spazi dei nomi figlio, oltre a quello corrente.

</dd> </dl>

</dd> <dt>

**Mask**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Maschera di maschera che specifica i diritti di accesso allo spazio dei nomi nel repository di Strumentazione gestione Windows (WMI). Per i valori di bit, vedere [**costanti di diritti di accesso allo spazio dei nomi**](namespace-access-rights-constants.md).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Nome utente.

</dd> <dt>

**Tipo**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Accesso consentito.

<dt>

0
</dt> <dd>

Accesso consentito.

</dd> <dt>

2
</dt> <dd>

Accesso negato.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **\_ \_ NTLMUser9X** viene usata come parametro di input per i metodi [**\_ \_ SystemSecurity:: Get9XUserList**](--systemsecurity-get9xuserlist.md) e [**\_ \_ SystemSecurity:: Set9XUserList**](--systemsecurity-set9xuserlist.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |
| Spazio dei nomi<br/>                | Tutti gli spazi dei nomi WMI<br/>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_\_SecurityRelatedClass**](/windows/desktop/WmiSdk/--securityrelatedclass)
</dt> <dt>

[Classi di sistema WMI](wmi-system-classes.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> </dl>

 


---
description: La \_ \_ classe di sistema astratta trustee rappresenta un trustee. È possibile utilizzare un nome o un SID (matrice di byte).
ms.assetid: 92d17c7c-ebca-4dd0-80d8-6edd999ca394
ms.tgt_platform: multiple
title: Classe __Trustee
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Trustee
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 5c6ba04760e924ffe9d86916cffdb82ea2488219
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530367"
---
# <a name="__trustee-class"></a>\_\_Classe Trustee

La classe di sistema astratta [**\_ \_ trustee**](--securitydescriptor.md) rappresenta un [*trustee*](/windows/desktop/SecGloss/t-gly). È possibile utilizzare un nome o un SID (matrice di byte).

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class __Trustee
{
  string Domain;
  string Name;
  uint8  SID[];
  uint32 SidLength;
  string SidString;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Members

La classe **\_ \_ trustee** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **\_ \_ trustee** dispone di queste proprietà.

<dl> <dt>

**Dominio**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Parte di dominio dell'account.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Parte relativa al nome dell'account.

</dd> <dt>

**SID**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Uint8**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

SID del trustee nel formato della matrice di byte binari.

</dd> <dt>

**SidLength**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Lunghezza in byte del SID.

</dd> <dt>

**SidString**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

SID del trustee nel formato stringa, ad esempio "S-1-1-0".

</dd> <dt>

**ORA di \_ creazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ora nel formato [CIM \_ DateTime](cim-datetime.md) quando è stato creato il descrittore di sicurezza.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa classe fornisce le proprietà ereditate dalla classe [**\_ trustee Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) , che è un membro della classe [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) . Per ulteriori informazioni, vedere [oggetti del descrittore di sicurezza WMI](wmi-security-descriptor-objects.md) e [modifica della sicurezza di accesso per gli oggetti a protezione diretta](changing-access-security-on-securable-objects.md). Per ulteriori informazioni sulle voci ACE, vedere [Access Control Components](/windows/desktop/SecAuthZ/access-control-components).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |
| Spazio dei nomi<br/>                | Tutti gli spazi dei nomi WMI<br/>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi di sistema WMI](wmi-system-classes.md)
</dt> <dt>

[**\_Trustee Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)
</dt> <dt>

[Gestione della sicurezza WMI](maintaining-wmi-security.md)
</dt> </dl>

 


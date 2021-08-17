---
description: La \_ \_ classe di sistema astratta Trustee rappresenta un trustee. È possibile usare un nome o un SID (matrice di byte).
ms.assetid: 92d17c7c-ebca-4dd0-80d8-6edd999ca394
ms.tgt_platform: multiple
title: __Trustee classe
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
ms.openlocfilehash: ac1e80bceb3dc584a22e342780bbf32660276868e473ff33ff01d6c2ad65d504
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131954"
---
# <a name="__trustee-class"></a>\_\_Classe Trustee

La classe di sistema astratta [**\_ \_ Trustee**](--securitydescriptor.md) rappresenta un [*trustee.*](/windows/desktop/SecGloss/t-gly) È possibile usare un nome o un SID (matrice di byte).

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

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

La **\_ \_ classe Trustee** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **\_ \_ classe Trustee** dispone di queste proprietà.

<dl> <dt>

**Dominio**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Parte di dominio dell'account.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Parte relativa al nome dell'account.

</dd> <dt>

**SID**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint8**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

SID del fiduciario nel formato di matrice di byte binario.

</dd> <dt>

**SidLength**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Lunghezza del SID in byte.

</dd> <dt>

**SidString**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

SID del trustee nel formato stringa, ad esempio "S-1-1-0".

</dd> <dt>

**ORA \_ DI CREAZIONE**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ora nel [formato CIM \_ DATETIME](cim-datetime.md) in cui è stato creato il descrittore di sicurezza.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa classe fornisce proprietà ereditate dalla [**classe \_ Trustee Win32,**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) che è un membro della [**classe \_ SecurityDescriptor Win32.**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) Per altre informazioni, vedere [Oggetti descrittore di sicurezza WMI](wmi-security-descriptor-objects.md) e Modifica della sicurezza degli [accessi per gli oggetti a protezione diretta.](changing-access-security-on-securable-objects.md) Per altre informazioni sulle voci ACE, vedere [Componenti di controllo di accesso.](/windows/desktop/SecAuthZ/access-control-components)

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

[**Win32 \_ Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)
</dt> <dt>

[Gestione della sicurezza WMI](maintaining-wmi-security.md)
</dt> </dl>

 


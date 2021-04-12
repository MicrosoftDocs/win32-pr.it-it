---
description: Rappresenta un descrittore di sicurezza.
ms.assetid: 1ade1751-52a2-4ada-8255-323321111663
ms.tgt_platform: multiple
title: Classe __SecurityDescriptor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SecurityDescriptor
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
ms.openlocfilehash: 5f305387a29d1d1569addafd127f53c98246e1a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231826"
---
# <a name="__securitydescriptor-class"></a>\_\_Classe SecurityDescriptor

La classe di sistema astratta **\_ \_ securityDescriptor** rappresenta un [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly).

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class __SecurityDescriptor
{
  uint32 ControlFlags;
  __ACE  DACL[];
  __ACE  Group;
  __ACE  Owner;
  __ACE  SACL;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Members

La classe **\_ \_ securityDescriptor** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **\_ \_ securityDescriptor** dispone di queste proprietà.

<dl> <dt>

**ControlFlags**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Flag di bit che forniscono informazioni sul contenuto e sul formato del descrittore. Per una descrizione dei flag, vedere la proprietà **ControlFlags** nella classe [**\_ securityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .

</dd> <dt>

**DACL**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **[**\_ \_ ACE**](--ace.md)**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Matrice di voci [**\_ \_ ACE**](--ace.md) che specificano l'accesso all'oggetto.

</dd> <dt>

**Gruppo**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **\_ \_ ACE**](--ace.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

ACE che identifica il trustee che rappresenta il gruppo dell'oggetto.

</dd> <dt>

**Proprietario**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **\_ \_ ACE**](--ace.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

ACE che identifica il trustee che rappresenta il proprietario dell'oggetto.

</dd> <dt>

**SACL**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **\_ \_ ACE**](--ace.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di voci [**\_ \_ ACE**](--ace.md) che identifica gli utenti e i gruppi per i quali vengono raccolte le informazioni di controllo.

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

Questa classe fornisce le proprietà ereditate da [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor). Per ulteriori informazioni, vedere [oggetti del descrittore di sicurezza WMI](wmi-security-descriptor-objects.md) e [modifica della sicurezza di accesso per gli oggetti a protezione diretta](changing-access-security-on-securable-objects.md). Per ulteriori informazioni sulle voci ACE, vedere [Access Control Components](/windows/desktop/SecAuthZ/access-control-components).

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

[**\_SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[Gestione della sicurezza WMI](maintaining-wmi-security.md)
</dt> </dl>

 


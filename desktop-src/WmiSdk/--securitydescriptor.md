---
description: Rappresenta un descrittore di sicurezza.
ms.assetid: 1ade1751-52a2-4ada-8255-323321111663
ms.tgt_platform: multiple
title: __SecurityDescriptor classe
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
ms.openlocfilehash: c248a437651396811f71c04e72dd8b209c5d10823f49d03abbe7e9d9ee6b6867
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118110198"
---
# <a name="__securitydescriptor-class"></a>\_\_Classe SecurityDescriptor

La classe di sistema astratta **\_ \_ SecurityDescriptor** rappresenta un [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly).

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

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

La **\_ \_ classe SecurityDescriptor** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **\_ \_ classe SecurityDescriptor** ha queste proprietà.

<dl> <dt>

**Flag di controllo**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Flag di bit che forniscono informazioni sul contenuto e sul formato del descrittore. Per una descrizione dei flag, vedere la proprietà **ControlFlags** nella [**classe \_ SecurityDescriptor Win32.**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)

</dd> <dt>

**Dacl**
</dt> <dd> <dl> <dt>

Tipo di dati: **[**\_ \_ matrice ACE**](--ace.md)**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Matrice di voci [**\_ \_ ACE**](--ace.md) che specificano l'accesso all'oggetto .

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

**Sacl**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **\_ \_ ACE**](--ace.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di [**\_ \_ voci ACE**](--ace.md) che identifica gli utenti e i gruppi per cui vengono raccolte le informazioni di controllo.

</dd> <dt>

**ORA \_ DI CREAZIONE**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ora nel [formato CIM \_ DATETIME](cim-datetime.md) al momento della creazione del descrittore di sicurezza.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa classe fornisce le proprietà ereditate da [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor). Per altre informazioni, vedere [Oggetti descrittori di sicurezza WMI](wmi-security-descriptor-objects.md) e Modifica della sicurezza degli [accessi in oggetti a protezione diretta](changing-access-security-on-securable-objects.md). Per altre informazioni sulle ACE, vedere [Componenti di controllo di accesso](/windows/desktop/SecAuthZ/access-control-components).

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

[**Descrittore di sicurezza Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[Gestione della sicurezza WMI](maintaining-wmi-security.md)
</dt> </dl>

 


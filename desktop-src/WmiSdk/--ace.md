---
description: Rappresenta una voce di controllo di accesso (ACE, Access Control Entry).
ms.assetid: 47daffd0-b9db-4367-b0b8-654a2da30fed
ms.tgt_platform: multiple
title: Classe __ACE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ACE
- All
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
ms.openlocfilehash: ea2a765225145ce3d44e0aff89aeaca0a7563e0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485756"
---
# <a name="__ace-class"></a>\_\_ACE (classe)

La classe di sistema **\_ \_ ACE** abstract rappresenta una voce di controllo di accesso ([*ACE*](/windows/desktop/SecGloss/a-gly)).

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class  __ACE : __SecurityRelatedClass
{
            AceFlags;
            AccessMask;
            AceType;
            GuidInheritedObjectType;
            GuidObjectType;
  uint64    TIME_CREATED;
  __Trustee Trustee;
};
```

## <a name="members"></a>Members

La classe **\_ \_ ACE** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **\_ \_ ACE** dispone di queste proprietà.

<dl> <dt>

**AccessMask**
</dt> <dd> <dl> <dt>

Tipo di dati: 
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Flag di bit che rappresentano i diritti concessi o negati al trustee. Per ulteriori informazioni e una descrizione dei flag, vedere la proprietà **accessMask** nella classe [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) .

</dd> <dt>

**AceFlags**
</dt> <dd> <dl> <dt>

Tipo di dati: 
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Flag di bit che specificano l'ereditarietà della voce ACE. Per ulteriori informazioni e una descrizione dei flag, vedere la proprietà **AceFlags** nella classe [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) .

</dd> <dt>

**AceType**
</dt> <dd> <dl> <dt>

Tipo di dati: 
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Tipo di voce ACE rappresentata da questa istanza.

</dd> <dt>

**GuidInheritedObjectType**
</dt> <dd> <dl> <dt>

Tipo di dati: 
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

GUID dell'elemento padre dell'oggetto a cui si applicano i diritti di accesso nella proprietà **accessMask** .

</dd> <dt>

**GuidObjectType**
</dt> <dd> <dl> <dt>

Tipo di dati: 
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

GUID che indica il tipo di oggetto a cui si applicano i diritti nella proprietà **accessMask** .

</dd> <dt>

**ORA di \_ creazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ora, nel formato [ \_ DateTime CIM](cim-datetime.md) , in cui è stato creato il descrittore di sicurezza.

</dd> <dt>

**Fiduciario**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **\_ \_ trustee**](--trustee.md)**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Il trustee della voce ACE rappresentata da questa istanza della classe **\_ \_ ACE** .

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa classe fornisce le proprietà ereditate dalla classe [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) , che è un membro della classe [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) . Per ulteriori informazioni, vedere [oggetti del descrittore di sicurezza WMI](wmi-security-descriptor-objects.md) e [modifica della sicurezza di accesso per gli oggetti a protezione diretta](changing-access-security-on-securable-objects.md). Per ulteriori informazioni sulle voci ACE, vedere [Access Control Components](/windows/desktop/SecAuthZ/access-control-components).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |
| Spazio dei nomi<br/>                | Tutti gli spazi dei nomi WMI<br/>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_\_SecurityRelatedClass**](--securityrelatedclass.md)
</dt> <dt>

[Classi di sistema WMI](wmi-system-classes.md)
</dt> <dt>

[**\_ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[Gestione della sicurezza WMI](maintaining-wmi-security.md)
</dt> </dl>

 


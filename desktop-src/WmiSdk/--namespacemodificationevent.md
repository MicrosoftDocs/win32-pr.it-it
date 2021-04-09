---
description: Segnala un evento di modifica dello spazio dei nomi, ovvero un tipo di evento intrinseco che viene generato quando viene modificato uno spazio dei nomi.
ms.assetid: 168505d7-4677-4f41-935e-149f22de2cb5
ms.tgt_platform: multiple
title: Classe __NamespaceModificationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceModificationEvent
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 5af5783d3ebfbfb4b7842cb86b1919f8dbed1365
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759443"
---
# <a name="__namespacemodificationevent-class"></a>\_\_Classe NamespaceModificationEvent

La classe di sistema **\_ \_ NamespaceModificationEvent** segnala un evento di modifica dello spazio dei nomi, ovvero un tipo di [evento intrinseco](determining-the-type-of-event-to-receive.md) che viene generato quando viene modificato uno spazio dei nomi.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class __NamespaceModificationEvent : __NamespaceOperationEvent
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace PreviousNamespace;
  uint8       SECURITY_DESCRIPTOR [];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a>Members

La classe **\_ \_ NamespaceModificationEvent** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **\_ \_ NamespaceModificationEvent** dispone di queste proprietà.

<dl> <dt>

**PreviousNamespace**
</dt> <dd> <dl> <dt>

Tipo di dati: **\_ \_ namespace**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Copia della versione originale di un'istanza [**\_ \_ dello spazio dei nomi**](--namespace.md) . La proprietà **Name** di questa istanza identifica lo spazio dei nomi che viene modificato.

</dd> <dt>

**descrittore di sicurezza \_**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrittore utilizzato dal provider di eventi per determinare gli utenti che possono ricevere l'evento. Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).

</dd> <dt>

**descrittore di sicurezza \_** 
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrittore utilizzato dal provider di eventi per determinare gli utenti che possono ricevere un evento. Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).

> [!Note]  
> Un  elenco di controllo di accesso (ACL) null [**nel \_ descrittore di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) concede un accesso illimitato a tutti i tempi. Per ulteriori informazioni, vedere [creazione di un descrittore di sicurezza per un nuovo oggetto](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).

 

</dd> <dt>

**TargetNamespace**
</dt> <dd> <dl> <dt>

Tipo di dati: **\_ \_ namespace**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Copia dell'istanza [**\_ \_ dello spazio dei nomi**](--namespace.md) modificata. La proprietà **Name** dell'istanza **\_ \_ dello spazio dei nomi** indica lo spazio dei nomi modificato. Questa proprietà viene ereditata dalla classe [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md).

</dd> <dt>

**ORA di \_ creazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore univoco che indica l'ora in cui viene generato un evento. Si tratta di un valore a 64 bit che rappresenta il numero di intervalli di 100-nanosecondi dopo il 1 ° gennaio 1601. Le informazioni sono nel formato UTC (Coordinated Universal Time). Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **\_ \_ NamespaceModificationEvent** deriva da [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md).

Le uniche differenze tra lo spazio dei nomi di destinazione e lo spazio dei nomi precedente sono i qualificatori e le proprietà eccetto [**Name**](--namespace.md).

Si noti che la proprietà [**Name**](--namespace.md) di un'istanza **\_ \_ dello spazio dei nomi** non può essere modificata perché gli spazi dei nomi non possono essere rinominati. Per modificare il nome di uno spazio dei nomi, l'istanza **\_ \_ dello spazio dei nomi** deve essere eliminata e ricreata con un nuovo nome. Gli eventi di modifica dello spazio dei nomi vengono pertanto generati quando si verifica una modifica a qualificatori e proprietà diverse dal **nome**. Un evento di modifica dello spazio dei nomi non viene generato quando si verifica un qualsiasi tipo di modifica nello spazio dei nomi. Un evento di modifica dello spazio dei nomi viene generato solo quando viene modificata un'istanza dello spazio dei nomi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |
| Spazio dei nomi<br/>                | Tutti gli spazi dei nomi WMI<br/>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_\_NamespaceOperationEvent**](/windows/desktop/WmiSdk/--namespaceoperationevent)
</dt> <dt>

[Classi di sistema WMI](wmi-system-classes.md)
</dt> </dl>

 


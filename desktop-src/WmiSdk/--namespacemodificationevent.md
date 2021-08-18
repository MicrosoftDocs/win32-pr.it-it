---
description: Segnala un evento di modifica dello spazio dei nomi, ovvero un tipo di evento intrinseco generato quando viene modificato uno spazio dei nomi.
ms.assetid: 168505d7-4677-4f41-935e-149f22de2cb5
ms.tgt_platform: multiple
title: __NamespaceModificationEvent classe
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
ms.openlocfilehash: 3243afe0a8cae34e83ad85e2d89a3becab8d07775ba3ec0c3283fd4ea8ed8bbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118557814"
---
# <a name="__namespacemodificationevent-class"></a>\_\_Classe NamespaceModificationEvent

La **\_ \_ classe di sistema NamespaceModificationEvent** segnala un evento [](determining-the-type-of-event-to-receive.md) di modifica dello spazio dei nomi, ovvero un tipo di evento intrinseco generato quando viene modificato uno spazio dei nomi.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

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

La **\_ \_ classe NamespaceModificationEvent** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **\_ \_ classe NamespaceModificationEvent** ha queste proprietà.

<dl> <dt>

**PreviousNamespace**
</dt> <dd> <dl> <dt>

Tipo di dati: **\_ \_ Spazio dei nomi**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Copia della versione originale di un'istanza dello [**\_ \_ spazio dei**](--namespace.md) nomi. La **proprietà Name** di questa istanza identifica lo spazio dei nomi modificato.

</dd> <dt>

**DESCRITTORE \_ DI SICUREZZA**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrittore utilizzato dal provider di eventi per determinare quali utenti possono ricevere l'evento. Questa proprietà viene ereditata [**\_ \_ dall'evento**](--event.md).

</dd> <dt>

**DESCRITTORE \_ DI SICUREZZA** 
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrittore utilizzato dal provider di eventi per determinare gli utenti che possono ricevere un evento. Questa proprietà viene ereditata [**\_ \_ dall'evento**](--event.md).

> [!Note]  
> Un **elenco di** controllo di accesso (ACL) NULL in SECURITY [**\_ DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) concede sempre l'accesso illimitato a tutti gli utenti. Per altre informazioni, vedere [Creazione di un descrittore di sicurezza per un nuovo oggetto](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).

 

</dd> <dt>

**Targetnamespace**
</dt> <dd> <dl> <dt>

Tipo di dati: **\_ \_ Spazio dei nomi**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Copia [**\_ \_ dell'istanza dello**](--namespace.md) spazio dei nomi modificata. La **proprietà Name** dell'istanza **\_ \_ namespace** indica lo spazio dei nomi modificato. Questa proprietà viene ereditata dalla classe [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md).

</dd> <dt>

**ORA \_ DI CREAZIONE**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore univoco che indica l'ora in cui viene generato un evento. Si tratta di un valore a 64 bit che rappresenta il numero di intervalli di 100 nanosecondi dopo il 1° gennaio 1601. Le informazioni sono nel formato Coordinated Universal Time (UTC). Questa proprietà viene ereditata [**\_ \_ dall'evento**](--event.md).

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> </dl>

## <a name="remarks"></a>Commenti

La **\_ \_ classe NamespaceModificationEvent** è derivata da [**\_ \_ NamespaceOperationEvent.**](--namespaceoperationevent.md)

Le uniche differenze tra lo spazio dei nomi di destinazione e lo spazio dei nomi precedente sono i qualificatori e le proprietà ad eccezione [**di Name**](--namespace.md).

Si noti che la [**proprietà Name**](--namespace.md) di **\_ \_ un'istanza namespace** non può essere cambiata perché gli spazi dei nomi non possono essere rinominati. Per modificare il nome di uno spazio dei nomi, l'istanza **\_ \_ dello** spazio dei nomi deve essere eliminata e ri-creata con un nuovo nome. Di conseguenza, gli eventi di modifica dello spazio dei nomi vengono generati quando si verifica una modifica a qualificatori e proprietà diversi da **Name**. Un evento di modifica dello spazio dei nomi non viene generato quando si verifica qualsiasi tipo di modifica all'interno dello spazio dei nomi. Un evento di modifica dello spazio dei nomi viene generato solo quando viene modificata un'istanza dello spazio dei nomi.

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

 


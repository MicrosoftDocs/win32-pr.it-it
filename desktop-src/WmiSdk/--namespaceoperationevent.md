---
description: Classe di base per tutti gli eventi intrinseci correlati a uno spazio dei nomi.
ms.assetid: 168637b1-217e-4b6d-bd07-25127b9e9f6c
ms.tgt_platform: multiple
title: Classe __NamespaceOperationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceOperationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: d263af0eab5fc3899b45659bc8409a5e68776fe4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317584"
---
# <a name="__namespaceoperationevent-class"></a>\_\_Classe NamespaceOperationEvent

La classe di sistema **\_ \_ NamespaceOperationEvent** è una classe di base per tutti gli eventi intrinseci correlati a uno spazio dei nomi.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class __NamespaceOperationEvent : __Event
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a>Members

La classe **\_ \_ NamespaceOperationEvent** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **\_ \_ NamespaceOperationEvent** dispone di queste proprietà.

<dl> <dt>

**descrittore di sicurezza \_**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrittore utilizzato dal provider di eventi per determinare gli utenti che possono ricevere l'evento. Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).

</dd> <dt>

**TargetNamespace**
</dt> <dd> <dl> <dt>

Tipo di dati: **\_ \_ namespace**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Spazio dei nomi interessato dall'evento. Per gli eventi di creazione, si tratta dello spazio dei nomi appena creato. Per gli eventi di modifica, si tratta dello spazio dei nomi modificato. Per gli eventi di eliminazione, si tratta dello spazio dei nomi eliminato.

</dd> <dt>

**ORA di \_ creazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore univoco che indica l'ora in cui è stato generato l'evento. Si tratta di un valore a 64 bit che rappresenta il numero di intervalli di 100-nanosecondi dopo il 1 ° gennaio 1601. Le informazioni sono nel formato UTC (Coordinated Universal Time). Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **\_ \_ NamespaceOperationEvent** è derivata dall' [**\_ \_ evento**](--event.md).

Le istanze di questa classe non vengono create. WMI crea istanze di una delle classi seguenti derivate da questa classe:

[**\_\_NamespaceCreationEvent**](--namespacecreationevent.md)

[**\_\_NamespaceModificationEvent**](--namespacemodificationevent.md)

[**\_\_NamespaceDeletionEvent**](--namespacedeletionevent.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |
| Spazio dei nomi<br/>                | Tutti gli spazi dei nomi WMI<br/>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_\_Evento**](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[Classi di sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Determinazione del tipo di evento da ricevere](determining-the-type-of-event-to-receive.md)
</dt> </dl>

 


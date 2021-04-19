---
description: Segnala un evento di eliminazione dello spazio dei nomi, ovvero un tipo di evento intrinseco generato quando uno spazio dei nomi secondario viene rimosso dallo spazio dei nomi corrente.
ms.assetid: f7160a90-562d-40d9-9189-32aaabcd81d0
ms.tgt_platform: multiple
title: Classe __NamespaceDeletionEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceDeletionEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 6e23f909718167760c02bbdb38e2a075d04bc516
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317588"
---
# <a name="__namespacedeletionevent-class"></a>\_\_Classe NamespaceDeletionEvent

La classe di sistema **\_ \_ NamespaceDeletionEvent** segnala un evento di eliminazione dello spazio dei nomi, ovvero un tipo di [evento intrinseco](determining-the-type-of-event-to-receive.md) generato quando uno spazio dei nomi secondario viene rimosso dallo spazio dei nomi corrente.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class __NamespaceDeletionEvent : __NamespaceOperationEvent
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a>Members

La classe **\_ \_ NamespaceDeletionEvent** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **\_ \_ NamespaceDeletionEvent** dispone di queste proprietà.

<dl> <dt>

**descrittore di sicurezza \_**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrittore utilizzato dal provider di eventi per determinare gli utenti che possono ricevere un evento. Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).

</dd> <dt>

**TargetNamespace**
</dt> <dd> <dl> <dt>

Tipo di dati: **\_ \_ namespace**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Copia dell'istanza [**\_ \_ dello spazio dei nomi**](--namespace.md) eliminata. La proprietà **Name** dell'istanza **\_ \_ dello spazio dei nomi** identifica lo spazio dei nomi che viene eliminato. Questa proprietà viene ereditata da [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md).

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

La classe **\_ \_ NamespaceDeletionEvent** deriva da [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md).

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

 


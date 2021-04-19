---
description: Segnala quando un evento viene eliminato in seguito all'overflow della coda di recapito.
ms.assetid: 7cb1ef3b-3b0a-4f72-96de-862022fd6db8
ms.tgt_platform: multiple
title: Classe __EventQueueOverflowEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventQueueOverflowEvent
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 058b03b8a3311aad805f47a04d20e9f1fa8c2477
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317600"
---
# <a name="__eventqueueoverflowevent-class"></a>\_\_Classe EventQueueOverflowEvent

La classe di sistema **\_ \_ EventQueueOverflowEvent** segnala quando viene eliminato un evento in seguito all'overflow della coda di recapito.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class __EventQueueOverflowEvent : __EventDroppedEvent
{
  uint32              CurrentQueueSize;
  object              Event;
  __EventConsumer REF IntendedConsumer;
  uint8               SECURITY_DESCRIPTOR[];
  uint64              TIME_CREATED;
};
```

## <a name="members"></a>Members

La classe **\_ \_ EventQueueOverflowEvent** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **\_ \_ EventQueueOverflowEvent** dispone di queste proprietà.

<dl> <dt>

**CurrentQueueSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dimensioni correnti della coda, in byte. Per impostazione predefinita, questa proprietà è 10 MB per tutte le code combinate.

</dd> <dt>

**Event**
</dt> <dd> <dl> <dt>

Tipo di dati: **Object**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Evento di interesse. Questa proprietà viene ereditata da [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).

</dd> <dt>

**IntendedConsumer**
</dt> <dd> <dl> <dt>

Tipo di dati: **\_ \_ EventConsumer**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento al consumer previsto. Questa proprietà viene ereditata da [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).

</dd> <dt>

**descrittore di sicurezza \_**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrittore utilizzato dal provider di eventi per determinare gli utenti che possono ricevere l'evento. Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).

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

Solo gli utenti con privilegi di amministratore possono ricevere questo evento. La classe **\_ \_ EventQueueOverflowEvent** deriva da [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).

Per ulteriori informazioni, vedere la proprietà [**MaximumQueueSize**](--eventconsumer.md) nella classe [**\_ \_ EventConsumer**](--eventconsumer.md) e la proprietà [**HighThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) nella classe **\_ WMISetting di Win32** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |
| Spazio dei nomi<br/>                | Tutti gli spazi dei nomi WMI<br/>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_\_EventDroppedEvent**](/windows/desktop/WmiSdk/--eventdroppedevent)
</dt> <dt>

[Classi di sistema WMI](wmi-system-classes.md)
</dt> </dl>

 


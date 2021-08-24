---
description: Rappresenta l'occorrenza di un evento eliminato. Un evento eliminato è un evento che non viene recapitato a un consumer di eventi.
ms.assetid: fae267a9-e0ec-43fa-a3c3-d50345775a1d
ms.tgt_platform: multiple
title: __EventDroppedEvent classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventDroppedEvent
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 695381a3471dcc744cae10622ee9e7935b2770941a770bd0e4e4e93e591a9220
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051089"
---
# <a name="__eventdroppedevent-class"></a>\_\_Classe EventDroppedEvent

La **\_ \_ classe di sistema EventDroppedEvent** rappresenta l'occorrenza di un evento eliminato. Un evento eliminato è un evento che non viene recapitato a un consumer di eventi.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class __EventDroppedEvent : __SystemEvent
{
  __Event             Event;
  __EventConsumer REF IntendedConsumer;
  uint8               SECURITY_DESCRIPTOR[];
  uint64              TIME_CREATED;
};
```

## <a name="members"></a>Members

La **\_ \_ classe EventDroppedEvent** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **\_ \_ classe EventDroppedEvent** ha queste proprietà.

<dl> <dt>

**Event**
</dt> <dd> <dl> <dt>

Tipo di dati: **\_ \_ Evento**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Evento eliminato.

</dd> <dt>

**IntendedConsumer**
</dt> <dd> <dl> <dt>

Tipo di dati: **\_ \_ EventConsumer**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento a un'istanza di [**\_ \_ EventConsumer**](--eventconsumer.md) che rappresenta il consumer permanente identificato per ricevere un evento. I diversi consumer permanenti che sottoscriveno un evento possono continuare a ricevere l'evento.

</dd> <dt>

**DESCRITTORE \_ DI SICUREZZA**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrittore utilizzato da un provider di eventi per determinare gli utenti che possono ricevere un evento. Questa proprietà viene ereditata [**\_ \_ dall'evento**](--event.md).

</dd> <dt>

**ORA \_ DI CREAZIONE**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore univoco che indica l'ora in cui viene generato un evento. Valore a 64 bit che rappresenta il numero di intervalli di 100 nanosecondi dopo il 1° gennaio 1601. Le informazioni sono nel formato Coordinated Universal Time (UTC). Questa proprietà viene ereditata [**\_ \_ dall'evento**](--event.md).

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Commenti

La **\_ \_ classe EventDroppedEvent** è derivata da [**\_ \_ SystemEvent**](--systemevent.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |
| Spazio dei nomi<br/>                | Tutti gli spazi dei nomi WMI<br/>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_\_SystemEvent**](/windows/desktop/WmiSdk/--systemevent)
</dt> <dt>

[Classi di sistema WMI](wmi-system-classes.md)
</dt> </dl>

 


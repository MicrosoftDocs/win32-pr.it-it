---
description: Segnala quando un evento viene eliminato a causa dell'overflow della coda di recapito.
ms.assetid: 7cb1ef3b-3b0a-4f72-96de-862022fd6db8
ms.tgt_platform: multiple
title: __EventQueueOverflowEvent classe
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
ms.openlocfilehash: 6fd31df9f84883c8b677ea4fef0431ed762b4cec2155cb3d600893a40e3e1d9f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612631"
---
# <a name="__eventqueueoverflowevent-class"></a>\_\_Classe EventQueueOverflowEvent

La **\_ \_ classe di sistema EventQueueOverflowEvent** segnala quando un evento viene eliminato a causa dell'overflow della coda di recapito.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

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

La **\_ \_ classe EventQueueOverflowEvent** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **\_ \_ classe EventQueueOverflowEvent** ha queste proprietà.

<dl> <dt>

**CurrentQueueSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dimensioni correnti della coda, in byte. Questa proprietà è impostata su 10 MB per tutte le code combinate.

</dd> <dt>

**Event**
</dt> <dd> <dl> <dt>

Tipo di dati: **object**
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

**DESCRITTORE \_ DI SICUREZZA**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrittore utilizzato dal provider di eventi per determinare quali utenti possono ricevere l'evento. Questa proprietà viene ereditata [**\_ \_ dall'evento**](--event.md).

</dd> <dt>

**ORA \_ DI CREAZIONE**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore univoco che indica l'ora in cui è stato generato l'evento. Valore a 64 bit che rappresenta il numero di intervalli di 100 nanosecondi dopo il 1° gennaio 1601. Le informazioni sono nel formato Coordinated Universal Time (UTC). Questa proprietà viene ereditata [**\_ \_ dall'evento**](--event.md).

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Commenti

Solo gli utenti con privilegi di amministratore possono ricevere questo evento. La **\_ \_ classe EventQueueOverflowEvent** è derivata da [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).

Per altre informazioni, vedere la [**proprietà MaximumQueueSize**](--eventconsumer.md) nella classe [**\_ \_ EventConsumer**](--eventconsumer.md) e [**la proprietà HighThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) nella **classe \_ WMISetting Win32.**

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

 


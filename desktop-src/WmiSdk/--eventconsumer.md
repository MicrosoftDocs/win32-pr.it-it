---
description: È una classe di base astratta utilizzata nella registrazione di un consumer di eventi permanenti.
ms.assetid: c1dc9a91-76f9-4527-ad69-0323a9aef28a
ms.tgt_platform: multiple
title: Classe __EventConsumer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventConsumer
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: b8478b76aebf293d562129d047330f33e52706b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968648"
---
# <a name="__eventconsumer-class"></a>\_\_Classe EventConsumer

La classe di sistema **\_ \_ EventConsumer** è una classe di base astratta utilizzata nella registrazione di un consumer di eventi permanenti. È possibile derivare una nuova classe di consumer di eventi da **\_ \_ EventConsumer**.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[abstract]
class __EventConsumer : __IndicationRelated
{
  uint8  CreatorSID[];
  string MachineName;
  uint32 MaximumQueueSize;
};
```

## <a name="members"></a>Members

La classe **\_ \_ EventConsumer** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **\_ \_ EventConsumer** dispone di queste proprietà.

<dl> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

ID di sicurezza (SID) che identifica in modo univoco l'utente che crea un filtro. WMI archivia il SID dell'utente che crea un'istanza di **\_ \_ EventConsumer** o il SID Administrator, a seconda del sistema operativo. Per ulteriori informazioni, vedere [associazione di un filtro eventi a un consumer logico](binding-an-event-filter-with-a-logical-consumer.md) e [monitoraggio e risposta agli eventi con](monitoring-and-responding-to-events-with-standard-consumers.md)consumer standard.

</dd> <dt>

**MachineName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del computer a cui Strumentazione gestione Windows (WMI) Invia gli eventi.

</dd> <dt>

**MaximumQueueSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero massimo di code per un consumer specifico, in byte.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **\_ \_ EventConsumer** deriva da [**\_ \_ IndicationRelated**](--indicationrelated.md), che non dispone di proprietà.

I consumer permanenti definiscono nuove classi consumer per descrivere un'azione da eseguire e i dati da elaborare quando i consumer ricevono notifiche degli eventi. I consumer permanenti hanno particolari problemi di sicurezza. Per ulteriori informazioni, vedere [protezione degli eventi WMI](securing-wmi-events.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |
| Spazio dei nomi<br/>                | Tutti gli spazi dei nomi WMI<br/>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_\_IndicationRelated**](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[Classi di sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Ricezione di eventi in qualsiasi momento](receiving-events-at-all-times.md)
</dt> <dt>

[Creazione di una nuova classe di consumer di eventi permanenti](creating-a-new-permanent-event-consumer-class.md)
</dt> <dt>

[Creazione di un consumer logico](creating-a-logical-consumer.md)
</dt> <dt>

[Protezione degli eventi WMI](securing-wmi-events.md)
</dt> </dl>

 


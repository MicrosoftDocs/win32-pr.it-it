---
description: Rappresenta un evento di aggregazione di diversi eventi intrinseci o estrinseci singoli.
ms.assetid: 99afa390-01fe-4a13-ba21-27587470f111
ms.tgt_platform: multiple
title: Classe __AggregateEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __AggregateEvent
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: f93a962e57452ac555214e42f00af8ac8a4ea3db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317604"
---
# <a name="__aggregateevent-class"></a>\_\_Classe AggregateEvent

La classe di sistema **\_ \_ AggregateEvent** rappresenta un evento di aggregazione di più eventi intrinseci o estrinseci singoli. WMI genera un'istanza di **\_ \_ AggregateEvent** anziché di un [**\_ \_ evento**](--event.md) quando gli utenti effettuano la registrazione con la clausola [Group](group-clause.md) into nella query di eventi.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class __AggregateEvent : __IndicationRelated
{
  uint32 NumberOfEvents;
  object Representative;
};
```

## <a name="members"></a>Members

La classe **\_ \_ AggregateEvent** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **\_ \_ AggregateEvent** dispone di queste proprietà.

<dl> <dt>

**NumberOfEvents**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di eventi combinati per produrre questo evento di riepilogo singolo.

</dd> <dt>

**Representative**
</dt> <dd> <dl> <dt>

Tipo di dati: **Object**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Copia di uno degli eventi recapitati all'interno dell'intervallo di aggregazione. Ad esempio, se un consumer ha effettuato la registrazione per gli eventi di modifica della chiave del registro di sistema dal provider di eventi del registro di sistema, il **rappresentante** manterrà un'istanza della classe **RegistryKeyChangeEvent** .

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **\_ \_ AggregateEvent** deriva da [**\_ \_ IndicationRelated**](--indicationrelated.md), che non dispone di proprietà.

I provider di eventi non generano mai eventi aggregati. Devono ignorare la clausola GROUP with nell'elaborazione delle query di eventi.

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

[Esecuzione di query con WQL](querying-with-wql.md)
</dt> </dl>

 


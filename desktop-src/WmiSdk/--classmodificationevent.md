---
description: Rappresenta un evento di modifica della classe, ovvero un tipo di evento intrinseco generato quando una classe viene modificata nello spazio dei nomi .
ms.assetid: 77e8e025-d584-495d-98f8-71e7fb2c9698
ms.tgt_platform: multiple
title: __ClassModificationEvent classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassModificationEvent
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: a5561f7cdb0bcb434ae43fb393e39b3edba47987f47b15583702d96bdb3ded7b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119732951"
---
# <a name="__classmodificationevent-class"></a>\_\_Classe ClassModificationEvent

La **\_ \_ classe di sistema ClassModificationEvent** rappresenta un evento [](determining-the-type-of-event-to-receive.md) di modifica della classe, ovvero un tipo di evento intrinseco generato quando una classe viene modificata nello spazio dei nomi .

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class __ClassModificationEvent : __ClassOperationEvent
{
  object PreviousClass;
  uint8  SECURITY_DESCRIPTOR[];
  object TargetClass;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Members

La **\_ \_ classe ClassModificationEvent** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **\_ \_ classe ClassModificationEvent** ha queste proprietà.

<dl> <dt>

**PreviousClass**
</dt> <dd> <dl> <dt>

Tipo di dati: **object**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Copia della versione originale della classe .

</dd> <dt>

**DESCRITTORE \_ DI SICUREZZA**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrittore utilizzato dal provider di eventi per determinare quali utenti possono ricevere l'evento. Questa proprietà viene ereditata [**\_ \_ dall'evento**](--event.md).

</dd> <dt>

**Classe di destinazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **object**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Copia della classe appena modificata segnalata dall'evento di modifica della classe. Questa proprietà viene ereditata da [**\_ \_ ClassOperationEvent.**](--classoperationevent.md)

</dd> <dt>

**ORA \_ DI CREAZIONE**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore univoco che indica l'ora in cui è stato generato l'evento. Si tratta di un valore a 64 bit che rappresenta il numero di intervalli di 100 nanosecondi dopo il 1° gennaio 1601. Le informazioni sono nel formato UTC (Coordinated Universal Times). Questa proprietà viene ereditata [**\_ \_ dall'evento**](--event.md).

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> </dl>

## <a name="remarks"></a>Commenti

La **\_ \_ classe ClassModificationEvent** è derivata da [**\_ \_ ClassOperationEvent.**](--classoperationevent.md)

L'evento segnala le versioni nuove e precedenti della definizione della classe.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |
| Spazio dei nomi<br/>                | Tutti gli spazi dei nomi WMI<br/>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_\_ClassOperationEvent**](/windows/desktop/WmiSdk/--classoperationevent)
</dt> <dt>

[Classi di sistema WMI](wmi-system-classes.md)
</dt> </dl>

 


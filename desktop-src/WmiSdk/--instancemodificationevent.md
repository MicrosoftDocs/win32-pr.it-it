---
description: Segnala un evento di modifica dell'istanza, ovvero un tipo di evento intrinseco generato quando un'istanza viene modificata nello spazio dei nomi .
ms.assetid: aa35f349-8b57-435f-bf82-76daf2b43ec9
ms.tgt_platform: multiple
title: __InstanceModificationEvent classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceModificationEvent
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: fffc8508eff24181201792207a151f5effd28a3022fec56506953b55d3e59deb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118557758"
---
# <a name="__instancemodificationevent-class"></a>\_\_Classe InstanceModificationEvent

La **\_ \_ classe di sistema InstanceModificationEvent** segnala un evento [](determining-the-type-of-event-to-receive.md) di modifica dell'istanza, ovvero un tipo di evento intrinseco generato quando un'istanza viene modificata nello spazio dei nomi .

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class __InstanceModificationEvent : __InstanceOperationEvent
{
  object PreviousInstance;
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Members

La **\_ \_ classe InstanceModificationEvent** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **\_ \_ classe InstanceModificationEvent** ha queste proprietà.

<dl> <dt>

**Istanza precedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **object**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Copia dell'istanza di prima della modifica.

</dd> <dt>

**DESCRITTORE \_ DI SICUREZZA**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrittore utilizzato dal provider di eventi per determinare quali utenti possono ricevere l'evento. Questa proprietà viene ereditata [**\_ \_ dall'evento**](--event.md).

</dd> <dt>

**Istanza di destinazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **object**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nuova versione dell'istanza modificata. Questa proprietà viene ereditata da [**\_ \_ InstanceOperationEvent.**](--instanceoperationevent.md)

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

La **\_ \_ classe InstanceModificationEvent** è derivata da [**\_ \_ InstanceOperationEvent.**](--instanceoperationevent.md)

**Modifica di una risorsa: \_ \_ InstanceModificationEvent**

Si supponga di sospettare che un'applicazione di gestione in uso cambi erroneamente il tipo di avvio di un servizio in uno dei server. Si vuole scrivere uno script WMI per monitorare eventuali modifiche apportate alla configurazione del servizio. Non appena viene apportata una modifica a un servizio, l'istanza TargetInstance corrispondente riflette la modifica.

Se si registra l'interesse per questo evento, una modifica alla configurazione del servizio comporta la creazione di un'istanza **\_ \_ della classe InstanceModificationEvent.**

Le query di notifica che richiedono la notifica della modifica di una risorsa e usano eventi intrinseci usano tutte una sintassi simile alla seguente:

`SELECT * FROM __InstanceModificationEvent WITHIN PollingInterval WHERE TargetInstance ISA 'Win32_Service' and TargetInstance.Name = 'alerter'`

## <a name="examples"></a>Esempio

[L'esempio VBScript](https://Gallery.TechNet.Microsoft.Com/daa06cdd-c1d9-4179-ba67-83aef2b9a079) monitor process modification event in TechNet Gallery usa **\_ \_ InstanceModificationEvent** per monitorare la prima occorrenza di un evento di modifica dell'istanza WMI per [**il processo Win32. \_**](/windows/desktop/CIMWin32Prov/win32-process)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |
| Spazio dei nomi<br/>                | Tutti gli spazi dei nomi WMI<br/>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_\_InstanceOperationEvent**](/windows/desktop/WmiSdk/--instanceoperationevent)
</dt> <dt>

[Classi di sistema WMI](wmi-system-classes.md)
</dt> </dl>

 


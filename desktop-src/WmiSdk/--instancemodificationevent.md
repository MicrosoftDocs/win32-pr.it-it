---
description: Segnala un evento di modifica dell'istanza, ovvero un tipo di evento intrinseco generato quando un'istanza viene modificata nello spazio dei nomi.
ms.assetid: aa35f349-8b57-435f-bf82-76daf2b43ec9
ms.tgt_platform: multiple
title: Classe __InstanceModificationEvent
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
ms.openlocfilehash: e644db16b6638bbc87006819e186540a9ce1874e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883549"
---
# <a name="__instancemodificationevent-class"></a>\_\_Classe InstanceModificationEvent

La classe di sistema **\_ \_ InstanceModificationEvent** segnala un evento di modifica dell'istanza, ovvero un tipo di [evento intrinseco](determining-the-type-of-event-to-receive.md) generato quando un'istanza viene modificata nello spazio dei nomi.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

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

La classe **\_ \_ InstanceModificationEvent** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **\_ \_ InstanceModificationEvent** dispone di queste proprietà.

<dl> <dt>

**PreviousInstance**
</dt> <dd> <dl> <dt>

Tipo di dati: **Object**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Copia dell'istanza prima della modifica.

</dd> <dt>

**descrittore di sicurezza \_**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrittore utilizzato dal provider di eventi per determinare gli utenti che possono ricevere l'evento. Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).

</dd> <dt>

**TargetInstance**
</dt> <dd> <dl> <dt>

Tipo di dati: **Object**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nuova versione dell'istanza modificata. Questa proprietà viene ereditata da [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).

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

La classe **\_ \_ InstanceModificationEvent** deriva da [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).

**Modifica di una risorsa: \_ \_ InstanceModificationEvent**

Si supponga di sospettare che un'applicazione di gestione in uso modifichi erroneamente il tipo di avvio di un servizio in uno dei server. Si desidera scrivere uno script WMI per monitorare tutte le modifiche apportate alla configurazione del servizio. Non appena viene apportata una modifica a un servizio, il TargetInstance corrispondente riflette la modifica.

Se si registra il proprio interesse in questo evento, una modifica alla configurazione del servizio comporta la creazione di un'istanza della classe **\_ \_ InstanceModificationEvent** .

Per le query di notifica che richiedono la notifica della modifica di una risorsa e l'utilizzo di eventi intrinseci tutti viene utilizzata una sintassi simile alla seguente:

`SELECT * FROM __InstanceModificationEvent WITHIN PollingInterval WHERE TargetInstance ISA 'Win32_Service' and TargetInstance.Name = 'alerter'`

## <a name="examples"></a>Esempio

L'esempio di [monitoraggio del processo di modifica dell'evento](https://Gallery.TechNet.Microsoft.Com/daa06cdd-c1d9-4179-ba67-83aef2b9a079) VBScript sulla raccolta TechNet utilizza **\_ \_ InstanceModificationEvent** per monitorare la prima occorrenza di un evento di modifica dell'istanza WMI per il [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process).

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

 


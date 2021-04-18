---
description: Segnala un evento di eliminazione di un'istanza, ovvero un tipo di evento intrinseco generato quando un'istanza viene eliminata dallo spazio dei nomi.
ms.assetid: a370fc95-15e3-49c3-98de-2f40d742f207
ms.tgt_platform: multiple
title: Classe __InstanceDeletionEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceDeletionEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 018bac665aa95393fc1a9c7e51ad42038e8b27c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315259"
---
# <a name="__instancedeletionevent-class"></a>\_\_Classe InstanceDeletionEvent

La classe di sistema **\_ \_ InstanceDeletionEvent** segnala un evento di eliminazione di un'istanza, ovvero un tipo di [evento intrinseco](determining-the-type-of-event-to-receive.md) generato quando un'istanza viene eliminata dallo spazio dei nomi.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class __InstanceDeletionEvent : __InstanceOperationEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Members

La classe **\_ \_ InstanceDeletionEvent** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **\_ \_ InstanceDeletionEvent** dispone di queste proprietà.

<dl> <dt>

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

Copia dell'istanza di eliminata. Questa proprietà viene ereditata da [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).

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

La classe **\_ \_ InstanceDeletionEvent** deriva da [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).

**Eliminazione di una risorsa: \_ \_ InstanceDeletionEvent**

Se si desidera garantire che un programma antivirus specifico continui a essere eseguito in un computer, è possibile scrivere uno script che monitora i processi nel computer per determinare se uno di essi viene arrestato.

Per le query di notifica che richiedono la notifica dell'eliminazione di una risorsa e l'utilizzo di eventi intrinseci tutti viene utilizzata una sintassi simile alla seguente:

`SELECT * FROM __InstanceDeletionEvent WHERE TargetInstance ISA 'Win32_Process' and TargetInstance.Name = 'notepad.exe' `

## <a name="examples"></a>Esempio

Il codice di esempio di [monitoraggio dell'evento di eliminazione del processo](https://Gallery.TechNet.Microsoft.Com/060a9adb-f99b-4f34-ba65-19b5f5815a38) VBScript nella raccolta TechNet utilizza **\_ \_ InstanceDeletionEvent** per monitorare la prima occorrenza di un evento di eliminazione di un'istanza WMI per il [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process).

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

 


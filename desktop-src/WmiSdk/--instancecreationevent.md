---
description: Segnala un evento di creazione di istanza, ovvero un tipo di evento intrinseco che viene generato quando una nuova istanza di viene aggiunta allo spazio dei nomi.
ms.assetid: 41976479-70e3-4914-a56a-fa94a1fd31c7
ms.tgt_platform: multiple
title: Classe __InstanceCreationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceCreationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 29bdefbe1db20cd8b55b74433061b6c0cf152378
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233479"
---
# <a name="__instancecreationevent-class"></a>\_\_Classe InstanceCreationEvent

La classe di sistema **\_ \_ InstanceCreationEvent** segnala un evento di creazione di istanza, ovvero un tipo di [evento intrinseco](determining-the-type-of-event-to-receive.md) che viene generato quando una nuova istanza viene aggiunta allo spazio dei nomi.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class __InstanceCreationEvent : __InstanceOperationEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Members

La classe **\_ \_ InstanceCreationEvent** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **\_ \_ InstanceCreationEvent** dispone di queste proprietà.

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

Copia dell'istanza di creata. Questa proprietà viene ereditata da [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).

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

La classe **\_ \_ InstanceCreationEvent** deriva da [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).

**Creazione di una risorsa: \_ \_ InstanceCreationEvent**

Si supponga di essere interessati a ricevere una notifica se il blocco note viene eseguito in un determinato computer. Quando viene eseguito il blocco note, viene creato un processo corrispondente. I processi possono essere gestiti tramite WMI e sono rappresentati dalla \_ classe di processo Win32. Quando viene avviata l'esecuzione del blocco note, un'istanza corrispondente della \_ classe di processo Win32 diventa disponibile tramite WMI. Se l'interesse è stato registrato in questo evento (eseguendo la query di notifica degli eventi appropriata), la disponibilità di questa istanza comporta la creazione di un'istanza della classe **\_ \_ InstanceCreationEvent** .

Per le query di notifica che richiedono la notifica della creazione di una risorsa e l'utilizzo di eventi intrinseci tutti viene utilizzata una sintassi simile alla seguente:

`SELECT * FROM __InstanceCreationEvent WITHIN PollingInterval WHERE TargetInstance ISA 'Win32_Process' and TargetInstance.Name = 'notepad.exe'`

Per una descrizione più approfondita dell'uso di **\_ \_ InstanceCreationEvent** come metodo per il monitoraggio dei file System, vedere [WMI e monitoraggio del file System](https://www.codeproject.com/Articles/42212/WMI-and-File-System-Monitoring) in CodeProject.

## <a name="examples"></a>Esempio

Nell'esempio di PowerShell [per la creazione di una registrazione di eventi WMI permanenti per il monitoraggio dei file](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) nella raccolta TechNet viene usato **\_ \_ InstanceCreationEvent** come parte di uno script complesso per configurare la registrazione di un evento WMI permanente.

L'esempio PowerShell per [gli eventi permanenti WMI di PowerShell](https://Gallery.TechNet.Microsoft.Com/PowerShell-WMI-Permanent-7e17f262) nella raccolta TechNet USA **\_ \_ InstanceCreationEvent** come parte di uno script di dimostrazione per la configurazione di una registrazione di eventi permanenti.

L'esempio di [monitoraggio del processo di creazione dell'evento](https://Gallery.TechNet.Microsoft.Com/6f137d9e-f00a-4f0a-ad07-7d752ff5251d) VBScript in TechNet utilizza **\_ \_ InstanceCreationEvent** per monitorare il primo evento di creazione dell'istanza WMI per il [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process).

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

 


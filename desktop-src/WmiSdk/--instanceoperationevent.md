---
description: Funge da classe base per tutti gli eventi intrinseci correlati a un'istanza di.
ms.assetid: f6d2b6e5-0dca-4cb5-95a5-33b45cd76807
ms.tgt_platform: multiple
title: Classe __InstanceOperationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceOperationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 1d3111b74c876cc7ffedb959eca7f46812ed92e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317592"
---
# <a name="__instanceoperationevent-class"></a>\_\_Classe InstanceOperationEvent

La classe di sistema **\_ \_ InstanceOperationEvent** funge da classe di base per tutti gli eventi intrinseci correlati a un'istanza di.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class __InstanceOperationEvent : __Event
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Members

La classe **\_ \_ InstanceOperationEvent** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **\_ \_ InstanceOperationEvent** dispone di queste proprietà.

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

Istanza interessata dall'evento. Per gli eventi di creazione, si tratta dell'istanza appena creata. Per gli eventi di modifica, si tratta della nuova versione dell'istanza modificata. Per gli eventi di eliminazione, si tratta dell'istanza eliminata.

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

La classe **\_ \_ InstanceOperationEvent** è derivata dall' [**\_ \_ evento**](--event.md).

Le istanze di **\_ \_ InstanceOperationEvent** non vengono create. vengono create solo le istanze delle relative sottoclassi. Le classi seguenti derivano da **\_ \_ InstanceOperationEvent**:

[**\_\_InstanceCreationEvent**](--instancecreationevent.md)

[**\_\_InstanceModificationEvent**](--instancemodificationevent.md)

[**\_\_InstanceDeletionEvent**](--instancedeletionevent.md)

**Overview**

Analogamente a una classe WMI che rappresenta ogni tipo di risorsa di sistema che può essere gestita tramite WMI, esiste una classe WMI che rappresenta ogni tipo di evento WMI. Quando si verifica un evento che può essere monitorato da WMI, viene creata un'istanza della classe di evento WMI corrispondente. Un evento WMI si verifica quando viene creata l'istanza.

Esistono tre tipi principali di classi di evento WMI, che derivano tutti dalla classe WMI dell' [**\_ \_ evento**](--event.md) : eventi intrinseci, eventi estrinseci ed eventi del timer. Gli eventi intrinseci, a loro volta, sono rappresentati da tre classi distinte derivate dalla classe di **\_ \_ evento** : [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md), **\_ \_ InstanceOperationEvent** e [**\_ \_ ClassOperationEvent**](--classoperationevent.md).

Eventi intrinseci

Gli eventi intrinseci vengono usati per monitorare una risorsa rappresentata da una classe nel repository CIM. Ogni risorsa è rappresentata da un'istanza di una classe. Questo significa che il monitoraggio di una risorsa tramite WMI comporta effettivamente il monitoraggio delle istanze che corrispondono alla risorsa.

Gli eventi intrinseci possono essere usati anche per monitorare le modifiche apportate a uno spazio dei nomi o a una classe nel repository. Tuttavia, il monitoraggio delle modifiche apportate agli spazi dei nomi o alle classi ha un valore limitato per gli amministratori di sistema.

Un evento intrinseco è rappresentato da un'istanza di una classe derivata da \_ \_ InstanceOperationEvent, \_ \_ NamespaceOperationEvent o \_ \_ ClassOperationEvent. Tutte le modifiche apportate alle istanze in WMI sono rappresentate dalla \_ \_ classe InstanceOperationEvent e dalle classi derivate: \_ \_ InstanceCreationEvent, \_ \_ InstanceModificationEvent e \_ \_ InstanceDeletionEvent.

Il monitoraggio delle risorse tramite WMI prevede il monitoraggio di istanze e tutte le modifiche alle istanze sono rappresentate da \_ \_ InstanceOperationEvent e dalle classi derivate. Questo significa che le risorse di monitoraggio includono in definitiva le istanze di monitoraggio delle \_ \_ classi derivate da InstanceOperationEvent.

Per registrare l'interesse nelle istanze di una di queste classi, è necessario emettere una query di notifica espressa in WQL. La query utilizza una sintassi simile alla seguente:

`SELECT * FROM __InstanceOperationEventOrDerivedClass WITHIN PollingInterval WHERE TargetInstance ISA WMIClassName AND TargetInstance.WMIClassPropertyName = Value`

Per una discussione più lunga sull'utilizzo degli eventi dell'istanza WMI per monitorare l'attività del computer, vedere [come è possibile monitorare i diversi tipi di eventi con un solo script?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/04/04/how-can-i-monitor-for-different-types-of-events-with-just-one-script.aspx)

## <a name="examples"></a>Esempio

L'esempio di codice per l' [evento di monitoraggio](https://Gallery.TechNet.Microsoft.Com/94c7dc4c-813a-411d-aa3f-f98982cd2a2f) VBScript della raccolta TechNet USA **\_ \_ InstanceOperationEvent** per monitorare il primo evento dell'istanza WMI per il [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |
| Spazio dei nomi<br/>                | Tutti gli spazi dei nomi WMI<br/>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_\_Evento**](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[Classi di sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Determinazione del tipo di evento da ricevere](determining-the-type-of-event-to-receive.md)
</dt> <dt>

[Scrittura in un file di log in base a un evento](writing-to-a-log-file-based-on-an-event.md)
</dt> </dl>

 


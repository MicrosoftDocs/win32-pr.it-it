---
description: Funge da classe base per tutti gli eventi intrinseci correlati a un'istanza di .
ms.assetid: f6d2b6e5-0dca-4cb5-95a5-33b45cd76807
ms.tgt_platform: multiple
title: __InstanceOperationEvent classe
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
ms.openlocfilehash: a4e988f26b64d0d8bd4a23f853b7bf9dc92f2610936239b4363439d5c7d70170
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320808"
---
# <a name="__instanceoperationevent-class"></a>\_\_Classe InstanceOperationEvent

La classe di sistema **\_ \_ InstanceOperationEvent** funge da classe di base per tutti gli eventi intrinseci correlati a un'istanza.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

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

La **\_ \_ classe InstanceOperationEvent** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **\_ \_ classe InstanceOperationEvent** ha queste proprietà.

<dl> <dt>

**DESCRITTORE \_ DI SICUREZZA**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrittore utilizzato dal provider di eventi per determinare quali utenti possono ricevere l'evento. Questa proprietà viene ereditata [**\_ \_ dall'evento**](--event.md).

</dd> <dt>

**TargetInstance**
</dt> <dd> <dl> <dt>

Tipo di dati: **object**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Istanza interessata dall'evento . Per gli eventi di creazione, si tratta dell'istanza appena creata. Per gli eventi di modifica, si tratta della nuova versione dell'istanza modificata. Per gli eventi di eliminazione, si tratta dell'istanza eliminata.

</dd> <dt>

**ORA \_ DI CREAZIONE**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore univoco che indica l'ora in cui è stato generato l'evento. Valore a 64 bit che rappresenta il numero di intervalli di 100 nanosecondi dopo il 1° gennaio 1601. Le informazioni sono nel formato UTC (Coordinated Universal Times). Questa proprietà viene ereditata [**\_ \_ dall'evento**](--event.md).

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Commenti

La **\_ \_ classe InstanceOperationEvent** è derivata da [**\_ \_ Event**](--event.md).

Le istanze **\_ \_ di InstanceOperationEvent** non vengono create. Vengono create solo istanze delle relative sottoclassi. Le classi seguenti derivano da **\_ \_ InstanceOperationEvent**:

[**\_\_InstanceCreationEvent**](--instancecreationevent.md)

[**\_\_InstanceModificationEvent**](--instancemodificationevent.md)

[**\_\_InstanceDeletionEvent**](--instancedeletionevent.md)

**Overview**

Così come esiste una classe WMI che rappresenta ogni tipo di risorsa di sistema che può essere gestita tramite WMI, esiste una classe WMI che rappresenta ogni tipo di evento WMI. Quando si verifica un evento che può essere monitorato da WMI, viene creata un'istanza della classe di evento WMI corrispondente. Un evento WMI si verifica quando viene creata l'istanza.

Esistono tre tipi principali di classi di eventi WMI, tutti derivati dalla classe [**\_ \_ WMI**](--event.md) event: eventi intrinseci, eventi estensivi ed eventi timer. Gli eventi intrinseci, a loro volta, sono rappresentati da tre classi distinte derivate dalla classe **\_ \_ Event:** [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md), **\_ \_ InstanceOperationEvent** e [**\_ \_ ClassOperationEvent**](--classoperationevent.md).

Eventi intrinseci

Gli eventi intrinseci vengono usati per monitorare una risorsa rappresentata da una classe nel repository CIM. Ogni risorsa è rappresentata da un'istanza di una classe. Ciò significa che il monitoraggio di una risorsa tramite WMI comporta effettivamente il monitoraggio delle istanze che corrispondono alla risorsa.

Gli eventi intrinseci possono essere usati anche per monitorare le modifiche apportate a uno spazio dei nomi o a una classe nel repository. Tuttavia, il monitoraggio delle modifiche agli spazi dei nomi o alle classi ha un valore limitato per gli amministratori di sistema.

Un evento intrinseco è rappresentato da un'istanza di una classe derivata da \_ \_ InstanceOperationEvent, \_ \_ NamespaceOperationEvent o \_ \_ ClassOperationEvent. Tutte le modifiche alle istanze in WMI sono rappresentate dalla classe InstanceOperationEvent e dalle classi derivate \_ \_ da essa: \_ \_ InstanceCreationEvent, \_ \_ InstanceModificationEvent e \_ \_ InstanceDeletionEvent.

Il monitoraggio delle risorse tramite WMI comporta il monitoraggio delle istanze e tutte le modifiche alle istanze sono rappresentate da \_ \_ InstanceOperationEvent e dalle classi derivate da essa. Ciò significa che il monitoraggio delle risorse comporta infine il monitoraggio delle istanze delle \_ \_ classi derivate da InstanceOperationEvent.

È possibile registrare interesse per le istanze di una di queste classi inviando una query di notifica espressa in WQL. La query usa una sintassi simile alla seguente:

`SELECT * FROM __InstanceOperationEventOrDerivedClass WITHIN PollingInterval WHERE TargetInstance ISA WMIClassName AND TargetInstance.WMIClassPropertyName = Value`

Per una descrizione più approfondita dell'uso degli eventi dell'istanza WMI per monitorare l'attività del computer, vedere Come è possibile monitorare diversi tipi di [eventi con un solo script?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/04/04/how-can-i-monitor-for-different-types-of-events-with-just-one-script.aspx)

## <a name="examples"></a>Esempio

[L'esempio di](https://Gallery.TechNet.Microsoft.Com/94c7dc4c-813a-411d-aa3f-f98982cd2a2f) codice VBScript dell'evento monitor process in TechNet Gallery usa **\_ \_ InstanceOperationEvent** per monitorare il primo evento dell'istanza WMI per [**il processo Win32. \_**](/windows/desktop/CIMWin32Prov/win32-process)

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

 


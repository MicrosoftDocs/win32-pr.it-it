---
description: 'Prima di eseguire la registrazione per ricevere un evento, è necessario determinare i tipi di eventi da ricevere: intrinseco o estrinseco.'
ms.assetid: 46cdfcfa-42c6-4169-bc4d-725867224889
ms.tgt_platform: multiple
title: Determinazione del tipo di evento da ricevere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 477f3d10536e5b0622e1e64b6cec9abdf4183c7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758018"
---
# <a name="determining-the-type-of-event-to-receive"></a>Determinazione del tipo di evento da ricevere

Prima di eseguire la registrazione per ricevere un evento, è necessario determinare i tipi di eventi da ricevere: [intrinseco](#intrinsic-events) o [estrinseco](#extrinsic-events). Per ulteriori informazioni su come ricevere gli eventi, vedere [ricezione di un evento WMI](receiving-a-wmi-event.md). Per ulteriori informazioni sulla fornitura di eventi, vedere [sviluppo di un provider WMI](developing-a-wmi-provider.md) e [scrittura di un provider di eventi](writing-an-event-provider.md). Per ulteriori informazioni sui problemi di sicurezza relativi alla ricezione e alla fornitura di eventi, vedere [protezione degli eventi WMI.](securing-wmi-events.md)

## <a name="intrinsic-events"></a>Eventi intrinseci

Un evento intrinseco è un evento che si verifica in risposta a una modifica nel modello di dati WMI standard. Ogni classe di eventi intrinseci rappresenta un tipo specifico di modifica e si verifica quando WMI o un provider crea, elimina, rimuove o modifica uno spazio dei nomi, una classe o un'istanza della classe. La creazione di un'istanza di [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , ad esempio, comporterebbe un'istanza di [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) .

WMI crea eventi intrinseci per gli oggetti archiviati nel repository WMI. Un provider genera eventi intrinseci per le classi dinamiche, ma WMI può creare un'istanza per una classe dinamica se non è disponibile alcun provider. WMI utilizza il polling per rilevare le modifiche. Nella tabella seguente sono elencate le classi di sistema utilizzate da WMI per segnalare gli eventi intrinseci.



| Classe di sistema                                                           | Descrizione                                                                                                                                                                                             |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_\_ClassCreationEvent**](--classcreationevent.md)                 | Notifica a un utente quando viene creata una classe.                                                                                                                                                            |
| [**\_\_ClassDeletionEvent**](--classdeletionevent.md)                 | Notifica a un consumer quando una classe viene eliminata.                                                                                                                                                            |
| [**\_\_ClassModificationEvent**](--classmodificationevent.md)         | Notifica a un consumer quando una classe viene modificata.                                                                                                                                                           |
| [**\_\_InstanceCreationEvent**](--instancecreationevent.md)           | Notifica a un utente quando viene creata un'istanza della classe.                                                                                                                                                   |
| [**\_\_InstanceOperationEvent**](--instanceoperationevent.md)         | Notifica a un consumer quando si verifica un evento di istanza, ad esempio la creazione, l'eliminazione o la modifica dell'istanza. È possibile utilizzare questa classe nelle query per ottenere tutti i tipi di eventi associati a un'istanza di. |
| [**\_\_InstanceDeletionEvent**](--instancedeletionevent.md)           | Notifica a un consumer quando un'istanza viene eliminata.                                                                                                                                                        |
| [**\_\_InstanceModificationEvent**](--instancemodificationevent.md)   | Notifica a un consumer quando un'istanza di viene modificata.                                                                                                                                                       |
| [**\_\_NamespaceCreationEvent**](--namespacecreationevent.md)         | Notifica a un consumer quando viene creato uno spazio dei nomi.                                                                                                                                                        |
| [**\_\_NamespaceDeletionEvent**](--namespacedeletionevent.md)         | Notifica a un consumer quando uno spazio dei nomi viene eliminato.                                                                                                                                                        |
| [**\_\_NamespaceModificationEvent**](--namespacemodificationevent.md) | Notifica a un consumer quando uno spazio dei nomi viene modificato.                                                                                                                                                       |
| [**\_\_ConsumerFailureEvent**](--consumerfailureevent.md)             | Notifica a un consumer quando un altro evento viene eliminato a causa di un errore della parte di un consumer di eventi.                                                                                                 |
| [**\_\_EventDroppedEvent**](--eventdroppedevent.md)                   | Notifica a un consumer quando viene eliminato un altro evento anziché essere recapitato al consumer di eventi richiedente.                                                                                       |
| [**\_\_EventQueueOverflowEvent**](--eventqueueoverflowevent.md)       | Notifica a un utente quando un evento viene eliminato in seguito a un overflow della coda di recapito.                                                                                                                  |
| [**\_\_MethodInvocationEvent**](--methodinvocationevent.md)           | Notifica a un consumer quando si verifica un evento di chiamata al metodo.                                                                                                                                                    |



 

## <a name="extrinsic-events"></a>Eventi estrinseci

Un evento estrinseco è un'occorrenza predefinita che non può essere collegata direttamente alle modifiche nel modello di dati WMI. Pertanto, WMI consente a un provider di eventi di definire una classe di evento che descrive l'evento. Ad esempio, un evento che descrive un computer che passa alla modalità standby è un evento estrinseco. Un provider deriva un evento estrinseco dalla classe di sistema [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md) , che è una sottoclasse della classe del sistema di [**\_ \_ eventi**](--event.md) . Il [Registro di sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) e i provider [SNMP](snmp-provider.md) definiscono le classi di evento estrinseche, ad esempio **RegistryKeyChangeEvent**, che invia una notifica a un consumer quando viene modificata una chiave del registro di sistema. Per ulteriori informazioni, vedere la pagina [relativa alla registrazione degli eventi del registro di sistema e alla](registering-for-system-registry-events.md) [scrittura di un provider di eventi](writing-an-event-provider.md).

Nell'esempio seguente un provider di eventi segnala violazioni di sicurezza a una o più costruzioni. La classe seguente potrebbe essere definita per l'evento estrinseco che rappresenta una violazione di sicurezza.

``` syntax
class SecurityViolationEvent : __ExtrinsicEvent
{
   string Building;           // building where violation occurred
   sint32 EntranceNumber;     // entrance where violation occurred
   datetime TimeOfDetection;  // date and time of violation
}
```

Per ricevere le notifiche di violazione di sicurezza, un consumer registra per il tipo di evento SecurityViolationEvent. Se non diversamente specificato, un consumatore riceve la notifica di tutte le violazioni di sicurezza durante tutti i periodi di tempo e in tutti gli edifici. La classe di evento contiene inoltre informazioni che possono essere utilizzate dai consumer per richiedere eventi più specifici.

Nell'esempio seguente la query registra il consumer per gli eventi di violazione di sicurezza solo nell'edificio 24.

`SELECT * FROM SecurityViolationEvent WHERE Building = 24;`

 

 

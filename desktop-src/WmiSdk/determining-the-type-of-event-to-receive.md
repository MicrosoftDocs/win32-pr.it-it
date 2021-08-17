---
description: 'Prima di registrarsi per ricevere un evento, è necessario determinare i tipi di eventi da ricevere: intrinseci o estensivi.'
ms.assetid: 46cdfcfa-42c6-4169-bc4d-725867224889
ms.tgt_platform: multiple
title: Determinazione del tipo di evento da ricevere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9172e3246a31cb42ada3b9f5099bc3b0575959c125dedd44d7c6ed745134a4a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119374651"
---
# <a name="determining-the-type-of-event-to-receive"></a>Determinazione del tipo di evento da ricevere

Prima di registrarsi per ricevere un evento, è necessario determinare i tipi di eventi da ricevere: [intrinseco](#intrinsic-events) o [estensivo.](#extrinsic-events) Per altre informazioni su come ricevere eventi, vedere [Ricezione di un evento WMI.](receiving-a-wmi-event.md) Per altre informazioni sulla fornitura di eventi, vedere [Sviluppo di un provider WMI](developing-a-wmi-provider.md) e Scrittura di un provider di [eventi](writing-an-event-provider.md). Per altre informazioni sui problemi di sicurezza per la ricezione e la fornitura di eventi, vedere [Protezione degli eventi WMI.](securing-wmi-events.md)

## <a name="intrinsic-events"></a>Eventi intrinseci

Un evento intrinseco è un evento che si verifica in risposta a una modifica nel modello di dati WMI standard. Ogni classe di eventi intrinseci rappresenta un tipo specifico di modifica e si verifica quando WMI o un provider crea, elimina, rimuove o modifica uno spazio dei nomi, una classe o un'istanza della classe. Ad esempio, la creazione di [**un'istanza \_ di Win32 LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) comporta [**\_ \_ un'istanza di InstanceCreationEvent.**](--instancecreationevent.md)

WMI crea eventi intrinseci per gli oggetti archiviati nel repository WMI. Un provider genera eventi intrinseci per le classi dinamiche, ma WMI può creare un'istanza per una classe dinamica se non è disponibile alcun provider. WMI usa il polling per rilevare le modifiche. Nella tabella seguente sono elencate le classi di sistema utilizzate da WMI per segnalare gli eventi intrinseci.



| Classe di sistema                                                           | Descrizione                                                                                                                                                                                             |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_\_ClassCreationEvent**](--classcreationevent.md)                 | Notifica a un consumer quando viene creata una classe.                                                                                                                                                            |
| [**\_\_ClassDeletionEvent**](--classdeletionevent.md)                 | Notifica a un consumer quando viene eliminata una classe.                                                                                                                                                            |
| [**\_\_ClassModificationEvent**](--classmodificationevent.md)         | Notifica a un consumer quando una classe viene modificata.                                                                                                                                                           |
| [**\_\_InstanceCreationEvent**](--instancecreationevent.md)           | Notifica a un consumer quando viene creata un'istanza della classe.                                                                                                                                                   |
| [**\_\_InstanceOperationEvent**](--instanceoperationevent.md)         | Notifica a un consumer quando si verifica un evento di istanza, ad esempio la creazione, l'eliminazione o la modifica dell'istanza. È possibile usare questa classe nelle query per ottenere tutti gli eventi di tipo associati a un'istanza di . |
| [**\_\_InstanceDeletionEvent**](--instancedeletionevent.md)           | Notifica a un consumer quando un'istanza viene eliminata.                                                                                                                                                        |
| [**\_\_InstanceModificationEvent**](--instancemodificationevent.md)   | Notifica a un consumer quando un'istanza viene modificata.                                                                                                                                                       |
| [**\_\_NamespaceCreationEvent**](--namespacecreationevent.md)         | Notifica a un consumer quando viene creato uno spazio dei nomi.                                                                                                                                                        |
| [**\_\_NamespaceDeletionEvent**](--namespacedeletionevent.md)         | Notifica a un consumer quando viene eliminato uno spazio dei nomi.                                                                                                                                                        |
| [**\_\_NamespaceModificationEvent**](--namespacemodificationevent.md) | Notifica a un consumer quando viene modificato uno spazio dei nomi.                                                                                                                                                       |
| [**\_\_ConsumerFailureEvent**](--consumerfailureevent.md)             | Notifica a un consumer quando un altro evento viene eliminato a causa di un errore da parte di un consumer di eventi.                                                                                                 |
| [**\_\_EventDroppedEvent**](--eventdroppedevent.md)                   | Notifica a un consumer quando viene eliminato un altro evento anziché essere recapitato al consumer di eventi richiedente.                                                                                       |
| [**\_\_EventQueueOverflowEvent**](--eventqueueoverflowevent.md)       | Notifica a un consumer quando un evento viene eliminato a causa di un overflow della coda di recapito.                                                                                                                  |
| [**\_\_MethodInvocationEvent**](--methodinvocationevent.md)           | Notifica a un consumer quando si verifica un evento di chiamata al metodo.                                                                                                                                                    |



 

## <a name="extrinsic-events"></a>Eventi estensivi

Un evento estensiva è un'occorrenza predefinita che non può essere collegata direttamente alle modifiche nel modello di dati WMI. WMI consente pertanto a un provider di eventi di definire una classe di evento che descrive l'evento. Ad esempio, un evento che descrive il passaggio di un computer alla modalità stand-by è un evento estensiva. Un provider deriva un evento etrinsico dalla classe di sistema [**\_ \_ ExtrinsicEvent,**](--extrinsicevent.md) che è una sottoclasse della classe di sistema [**\_ \_ Event.**](--event.md) I [provider del Registro di](/previous-versions/windows/desktop/regprov/system-registry-provider) sistema e [SNMP](snmp-provider.md) definiscono classi di eventi estensivi, ad esempio **RegistryKeyChangeEvent**, che notifica a un consumer quando viene modificata una chiave del Registro di sistema. Per altre informazioni, vedere [Registrazione per gli eventi del Registro di sistema](registering-for-system-registry-events.md) e Scrittura di un provider di [eventi](writing-an-event-provider.md).

Nell'esempio seguente un provider di eventi segnala violazioni della sicurezza a uno o più edifici. La classe seguente potrebbe essere definita per l'evento estensiva che rappresenta una violazione della sicurezza.

``` syntax
class SecurityViolationEvent : __ExtrinsicEvent
{
   string Building;           // building where violation occurred
   sint32 EntranceNumber;     // entrance where violation occurred
   datetime TimeOfDetection;  // date and time of violation
}
```

Per ricevere le notifiche di violazione della sicurezza, un consumer si registra per il tipo di evento SecurityViolationEvent. Se non diversamente specificato, un consumer riceve una notifica di tutte le violazioni della sicurezza durante tutti i periodi di tempo e in tutti gli edifici. La classe di evento contiene anche informazioni che i consumer possono usare per richiedere eventi più specifici.

Nell'esempio seguente la query registra il consumer per gli eventi di violazione della sicurezza solo nella compilazione 24.

`SELECT * FROM SecurityViolationEvent WHERE Building = 24;`

 

 

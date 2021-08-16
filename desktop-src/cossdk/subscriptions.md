---
description: I dati della sottoscrizione si trovano nel catalogo COM+ della sottoscrizione. È possibile creare una sottoscrizione usando lo strumento di amministrazione Servizi componenti o a livello di codice tramite l'interfaccia ICOMAdminCatalog::InstallComponent.
ms.assetid: 190e88f3-1d87-4c27-9451-0a633cbae829
title: Sottoscrizioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48810ae90f3507ea7afb661b106c4d05f8cc5b9a4f1b09aafdfb26d9fdb03a75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546173"
---
# <a name="subscriptions"></a>Sottoscrizioni

I dati della sottoscrizione si trovano nel catalogo COM+ della sottoscrizione. È possibile creare una sottoscrizione usando lo strumento di amministrazione Servizi componenti o a livello di codice tramite [**l'interfaccia ICOMAdminCatalog::InstallComponent.**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installcomponent)

La [**raccolta SubscriptionsForComponent**](subscriptionsforcomponent.md) viene usata per aggiungere, eliminare o modificare le informazioni relative alle sottoscrizioni. La **raccolta SubscriptionsForComponent** è una raccolta figlio di un componente. Per aggiungere una sottoscrizione, ottenere la raccolta **SubscriptionsForComponent** del componente e usare il [**metodo Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) per aggiungere una voce alla raccolta. Per configurare le varie proprietà dell'oggetto sottoscrizione, usare la [**proprietà Value.**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_value) Per salvare le modifiche, usare [**SaveChanges nell'oggetto**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) **raccolta SubscriptionsForComponent.**

È anche possibile utilizzare lo strumento di amministrazione Servizi componenti per modificare alcune, ma non tutte, le proprietà della sottoscrizione. Le sottoscrizioni specificano le informazioni seguenti:

-   Identità e posizione del sottoscrittore
-   Metodo di distribuzione
-   Metodi di evento da recapitare
-   Oggetto della classe di evento e proprietà PublisherID di un componente della classe di evento da cui il sottoscrittore desidera ricevere eventi

Le sottoscrizioni esistono indipendentemente dagli oggetti della classe di evento. È possibile disabilitare una sottoscrizione impostando la proprietà Enabled su False. Una sottoscrizione disabilitata non viene chiamata dagli eventi COM+.

I tre tipi di sottoscrizioni sono i seguenti:

<dl> <dt>

<span id="Persistent"></span><span id="persistent"></span><span id="PERSISTENT"></span>Persistente
</dt> <dd>

Le sottoscrizioni permanenti risiedono nel catalogo COM+ e sono indipendenti dalla durata del sottoscrittore. Le sottoscrizioni permanenti non vengono riavviate. In genere, viene creata una sottoscrizione permanente quando un'applicazione viene installata nel computer di un sottoscrittore e rimossa quando l'applicazione viene rimossa. Dopo la creazione di una sottoscrizione permanente, eventi COM+ attiva il sottoscrittore ogni volta che un evento deve essere recapitato al sottoscrittore.

Quando un server di pubblicazione crea [](the-com--event-class-object.md) un'istanza ed effettua una chiamata su un oggetto classe di evento, l'oggetto cerca tutte le sottoscrizioni persistenti nel catalogo COM+ e crea una nuova istanza di ogni oggetto. Il processo di creazione può essere diretto o tramite un moniker per i componenti in coda. Specificare l'oggetto sottoscrittore [**in base alla proprietà SubscriberMoniker**](subscriptionsforcomponent.md) della sottoscrizione. Gli oggetti Sottoscrittore creati da una sottoscrizione permanente vengono sempre rilasciati dopo ogni chiamata di evento.

</dd> <dt>

<span id="Transient"></span><span id="transient"></span><span id="TRANSIENT"></span>Transitoria
</dt> <dd>

Per le sottoscrizioni temporanee, è possibile usare la [**raccolta TransientSubscriptions,**](transientsubscriptions.md) il cui oggetto padre è l'oggetto catalogo radice. Le sottoscrizioni temporanee richiedono un evento per un oggetto sottoscrittore specifico già esistente. Le sottoscrizioni temporanee vengono archiviate nel catalogo COM+, ma la sottoscrizione viene eliminata se il sistema operativo o il sistema operativo viene arrestato. A differenza delle sottoscrizioni permanenti, le sottoscrizioni temporanee sono collegate a un determinato oggetto e vengono archiviate solo nel sistema di eventi. Le sottoscrizioni temporanee possono essere più efficienti delle sottoscrizioni permanenti, ma è necessario gestirne i cicli di vita degli oggetti. Per informazioni sulla registrazione di una sottoscrizione temporanea, vedere [Registrazione di una sottoscrizione temporanea.](registering-a-transient-subscription.md)

</dd> <dt>

<span id="Per_user"></span><span id="per_user"></span><span id="PER_USER"></span>Per utente
</dt> <dd>

Le sottoscrizioni per utente possono recapitare gli eventi solo quando il sottoscrittore è connesso al computer del sistema di eventi. Quando il sottoscrittore esegue l'accesso, il sistema di eventi abilita tutte le sottoscrizioni in cui il flag *PerUser* è impostato su **TRUE** e *UserName* è impostato sul nome dell'utente connesso. Quando il sottoscrittore si disconnette, le sottoscrizioni vengono disabilitate.

Le sottoscrizioni per utente hanno effetto solo quando il server di pubblicazione e il sottoscrittore sono nello stesso computer. L'accesso e la disconnessione vengono rilevati solo nel computer del server di pubblicazione, non nel computer in cui risiede l'oggetto sottoscrittore.

</dd> </dl>

Il sistema di eventi usa i meta-eventi per notificare ai sottoscrittori interessati ogni volta che vengono creati, modificati o rimossi oggetti della classe di evento o sottoscrizioni. Per ricevere metaeventi dal sistema di eventi, le applicazioni devono creare una sottoscrizione che risiede nel computer del sistema eventi e che specifica l'ID di interfaccia di attivazione (IID \_ IEventObjectChange).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtro di eventi in COM+](filtering-events-in-com-.md)
</dt> <dt>

[Pubblicazione e recapito di eventi in COM+](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[Oggetto della classe di evento COM+](the-com--event-class-object.md)
</dt> <dt>

[Uso di eventi COM+ con componenti in coda COM+](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 




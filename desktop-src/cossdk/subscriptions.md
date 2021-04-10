---
description: "I dati della sottoscrizione si trovano nel catalogo COM+ della sottoscrizione. È possibile creare una sottoscrizione usando lo strumento di amministrazione Servizi componenti o a livello di codice usando l'interfaccia ICOMAdminCatalog:: InstallComponent."
ms.assetid: 190e88f3-1d87-4c27-9451-0a633cbae829
title: Sottoscrizioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9973eb76fc22354f1a2fc8e381c90cf5be1efee3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225632"
---
# <a name="subscriptions"></a>Sottoscrizioni

I dati della sottoscrizione si trovano nel catalogo COM+ della sottoscrizione. È possibile creare una sottoscrizione usando lo strumento di amministrazione Servizi componenti o a livello di codice usando l'interfaccia [**ICOMAdminCatalog:: InstallComponent**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installcomponent) .

La raccolta [**SubscriptionsForComponent**](subscriptionsforcomponent.md) viene utilizzata per aggiungere, eliminare o modificare le informazioni relative alle sottoscrizioni. La raccolta **SubscriptionsForComponent** è una raccolta figlio di un componente. Per aggiungere una sottoscrizione, ottenere la raccolta **SubscriptionsForComponent** del componente e usare il metodo [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) per aggiungere una voce alla raccolta. Per impostare le varie proprietà dell'oggetto sottoscrizione, utilizzare la proprietà [**valore**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_value) . Per salvare le modifiche, usare [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) nell'oggetto della raccolta **SubscriptionsForComponent** .

È inoltre possibile utilizzare lo strumento di amministrazione Servizi componenti per modificare alcune delle proprietà della sottoscrizione, ma non tutte. Le sottoscrizioni specificano le seguenti informazioni:

-   Identità e percorso del Sottoscrittore
-   Metodo di distribuzione
-   Metodi di evento da recapitare
-   Oggetto classe di evento e proprietà PublisherID di un componente della classe di evento da cui il sottoscrittore desidera ricevere eventi

Le sottoscrizioni esistono indipendentemente dagli oggetti della classe di evento. È possibile disabilitare una sottoscrizione impostando la proprietà Enabled su false. Una sottoscrizione disabilitata non viene chiamata dagli eventi COM+.

Di seguito sono riportati i tre tipi di sottoscrizioni:

<dl> <dt>

<span id="Persistent"></span><span id="persistent"></span><span id="PERSISTENT"></span>Persistente
</dt> <dd>

Le sottoscrizioni permanenti si trovano nel catalogo COM+ e sono indipendenti dalla durata del Sottoscrittore. Le sottoscrizioni permanenti rimangono in un riavvio del sistema. In genere, viene creata una sottoscrizione permanente quando un'applicazione viene installata nel computer di un Sottoscrittore e viene rimossa quando l'applicazione viene rimossa. Dopo la creazione di una sottoscrizione permanente, gli eventi COM+ attivano il Sottoscrittore ogni volta che un evento deve essere recapitato.

Quando un server di pubblicazione crea un'istanza ed esegue una chiamata su un oggetto della [classe di evento](the-com--event-class-object.md) , l'oggetto Cerca tutte le sottoscrizioni permanenti nel catalogo com+ e crea una nuova istanza di ogni oggetto. Il processo di creazione può essere diretto o tramite un moniker per i componenti in coda. Specificare l'oggetto Sottoscrittore tramite la proprietà [**SubscriberMoniker**](subscriptionsforcomponent.md) della sottoscrizione. Gli oggetti del Sottoscrittore creati da una sottoscrizione permanente vengono sempre rilasciati dopo ogni chiamata di evento.

</dd> <dt>

<span id="Transient"></span><span id="transient"></span><span id="TRANSIENT"></span>Transitoria
</dt> <dd>

Per le sottoscrizioni temporanee, è possibile usare la raccolta [**TransientSubscriptions**](transientsubscriptions.md) , il cui oggetto padre è l'oggetto Catalogo radice. Le sottoscrizioni temporanee richiedono un evento per un oggetto Sottoscrittore specifico già esistente. Le sottoscrizioni temporanee vengono archiviate nel catalogo COM+, ma la sottoscrizione viene eliminata se il sistema operativo o il sistema operativo viene arrestato. Diversamente dalle sottoscrizioni permanenti, le sottoscrizioni temporanee sono associate a un determinato oggetto e vengono archiviate solo nel sistema di eventi. Le sottoscrizioni temporanee possono essere più efficienti rispetto alle sottoscrizioni persistenti, ma è necessario gestire i cicli di vita degli oggetti. Per informazioni sulla registrazione di una sottoscrizione temporanea, vedere la pagina relativa alla [registrazione di una sottoscrizione temporanea](registering-a-transient-subscription.md).

</dd> <dt>

<span id="Per_user"></span><span id="per_user"></span><span id="PER_USER"></span>Per utente
</dt> <dd>

Le sottoscrizioni per utente possono recapitare gli eventi solo quando il Sottoscrittore è connesso al computer del sistema di eventi. Quando il Sottoscrittore esegue l'accesso, il sistema di eventi Abilita tutte le sottoscrizioni per cui il flag di *lettura* è impostato su **true** e *username* è impostato sul nome dell'utente che ha eseguito l'accesso. Quando il Sottoscrittore si disconnette, le sottoscrizioni vengono disabilitate.

Le sottoscrizioni per utente sono valide solo quando il server di pubblicazione e il Sottoscrittore si trovano nello stesso computer. L'accesso e la disconnessione vengono rilevati solo nel computer del server di pubblicazione, non nel computer in cui risiede l'oggetto Sottoscrittore.

</dd> </dl>

Il sistema di eventi USA i metadati per notificare ai sottoscrittori interessati ogni volta che vengono creati, modificati o rimossi sottoscrizioni o oggetti della classe di evento. Per ricevere i metadati dal sistema di eventi, le applicazioni devono creare una sottoscrizione che risiede nel computer del sistema di eventi e che specifica l'ID dell'interfaccia di generazione (IID \_ IEventObjectChange).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtro di eventi in COM+](filtering-events-in-com-.md)
</dt> <dt>

[Pubblicazione e distribuzione di eventi in COM+](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[Oggetto della classe di evento COM+](the-com--event-class-object.md)
</dt> <dt>

[Uso di eventi COM+ con componenti in coda COM+](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 




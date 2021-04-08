---
description: 'Gli eventi COM+ forniscono due modi per controllare gli eventi che raggiungono i sottoscrittori: filtro del server di pubblicazione e filtro dei parametri.'
ms.assetid: dfc82a57-5587-462d-a43d-516b7d70e25e
title: Filtro di eventi in COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d3a7d152813e4806a9cfb6a342255e0981ecf37
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748863"
---
# <a name="filtering-events-in-com"></a>Filtro di eventi in COM+

Gli eventi COM+ forniscono due modi per controllare gli eventi che raggiungono i sottoscrittori: *filtro del server di pubblicazione* e filtro dei *parametri*.

## <a name="publisher-filtering"></a>Filtro editore

Il filtro dell'editore controlla l'ordine e l'attivazione di un metodo di evento da parte di un oggetto della [classe di evento](the-com--event-class-object.md) . Il filtro dell'editore consente al server di pubblicazione di determinare i Sottoscrittori che ricevono un determinato evento.

Un esempio di utilizzo efficace del filtraggio del server di pubblicazione è quello di uno scambio azionario. La maggior parte dei sottoscrittori vuole scoprire quando viene aggiunta una nuova azione. Tuttavia, molti di questi stessi Sottoscrittori potrebbero non essere in grado di rilevare ogni volta che viene modificato il prezzo azionario. Il filtro dell'editore fornisce la granularità necessaria per recapitare in modo efficace gli eventi ai soli Sottoscrittori che desiderano queste informazioni.

Quando un metodo viene richiamato sull'oggetto della classe di evento di cui è stata creata un'istanza, raccoglie tutti i filtri del server di pubblicazione su tale metodo. Il filtro impone all'oggetto evento di attivare il metodo dell'evento in un Sottoscrittore specifico. Il filtro determina le sottoscrizioni da attivare e l'ordine in cui eseguirle. Ad esempio, il filtro può leggere l'elenco di sottoscrizioni e creare l'ordine in base ad alcuni criteri dell'applicazione e quindi chiamare i sottoscrittori in tale ordine.

Per istruzioni dettagliate sulla creazione di un filtro dell'editore, vedere [creazione di un filtro di pubblicazione](creating-a-publisher-filter.md).

## <a name="parameter-filtering"></a>Filtro parametri

Contrariamente al filtraggio del server di pubblicazione, il servizio eventi COM+ fornisce un filtro facoltativo per i parametri del Sottoscrittore per ogni sottoscrizione e ogni chiamata al metodo di evento. Il filtro dei parametri valuta la proprietà FilterCriteria della sottoscrizione rispetto ai parametri del metodo dell'evento. Questo tipo di filtro viene usato per ogni singolo metodo e per ogni sottoscrizione e fornisce un livello di filtro dei sottoscrittori nell'origine evento. La stringa dei criteri di filtro riconosce gli operatori relazionali per verificare l'uguaglianza (=, = =,!,! =, ~, ~ =,  <>), le parentesi annidate e le parole chiave logiche **and**, **or** o **not**.

Il filtro dei parametri si verifica dopo il filtro del server di pubblicazione e quando viene attivato l'oggetto evento standard per una determinata sottoscrizione. Se viene utilizzato il filtro del server di pubblicazione, il filtro dei parametri si verifica solo quando il filtro del server di pubblicazione richiama [**IFiringControl:: FireSubscription**](/windows/desktop/api/EventSys/nf-eventsys-ifiringcontrol-firesubscription). Per questo motivo, il filtraggio del server di pubblicazione e il filtro dei parametri possono comporre insieme, ma il filtro del server di pubblicazione

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pubblicazione e distribuzione di eventi in COM+](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[Sottoscrizioni](subscriptions.md)
</dt> <dt>

[Oggetto della classe di evento COM+](the-com--event-class-object.md)
</dt> <dt>

[Uso di eventi COM+ con componenti in coda COM+](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 




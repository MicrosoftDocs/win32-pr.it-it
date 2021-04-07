---
description: Per pubblicare un evento, è sufficiente creare un'istanza di un oggetto della classe di evento e richiamare il metodo desiderato; per istruzioni dettagliate su come eseguire questa operazione nel codice, vedere pubblicazione di un evento.
ms.assetid: 835c3753-fdcc-4afe-94c3-c954aaf1c832
title: Pubblicazione e distribuzione di eventi in COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47a444b64501156191590c115d6000f4c0bda153
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748855"
---
# <a name="publishing-and-delivering-events-in-com"></a>Pubblicazione e distribuzione di eventi in COM+

Per pubblicare un evento, è sufficiente creare un'istanza di un oggetto della [classe di evento](the-com--event-class-object.md) e richiamare il metodo desiderato; per istruzioni dettagliate su come eseguire questa operazione nel codice, vedere [pubblicazione di un evento](publishing-an-event.md).

Quando un server di pubblicazione genera un evento, il servizio eventi COM+ Cerca nel database di sottoscrizione tutti i Sottoscrittori che hanno registrato sottoscrizioni alla classe di evento di cui è stata creata un'istanza. Si connette a tali Sottoscrittori (per creazione diretta, moniker o componenti in coda) e chiama il metodo. Per supportare più di una notifica del Sottoscrittore per un evento, i metodi possono contenere solo parametri in e devono restituire solo valori **HRESULT** di esito positivo o negativo.

> [!Note]  
> Questa versione degli eventi COM+ non supporta un archivio eventi distribuito. Un Sottoscrittore deve sottoscrivere un evento in ogni computer da cui vuole ricevere una notifica. In alternativa, è possibile registrare l'oggetto della classe di evento e le sottoscrizioni in un computer centrale e creare un'istanza di questo oggetto classe di evento dai computer remoti in cui vengono pubblicati gli eventi. Il recapito degli eventi viene fornito da DCOM o dal servizio componenti accodati COM+. Per ulteriori informazioni sull'utilizzo del servizio componenti in coda COM+, vedere [utilizzo di eventi com+ con componenti accodati com+](using-com--events-with-com--queued-components.md).

 

Per impostazione predefinita, il servizio eventi COM+ genera gli eventi uno alla volta, in base a un ordine non determinato o ripetibile. Gli editori che devono controllare l'ordine in cui i sottoscrittori ricevono un evento possono implementare un filtro di pubblicazione. Per ulteriori informazioni, vedere [filtro di eventi in com+](filtering-events-in-com-.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtro di eventi in COM+](filtering-events-in-com-.md)
</dt> <dt>

[Sottoscrizioni](subscriptions.md)
</dt> <dt>

[Oggetto della classe di evento COM+](the-com--event-class-object.md)
</dt> <dt>

[Uso di eventi COM+ con componenti in coda COM+](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 




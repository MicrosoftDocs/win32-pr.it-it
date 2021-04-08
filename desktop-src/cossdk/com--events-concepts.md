---
description: Concetti relativi agli eventi COM+
ms.assetid: 6bfe4852-4029-4dd4-92ad-3061618b1b23
title: Concetti relativi agli eventi COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811dbca17c4e90ba5e8c2bcb8c918ce6634487e5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749087"
---
# <a name="com-events-concepts"></a>Concetti relativi agli eventi COM+

Il servizio eventi COM+ è un sistema di *eventi* automatizzato a regime di controllo libero che archivia le informazioni sugli eventi da autori diversi nel catalogo com+. I sottoscrittori possono eseguire una query su questo archivio eventi e selezionare gli eventi per i quali si desiderano sapere.

> [!Note]  
> Un *evento* viene identificato da un metodo in un'interfaccia com+, noto come *metodo di evento*, e viene originato da un server di pubblicazione e inviato al Sottoscrittore o ai sottoscrittori corretti tramite il servizio eventi com+. I metodi di evento devono essere denominati in modo univoco e possono contenere solo parametri di input (nessun output o parametri di input/output). Il valore restituito deve essere un valore **HRESULT**.

 

Il servizio eventi COM+ gestisce la maggior parte della semantica degli eventi per il server di pubblicazione e il Sottoscrittore. Gli editori offrono la pubblicazione di tipi di evento e Sottoscrittori che richiedono tipi di evento dai Publisher. A differenza di un sistema di *eventi strettamente accoppiato* , in cui gli editori devono gestire il sovraccarico della chiamata diretta dei sottoscrittori, il servizio eventi com+ gestisce i dati di sottoscrizione nel catalogo com+, indipendentemente dal server di pubblicazione e dal Sottoscrittore. Questo semplifica il modello di programmazione per il server di pubblicazione e il Sottoscrittore perché il componente del Sottoscrittore COM+ non deve contenere la logica per la compilazione delle sottoscrizioni.

Poiché il ciclo di vita dei dati di sottoscrizione degli eventi COM+ è separato da quello del server di pubblicazione o del Sottoscrittore, le sottoscrizioni possono essere compilate prima che il Sottoscrittore o le applicazioni di pubblicazione siano attive. Ciò significa anche che i Publisher e i sottoscrittori possono essere sviluppati e distribuiti separatamente. Il server di pubblicazione può essere scritto senza conoscere il numero e la posizione dei sottoscrittori. I Sottoscrittori utilizzano il servizio eventi COM+ per trovare il server di pubblicazione e gestirne le sottoscrizioni.

Negli argomenti seguenti di questa sezione vengono fornite informazioni dettagliate sugli elementi principali del servizio eventi COM+ e su come utilizzarli.

-   [Oggetto della classe di evento COM+](the-com--event-class-object.md)
-   [Sottoscrizioni](subscriptions.md)
-   [Pubblicazione e distribuzione di eventi in COM+](publishing-and-delivering-events-in-com-.md)
-   [Filtro di eventi in COM+](filtering-events-in-com-.md)
-   [Uso di eventi COM+ con componenti in coda COM+](using-com--events-with-com--queued-components.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Considerazioni sulla sicurezza degli eventi COM+](com--events-security-considerations.md)
</dt> <dt>

[Attività degli eventi COM+](com--events-tasks.md)
</dt> </dl>

 

 




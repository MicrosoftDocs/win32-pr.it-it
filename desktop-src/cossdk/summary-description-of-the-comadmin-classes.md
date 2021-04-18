---
description: La libreria COMAdmin (comadmin.dll) fornisce tre classi, ciascuna delle quali implementa un'interfaccia COM duale.
ms.assetid: 5a20199f-9d46-4dbe-8e30-2c7ddbde8795
title: Descrizione riepilogativa delle classi COMAdmin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d4a2f54f21f89e9bca644006d50f4eec544565c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304727"
---
# <a name="summary-description-of-the-comadmin-classes"></a>Descrizione riepilogativa delle classi COMAdmin

La libreria COMAdmin (comadmin.dll) fornisce tre classi, ciascuna delle quali implementa un'interfaccia COM duale. Gli oggetti creati da queste classi vengono utilizzati per ottenere l'accesso al catalogo, per rappresentare le raccolte nel catalogo e per rappresentare gli elementi contenuti nelle raccolte.

## <a name="comadmincatalog"></a>COMAdminCatalog

La classe [**COMAdminCatalog**](comadmincatalog.md) rappresenta il catalogo stesso. Un oggetto creato da **COMAdminCatalog** è l'oggetto fondamentale usato nell'amministrazione a livello di codice. Oltre a stabilire la connessione di base al server di catalogo quando ne viene creata un'istanza, **COMAdminCatalog** fornisce metodi che consentono di eseguire le operazioni seguenti:

-   Ottiene le raccolte nel catalogo.
-   Connettersi al server di catalogo in un computer remoto.
-   Installare, esportare, avviare, arrestare e ottenere informazioni sulle applicazioni COM+.
-   Installare i componenti in applicazioni COM+ e ottenere informazioni relative ai componenti.
-   Avviare, arrestare o aggiornare i servizi in esecuzione nel computer.
-   Aggiornare, ripristinare o eseguire il backup delle informazioni del catalogo.

In COM+ 1,0, la classe [**COMAdminCatalog**](comadmincatalog.md) implementa l'interfaccia [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog) . In COM+ 1,5, la classe **COMAdminCatalog** implementa [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) come interfaccia predefinita.

## <a name="comadmincatalogcollection"></a>COMAdminCatalogCollection

La classe [**COMAdminCatalogCollection**](comadmincatalogcollection.md) rappresenta qualsiasi raccolta nel catalogo, fornendo una stringa che assegna un nome alla raccolta specifica in fase di creazione dell'istanza dell'oggetto. Le raccolte di cataloghi disponibili sono denominate nella tabella in [raccolte di amministrazione com+](com--administration-collections.md). Gli oggetti vengono creati da questa classe durante il recupero di una raccolta di livello superiore chiamando il metodo [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) dell'oggetto [**COMAdminCatalog**](comadmincatalog.md) . Questi oggetti vengono creati anche quando si recupera una raccolta figlio chiamando il metodo **GetCollection** dell'oggetto raccolta padre. Gli oggetti **COMAdminCatalogCollection** consentono di eseguire le operazioni seguenti:

-   Enumerare gli elementi contenuti nella raccolta.
-   Recuperare un elemento dalla raccolta.
-   Aggiungere o rimuovere elementi da o verso la raccolta.
-   Salvare o rimuovere tutte le modifiche in sospeso apportate alla raccolta o agli elementi in esso contenuti.
-   Ottenere una raccolta diversa nel catalogo.

La classe [**COMAdminCatalogObject**](comadmincatalogobject.md) implementa l'interfaccia [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) .

## <a name="comadmincatalogobject"></a>COMAdminCatalogObject

La classe [**COMAdminCatalogObject**](comadmincatalogobject.md) rappresenta qualsiasi elemento contenuto in una raccolta. Gli oggetti vengono creati da questa classe quando si recupera un elemento tramite la proprietà [**Item**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) di un oggetto della raccolta di cataloghi. Gli oggetti creati dalla classe **COMAdminCatalogObject** consentono di eseguire le operazioni seguenti:

-   Ottiene o imposta le proprietà supportate dall'elemento che l'oggetto viene utilizzato per rappresentare.
-   Ottenere informazioni sull'elemento e le relative proprietà.

La classe [**COMAdminCatalogObject**](comadmincatalogobject.md) implementa l'interfaccia [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accesso al catalogo COM+](accessing-the-com--catalog.md)
</dt> <dt>

[Panoramica degli oggetti COMAdmin](overview-of-the-comadmin-objects.md)
</dt> </dl>

 

 




---
description: COM+ fornisce un modello a oggetti di amministrazione che espone tutte le funzionalità dello strumento di amministrazione Servizi componenti, ovvero un front-end grafico scritto sopra gli oggetti amministrativi.
ms.assetid: f302eb02-2ef5-42ee-a18f-59f7e60b38df
title: Automazione dell'amministrazione COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0ef3f56da64e442594a7685a77efb9a06e3fe08
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127163"
---
# <a name="automating-com-administration"></a>Automazione dell'amministrazione COM+

COM+ fornisce un modello a oggetti di amministrazione che espone tutte le funzionalità dello strumento di amministrazione Servizi componenti, ovvero un front-end grafico scritto sopra gli oggetti amministrativi. È possibile utilizzare questi oggetti, forniti dalla libreria di amministrazione di Servizi componenti (COMAdmin), per automatizzare tutte le attività nell'amministrazione di applicazioni e servizi COM+.

Gli oggetti COMAdmin consentono di leggere e scrivere le informazioni archiviate nel catalogo COM+, l'archivio dati sottostante che include tutti i dati di configurazione COM+.

È possibile utilizzare questi oggetti per eseguire le operazioni seguenti:

-   Creazione e configurazione di applicazioni COM+.
-   Installare ed esportare applicazioni COM+ esistenti.
-   Gestire le applicazioni COM+ installate.
-   Gestire e configurare i servizi.
-   Amministrare in remoto i servizi componenti in un computer diverso.

È possibile utilizzare gli oggetti COMAdmin consentiti tramite script con qualsiasi linguaggio compatibile con l'automazione, ad esempio Microsoft Visual Basic e Visual Basic script. È possibile sviluppare script leggeri o strumenti di amministrazione per utilizzo generico. Ad esempio, è possibile eseguire quanto le operazioni seguenti:

-   Scrivere script per eseguire attività amministrative di routine.
-   Scrivere script per automatizzare i processi nello sviluppo di applicazioni COM+.
-   Sviluppare strumenti generici per l'amministrazione e il monitoraggio di Servizi componenti.
-   Sviluppare eseguibili di installazione per installare e distribuire l'applicazione COM+.

La libreria COMAdmin fornisce la compatibilità con le versioni precedenti della libreria di amministrazione MTS 2,0. La maggior parte del codice di amministrazione MTS 2,0 esistente continuerà a funzionare, anche se con alcune eccezioni. Vedere la pagina relativa alla [libreria di amministrazione MTS](mts-administration-library.md).

Per automatizzare l'amministrazione, è necessario avere familiarità con le attività amministrative eseguite con lo strumento di amministrazione Servizi componenti.

Per una descrizione completa degli oggetti COMAdmin e delle interfacce corrispondenti, vedere la documentazione di riferimento COM+ per le classi e le interfacce seguenti:

-   [**COMAdminCatalog**](comadmincatalog.md)
-   [**COMAdminCatalogCollection**](comadmincatalogcollection.md)
-   [**COMAdminCatalogObject**](comadmincatalogobject.md)
-   [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)
-   [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)
-   [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection)
-   [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject)

Negli argomenti seguenti di questa sezione viene fornita una panoramica per l'automazione dell'amministrazione utilizzando gli oggetti COMAdmin:

-   [Panoramica degli oggetti COMAdmin](overview-of-the-comadmin-objects.md)
-   [Recupero di raccolte nel catalogo COM+](retrieving-collections-on-the-com--catalog.md)
-   [Impostazione delle proprietà e salvataggio delle modifiche nel catalogo COM+](setting-properties-and-saving-changes-to-the-com--catalog.md)
-   [Gestione degli errori di amministrazione COM+](handling-com--administration-errors.md)
-   [Operazioni di amministrazione COM+ all'interno delle transazioni](com--administration-operations-within-transactions.md)
-   [Esempio introduttivo di utilizzo del catalogo di amministrazione COM+](introductory-example-using-the-com--administration-catalog.md)

 

 




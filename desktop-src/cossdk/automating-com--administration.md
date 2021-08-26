---
description: COM+ fornisce un modello a oggetti di amministrazione che espone tutte le funzionalità dello strumento amministrativo servizi componenti, a sua stessa un front-end grafico scritto sopra gli oggetti amministrativi.
ms.assetid: f302eb02-2ef5-42ee-a18f-59f7e60b38df
title: Automazione dell'amministrazione COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72cb7370c3b1a90324b612108e9ec1ef17c7030d3372d303da74ced95298ab02
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029841"
---
# <a name="automating-com-administration"></a>Automazione dell'amministrazione COM+

COM+ fornisce un modello a oggetti di amministrazione che espone tutte le funzionalità dello strumento amministrativo servizi componenti, a sua stessa un front-end grafico scritto sopra gli oggetti amministrativi. È possibile usare questi oggetti, forniti dalla libreria COMAdmin (Component Services Administration), per automatizzare tutte le attività nell'amministrazione di applicazioni e servizi COM+.

Gli oggetti COMAdmin consentono di leggere e scrivere informazioni archiviate nel catalogo COM+, l'archivio dati sottostante che contiene tutti i dati di configurazione COM+.

È possibile usare questi oggetti per eseguire le operazioni seguenti:

-   Creare e configurare applicazioni COM+.
-   Installare ed esportare applicazioni COM+ esistenti.
-   Gestire le applicazioni COM+ installate.
-   Gestire e configurare i servizi.
-   Amministrare in remoto Servizi componenti in un computer diverso.

È possibile usare gli oggetti COMAdmin con script con qualsiasi linguaggio compatibile con Automazione, ad esempio Microsoft Visual Basic e Visual Basic Script. È possibile sviluppare script leggeri o strumenti di amministrazione per utilizzo generico. Ad esempio, è possibile eseguire quanto le operazioni seguenti:

-   Scrivere script per eseguire attività amministrative di routine.
-   Scrivere script per automatizzare i processi nello sviluppo di applicazioni COM+.
-   Sviluppare strumenti per utilizzo generico per l'amministrazione e il monitoraggio di Servizi componenti.
-   Sviluppare file eseguibili di installazione per installare e distribuire l'applicazione COM+.

La libreria COMAdmin offre la compatibilità con le versioni precedenti della libreria di amministrazione di MTS 2.0. La maggior parte del codice di amministrazione di MTS 2.0 esistente continuerà a funzionare, anche se con alcune eccezioni. Vedere [MTS Administration Library (Libreria di amministrazione MTS).](mts-administration-library.md)

Per automatizzare in modo efficace l'amministrazione, è necessario avere familiarità con le attività di amministrazione eseguite con lo strumento amministrativo Servizi componenti.

Per le descrizioni complete degli oggetti COMAdmin e delle interfacce corrispondenti, vedere la documentazione di riferimento di COM+ per le classi e le interfacce seguenti:

-   [**COMAdminCatalog**](comadmincatalog.md)
-   [**COMAdminCatalogCollection**](comadmincatalogcollection.md)
-   [**COMAdminCatalogObject**](comadmincatalogobject.md)
-   [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)
-   [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)
-   [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection)
-   [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject)

Negli argomenti seguenti di questa sezione viene fornita una panoramica per l'automazione dell'amministrazione tramite gli oggetti COMAdmin:

-   [Panoramica degli oggetti COMAdmin](overview-of-the-comadmin-objects.md)
-   [Recupero di raccolte nel catalogo COM+](retrieving-collections-on-the-com--catalog.md)
-   [Impostazione delle proprietà e salvataggio delle modifiche nel catalogo COM+](setting-properties-and-saving-changes-to-the-com--catalog.md)
-   [Gestione degli errori di amministrazione COM+](handling-com--administration-errors.md)
-   [Operazioni di amministrazione COM+ all'interno delle transazioni](com--administration-operations-within-transactions.md)
-   [Esempio introduttivo sull'uso del catalogo di amministrazione COM+](introductory-example-using-the-com--administration-catalog.md)

 

 




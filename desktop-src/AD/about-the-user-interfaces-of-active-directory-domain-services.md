---
title: Informazioni sulle interfacce utente di Active Directory Domain Services
description: Gli amministratori e gli utenti devono essere in grado di visualizzare e modificare gli oggetti del servizio directory in Microsoft Active Directory Domain Services da un'interfaccia utente.
ms.assetid: b6eec599-ebb3-40af-a4a2-059755285854
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c451a44660aaadbf0021ff57e675736b797d8f3e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046475"
---
# <a name="about-the-user-interfaces-of-active-directory-domain-services"></a>Informazioni sulle interfacce utente di Active Directory Domain Services

Gli amministratori e gli utenti devono essere in grado di visualizzare e modificare gli oggetti del servizio directory in Microsoft Active Directory Domain Services da un'interfaccia utente. Gli amministratori gestiscono il server Active Directory utilizzando diversi snap-in di Microsoft Management Console (MMC), in particolare Active Directory Domain Services utenti e computer, Active Directory Domain Services siti e servizi, Active Directory Domain Services domini e trust e gli snap-in di gestione dello schema di Active Directory Domain Services. L'utente finale, se concesso le autorizzazioni appropriate, può utilizzare anche gli snap-in di MMC Active Directory per visualizzare gli oggetti directory. La shell di Windows può essere utilizzata anche per visualizzare gli oggetti directory. La shell di Windows consente agli utenti di esplorare gli oggetti archiviati nella directory dall'elemento della directory nella rete locale sul desktop o tramite le finestre di dialogo di ricerca disponibili nel menu Start.

Active Directory Domain Services supportano un'interfaccia utente adatta per soddisfare le esigenze degli amministratori e degli utenti finali. Active Directory Domain Services consentono di estendere l'interfaccia utente che rappresenta le classi di oggetti esistenti, nonché le nuove classi aggiunte allo schema. Gli elementi seguenti possono essere utilizzati per controllare o estendere l'interfaccia utente per ogni classe definita nello schema:

-   [Pagine delle proprietà da usare con gli identificatori di visualizzazione](property-pages-for-use-with-display-specifiers.md)
-   [Menu di scelta rapida da usare con gli identificatori di visualizzazione](context-menus-for-use-with-display-specifiers.md)
-   [Nomi visualizzati della classe e dell'attributo](class-and-attribute-display-names.md)
-   [Creazione guidata oggetto](object-creation-wizards.md)
-   [Icone della classe](class-icons.md)
-   [Visualizzazione di contenitori come nodi foglia](viewing-containers-as-leaf-nodes.md)

A partire da Windows 2000, il sistema fornisce oggetti COM che implementano finestre di dialogo comuni per l'utilizzo di oggetti directory. Queste finestre di dialogo forniscono un'interfaccia utente comune senza dover reimplementare queste finestre di dialogo.

-   [Selezione oggetti directory](directory-object-picker.md)
-   [Browser di dominio](domain-browser.md)
-   [Browser contenitore](container-browser.md)

Active Directory gli snap-in amministrativi, i menu di scelta rapida e le pagine delle proprietà possono essere estesi tramite gli snap-in di estensione MMC. È possibile implementare anche altre estensioni MMC, ad esempio blocchi note attività, elementi dello spazio dei nomi, barre di controllo e barre degli strumenti. Per ulteriori informazioni, vedere [estensione degli snap-in di amministrazione Active Directory](/previous-versions/windows/desktop/mmc/extending-the-active-directory-administrative-snap-ins).

 

 
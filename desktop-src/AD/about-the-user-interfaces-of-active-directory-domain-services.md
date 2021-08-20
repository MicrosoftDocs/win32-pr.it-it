---
title: Informazioni sulle interfacce utente di Active Directory Domain Services
description: Gli amministratori e gli utenti devono essere in grado di visualizzare e modificare gli oggetti del servizio directory in Microsoft Active Directory Domain Services da un'interfaccia utente.
ms.assetid: b6eec599-ebb3-40af-a4a2-059755285854
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b22c97cd84fd51cc19a621ae948fceda28f87fda6077a0fcb50eb10b5618ea5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118025751"
---
# <a name="about-the-user-interfaces-of-active-directory-domain-services"></a>Informazioni sulle interfacce utente di Active Directory Domain Services

Gli amministratori e gli utenti devono essere in grado di visualizzare e modificare gli oggetti del servizio directory in Microsoft Active Directory Domain Services da un'interfaccia utente. Gli amministratori gestiscono il server Active Directory usando diversi snap-in di Microsoft Management Console (MMC), in particolare utenti e computer di Active Directory Domain Services, siti e servizi di Active Directory Domain Services, domini e trust di Active Directory Domain Services e snap-in di gestione dello schema Active Directory Domain Services. L'utente finale, se vengono concesse le autorizzazioni appropriate, può anche usare gli snap-in MMC di Active Directory per visualizzare gli oggetti directory. La Windows shell può essere usata anche per visualizzare gli oggetti directory. La shell Windows consente agli utenti di esplorare gli oggetti archiviati nella directory dall'elemento directory in Risorse di rete sul desktop o tramite le finestre di dialogo di ricerca disponibili nel menu Start.

Active Directory Domain Services un'interfaccia utente che si adatta alle esigenze degli amministratori e degli utenti finali. Active Directory Domain Services è possibile estendere l'interfaccia utente che rappresenta le classi di oggetti esistenti e le nuove classi aggiunte allo schema. Gli elementi seguenti possono essere usati per controllare o estendere l'interfaccia utente per ogni classe definita nello schema:

-   [Pagine delle proprietà da usare con identificatori di visualizzazione](property-pages-for-use-with-display-specifiers.md)
-   [Menu di scelta rapida da usare con identificatori di visualizzazione](context-menus-for-use-with-display-specifiers.md)
-   [Nomi visualizzati di classi e attributi](class-and-attribute-display-names.md)
-   [Procedure guidate per la creazione di oggetti](object-creation-wizards.md)
-   [Icone delle classi](class-icons.md)
-   [Visualizzazione di contenitori come nodi foglia](viewing-containers-as-leaf-nodes.md)

A partire da Windows 2000, il sistema fornisce oggetti COM che implementano finestre di dialogo comuni per l'uso di oggetti directory. Queste finestre di dialogo forniscono un'interfaccia utente comune senza dover reimplementare queste finestre di dialogo.

-   [Selezione oggetti directory](directory-object-picker.md)
-   [Browser di dominio](domain-browser.md)
-   [Browser contenitori](container-browser.md)

Gli snap-in amministrativi di Active Directory, i menu di scelta rapida e le pagine delle proprietà possono essere estesi tramite gli snap-in di estensione MMC. È anche possibile implementate altre estensioni MMC, ad esempio riquadri attività, elementi dello spazio dei nomi, barre di controllo e barre degli strumenti. Per altre informazioni, vedere [Estensione degli snap-in amministrativi di Active Directory.](/previous-versions/windows/desktop/mmc/extending-the-active-directory-administrative-snap-ins)

 

 
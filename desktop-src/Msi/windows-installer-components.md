---
description: Un componente è una parte dell'applicazione o del prodotto da installare.
ms.assetid: f1c9696d-3267-44be-a904-ab26250fae2e
title: Componenti Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad90f2fb576d0333a26fc92f9cf951e4da06bab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967783"
---
# <a name="windows-installer-components"></a>Componenti Windows Installer

Un componente è una parte dell'applicazione o del prodotto da installare. Esempi di componenti includono singoli file, un gruppo di file correlati, oggetti COM, registrazione, chiavi del registro di sistema, scelte rapide, risorse, librerie raggruppate in una directory o parti condivise di codice, ad esempio MFC o DAO.

Il servizio del programma di installazione installa o rimuove un componente come singolo elemento coerente. Tiene traccia di ogni componente in base al rispettivo GUID ID componente specificato nella colonna ComponentId della [tabella Component](component-table.md).

> [!Note]  
> Due componenti che condividono lo stesso ID componente vengono considerati come più istanze dello stesso componente indipendentemente dal contenuto effettivo. Nel computer di un utente viene installata una sola istanza di un componente. Diverse funzionalità o applicazioni possono pertanto condividere alcuni componenti.

 

Poiché i componenti sono comunemente condivisi, l'autore di un pacchetto di installazione deve seguire regole rigide quando si specificano i componenti di una funzionalità o di un'applicazione. Questo è essenziale per il corretto funzionamento del Windows Installer meccanismo di conteggio dei riferimenti. Per altre informazioni, vedere [organizzazione di applicazioni in componenti](organizing-applications-into-components.md).

In breve, queste regole sono:

-   Ogni componente deve essere archiviato in un'unica cartella.
-   Nessun file, voce del registro di sistema, collegamento o altre risorse devono essere spediti come membro di più di un componente. Questo vale per i prodotti, le versioni dei prodotti e le società.

Per ulteriori informazioni sull'utilizzo dei componenti di, vedere.

-   [Installazione di un componente mancante](installing-a-missing-component.md)
-   [Installazione di componenti permanenti, file, tipi di carattere, chiavi del registro di sistema](installing-permanent-components-files-fonts-registry-keys.md)
-   [Utilizzo di componenti qualificati](using-qualified-components.md)
-   [Utilizzo di componenti transitivi](using-transitive-components.md)
-   [Utilizzo delle funzionalità e dei componenti](working-with-features-and-components.md)
-   [Creazione di un pacchetto di grandi dimensioni](authoring-a-large-package.md)
-   [Verifica dell'installazione di funzionalità, componenti, file](checking-the-installation-of-features-components-files.md)
-   [Ricerca di una funzionalità o di un componente danneggiato](searching-for-a-broken-feature-or-component.md)
-   [Pubblicazione di prodotti, funzionalità e componenti](publishing-products-features-and-components.md)

 

 




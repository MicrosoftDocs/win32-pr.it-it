---
description: Windows Installer possibile cercare un file o una directory specifica durante un'installazione. Le ricerche di file o directory vengono utilizzate per determinare se un utente ha già installato una versione di un'applicazione.
ms.assetid: a78ca652-c730-4231-80f2-60cf0bad5b02
title: Ricerca di applicazioni, file, voci del registro di sistema o voci di file ini esistenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a41d0ebf8943d1fb82b7c0901a62230e6befdcba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319438"
---
# <a name="searching-for-existing-applications-files-registry-entries-or-ini-file-entries"></a>Ricerca di applicazioni, file, voci del registro di sistema o voci di file ini esistenti

Windows Installer possibile cercare un file o una directory specifica durante un'installazione. Le ricerche di file o directory vengono utilizzate per determinare se un utente ha già installato una versione di un'applicazione.

L' [azione AppSearch](appsearch-action.md) esegue una ricerca in un sistema utente per le firme dei file specificate nella [tabella AppSearch](appsearch-table.md). Se l'azione AppSearch trova un file o una directory installata con la firma specificata, imposta una proprietà corrispondente, anch ' essa specificata nella tabella AppSearch, al percorso del file o della directory. Quando si cerca un file, anche la firma del file deve essere elencata nella [tabella della firma](signature-table.md). Se la firma di un file è elencata nella tabella AppSearch e non è elencata nella tabella della firma, la ricerca Cerca una directory, una voce del registro di sistema o un file ini.

Per velocizzare la ricerca di un computer utente, il programma di installazione esegue una query sulle tabelle del database Locator seguenti nell'ordine indicato per un percorso di ricerca suggerito:

-   Se la firma del file è elencata nella [tabella CompLocator](complocator-table.md), il percorso di ricerca suggerito è il percorso della chiave di un componente. Se la firma non è elencata in questa tabella o non è installata nel percorso suggerito, il programma di installazione esegue una query sulla [tabella RegLocator](reglocator-table.md) per un percorso suggerito.
-   Se la firma del file è elencata nella [tabella RegLocator](reglocator-table.md), il percorso di ricerca suggerito è un percorso chiave scritto nel registro di sistema dell'utente. Se la firma non è elencata in questa tabella o non è installata nel percorso suggerito, il programma di installazione esegue una query sulla [tabella IniLocator](inilocator-table.md) per un percorso suggerito.
-   Se la firma del file è elencata nella [tabella IniLocator](inilocator-table.md), il percorso di ricerca suggerito è un percorso chiave scritto in un file ini presente nella directory Windows predefinita di un sistema utente. Se la firma non è elencata in questa tabella o non è installata nel percorso suggerito, il programma di installazione esegue una query sulla [tabella DrLocator](drlocator-table.md) per un percorso suggerito.
-   Se la firma del file è elencata nella [tabella DrLocator](drlocator-table.md), il percorso di ricerca suggerito è un percorso nella struttura ad albero di directory utente. In questa tabella viene anche specificata la profondità dei livelli di sottodirectory in cui eseguire la ricerca sotto questa posizione.

La prima volta che il programma di installazione individua la firma del file nel percorso suggerito, interrompe la ricerca del file o della directory e imposta la proprietà corrispondente nella [tabella AppSearch](appsearch-table.md). Per altre informazioni, vedere gli argomenti seguenti:

-   [Ricerca in tutte le unità fisse per un file](searching-all-fixed-drives-for-a-file.md)
-   [Ricerca di una directory e di un file nella directory](searching-for-a-directory-and-a-file-in-the-directory.md)
-   [Ricerca di un file e creazione di una proprietà che contiene il percorso del file](searching-for-a-file-and-creating-a-property-holding-the-file-s-path.md)
-   [Ricerca di un file in un percorso specifico](searching-for-a-file-in-a-specific-location.md)
-   [Ricerca di una voce del registro di sistema e creazione di una proprietà contenente il valore del registro di sistema](searching-for-a-registry-entry-and-creating-a-property-holding-the-value-of-the-registry.md)

 

 




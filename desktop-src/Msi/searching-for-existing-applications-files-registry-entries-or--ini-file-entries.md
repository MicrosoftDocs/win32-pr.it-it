---
description: Windows Il programma di installazione può cercare un file o una directory specifica durante un'installazione. Le ricerche di file o directory vengono usate per determinare se un utente ha già installato una versione di un'applicazione.
ms.assetid: a78ca652-c730-4231-80f2-60cf0bad5b02
title: Ricerca di applicazioni, file, voci del Registro di sistema o .ini file esistenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ac9cf4b39f8a46ccd16e83c96ee6ca808b3a1bee32094da480d0226d8bdf283
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041051"
---
# <a name="searching-for-existing-applications-files-registry-entries-or-ini-file-entries"></a>Ricerca di applicazioni, file, voci del Registro di sistema o .ini file esistenti

Windows Il programma di installazione può cercare un file o una directory specifica durante un'installazione. Le ricerche di file o directory vengono usate per determinare se un utente ha già installato una versione di un'applicazione.

[L'azione AppSearch](appsearch-action.md) cerca in un sistema utente le firme dei file specificate nella [tabella AppSearch](appsearch-table.md). Se l'azione AppSearch trova un file o una directory installata con la firma specificata, imposta una proprietà corrispondente, specificata anche nella tabella AppSearch, sul percorso del file o della directory. Quando si cerca un file, la firma del file deve essere elencata anche nella [tabella delle firme](signature-table.md). Se una firma di file è elencata nella tabella AppSearch e non è elencata nella tabella delle firme, la ricerca cerca una directory, una voce del Registro di sistema o una voce .ini file.

Per velocizzare la ricerca di un computer utente, il programma di installazione esegue una query sulle tabelle di database del localizzatore seguenti nell'ordine indicato per una posizione di ricerca suggerita:

-   Se la firma del file è elencata nella [tabella CompLocator](complocator-table.md), il percorso di ricerca suggerito è il percorso chiave di un componente. Se la firma non è elencata in questa tabella o non è installata nel percorso suggerito, il programma di installazione esegue una query sulla tabella [RegLocator](reglocator-table.md) per una posizione suggerita.
-   Se la firma del file è elencata nella tabella [RegLocator](reglocator-table.md), il percorso di ricerca suggerito è un percorso di chiave scritto nel registro utenti. Se la firma non è elencata in questa tabella o non è installata nel percorso suggerito, il programma di installazione esegue una query sulla tabella [IniLocator](inilocator-table.md) per un percorso suggerito.
-   Se la firma del file è elencata nella tabella [IniLocator](inilocator-table.md), il percorso di ricerca suggerito è un percorso chiave scritto in un file .ini presente nella directory Windows predefinita di un sistema utente. Se la firma non è elencata in questa tabella o non è installata nel percorso suggerito, il programma di installazione esegue una query sulla tabella [DrLocator](drlocator-table.md) per una posizione suggerita.
-   Se la firma del file è elencata nella [tabella DrLocator](drlocator-table.md), il percorso di ricerca suggerito è un percorso nell'albero di directory utente. In questa tabella viene specificata anche la profondità dei livelli di sottodirectory in cui eseguire la ricerca al di sotto di questo percorso.

La prima volta che il programma di installazione trova la firma del file in una posizione suggerita, interrompe la ricerca di questo file o directory e imposta la proprietà corrispondente nella [tabella AppSearch](appsearch-table.md). Per altre informazioni, vedere gli argomenti seguenti:

-   [Ricerca di un file in tutte le unità fisse](searching-all-fixed-drives-for-a-file.md)
-   [Ricerca di una directory e di un file nella directory](searching-for-a-directory-and-a-file-in-the-directory.md)
-   [Ricerca di un file e creazione di una proprietà contenente il percorso del file](searching-for-a-file-and-creating-a-property-holding-the-file-s-path.md)
-   [Ricerca di un file in un percorso specifico](searching-for-a-file-in-a-specific-location.md)
-   [Ricerca di una voce del Registro di sistema e creazione di una proprietà contenente il valore del Registro di sistema](searching-for-a-registry-entry-and-creating-a-property-holding-the-value-of-the-registry.md)

 

 




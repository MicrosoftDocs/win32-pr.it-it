---
description: Il gruppo Locator Tables viene utilizzato per individuare i file e le applicazioni.
ms.assetid: 44ab770b-1a7f-4590-9681-8f6bd343bf86
title: Gruppo di tabelle Locator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 300a869a912c06b2112476f50bcda021833cfbe7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314204"
---
# <a name="locator-tables-group"></a>Gruppo di tabelle Locator

Il gruppo Locator Tables viene utilizzato per individuare i file e le applicazioni. Per cercare un file, determinare innanzitutto la firma del file e quindi individuare il file. Le tabelle del localizzatore vengono usate per eseguire ricerche nel registro di sistema, nei dati di configurazione del programma di installazione, nell'albero di directory o nei file ini per la firma univoca di un file. La firma del file può quindi essere archiviata nella [tabella della firma](signature-table.md) per verificare che un determinato file sia effettivamente il file cercato e non un altro file con lo stesso nome. Se un record in una tabella del localizzatore non contiene una chiave nella tabella di firma, il record si riferisce a una directory e non a un file.

Il componente che controlla un file si trova nella tabella dei [file](file-table.md) tramite la chiave esterna per la [tabella dei componenti](component-table.md). Il programma di installazione risolve il percorso di un file tramite la tabella Component perché ogni file appartiene a un componente. Il percorso di un componente viene individuato tramite una chiave esterna nella tabella dei componenti della tabella di [directory](directory-table.md).

Il percorso di un'applicazione viene individuato cercando i file che costituiscono l'applicazione. Il programma di installazione fornisce inoltre due tabelle per la ricerca di versioni precedenti di un'applicazione, ovvero la [tabella AppSearch](appsearch-table.md) e la [tabella CCPSearch](ccpsearch-table.md).

Le tabelle seguenti costituiscono il gruppo Locator Tables e vengono utilizzate per determinare la firma del file.

-   La [tabella RegLocator](reglocator-table.md) include le informazioni necessarie per la ricerca di un file o di una directory nel registro di sistema.
-   La [tabella IniLocator](inilocator-table.md) include le informazioni necessarie per cercare un file ini. Il file ini deve essere presente nella directory predefinita di Microsoft Windows.
-   La [tabella CompLocator](complocator-table.md) include le informazioni necessarie per cercare un file o una directory usando i dati di configurazione del programma di installazione.
-   La [tabella DrLocator](drlocator-table.md) include le informazioni necessarie per la ricerca di un file o di una directory nell'albero di directory.
-   La [tabella AppSearch](appsearch-table.md) contiene le proprietà che devono essere impostate sul risultato della ricerca di una firma del file corrispondente.
-   La [tabella CCPSearch](ccpsearch-table.md) contiene l'elenco delle firme dei file, almeno una delle quali deve essere presente nel computer di un utente per il programma di verifica della conformità (CCP).

 

 




---
description: Il gruppo Tabelle localizzatore viene usato per individuare file e applicazioni.
ms.assetid: 44ab770b-1a7f-4590-9681-8f6bd343bf86
title: Gruppo tabelle localizzatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ad0cf5b2d28d01b6e10cf796dc9653c82feb8ffb63adc57c7a7bc244e7ccfcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629168"
---
# <a name="locator-tables-group"></a>Gruppo tabelle localizzatore

Il gruppo Tabelle localizzatore viene usato per individuare file e applicazioni. Per cercare un file, determinare prima la firma del file e quindi individuare il file. Le tabelle localizzatore vengono usate per cercare la firma univoca di un file nel Registro di sistema, i dati di configurazione del programma di installazione, l'albero della directory o .ini file. La firma del file può [](signature-table.md) quindi essere verificata nella tabella Firma per verificare che un determinato file sia effettivamente il file cercato e non un altro file con lo stesso nome. Se un record in una tabella del localizzatore non contiene una chiave nella tabella Signature, il record fa riferimento a una directory e non a un file.

Il componente che controlla un file si trova nella [tabella File](file-table.md) tramite la chiave esterna alla [tabella Component](component-table.md). Il programma di installazione risolve il percorso di un file tramite la tabella Component perché ogni file appartiene a un componente. La posizione di un componente viene trovata tramite una chiave esterna nella tabella Componente della [tabella Directory](directory-table.md).

Il percorso di un'applicazione viene trovato cercando i file che costituiscono l'applicazione. Il programma di installazione fornisce anche due tabelle per la ricerca di versioni precedenti di un'applicazione: la [tabella AppSearch](appsearch-table.md) e [la tabella CCPSearch](ccpsearch-table.md).

Le tabelle seguenti costituiscono il gruppo Di tabelle localizzatore e vengono usate per determinare la firma del file.

-   La [tabella RegLocator](reglocator-table.md) contiene le informazioni necessarie per cercare un file o una directory nel Registro di sistema.
-   La [tabella IniLocator](inilocator-table.md) contiene le informazioni necessarie per cercare un .ini file. Il .ini file deve essere presente nella directory predefinita di Microsoft Windows.
-   La [tabella CompLocator contiene](complocator-table.md) le informazioni necessarie per cercare un file o una directory usando i dati di configurazione del programma di installazione.
-   La [tabella DrLocator](drlocator-table.md) contiene le informazioni necessarie per cercare un file o una directory nell'albero della directory.
-   La [tabella AppSearch](appsearch-table.md) contiene le proprietà che devono essere impostate sul risultato della ricerca di una firma di file corrispondente.
-   La [tabella CCPSearch](ccpsearch-table.md) contiene l'elenco delle firme di file, almeno una delle quali deve essere presente nel computer di un utente per il programma CCP (Compliance Checking Program).

 

 




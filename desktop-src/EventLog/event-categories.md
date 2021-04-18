---
description: Le categorie consentono di organizzare gli eventi in modo che Visualizzatore eventi possibile filtrarli. Ogni origine evento può definire le proprie categorie numerate e le stringhe di testo a cui viene eseguito il mapping.
ms.assetid: ddba8066-b6b9-42a6-b49f-cbae8f97ef6d
title: Categorie di eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efd84a095754bd51499edf5a21ebea0ade042d75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308374"
---
# <a name="event-categories"></a>Categorie di eventi

Le categorie consentono di organizzare gli eventi in modo che Visualizzatore eventi possibile filtrarli. Ogni [origine evento](event-sources.md) può definire le proprie categorie numerate e le stringhe di testo a cui viene eseguito il mapping.

Le categorie devono essere numerate consecutivamente, a partire dal numero 1. Le categorie stesse sono definite in un file di messaggio. Usare, ad esempio, la sintassi seguente per dichiarare tre categorie di eventi. In Visualizzatore eventi, gli eventi che utilizzano queste categorie avranno la categoria 1, categoria 2 o la categoria 3 visualizzata nella colonna **categoria** .

``` syntax
MessageId=0x1
SymbolicName=CATEGORY_1
Language=English
Category 1
.

MessageId=0x2
SymbolicName=CATEGORY_2
Language=English
Category 2
.

MessageId=0x3
SymbolicName=CATEGORY_3
Language=English
Category 3
.
```

Le categorie possono essere archiviate in un file di messaggi separato o in un file che contiene messaggi di altri tipi. Se si crea un singolo file di messaggio, assicurarsi che le categorie siano i primi messaggi del file. Per altre informazioni sulla creazione e l'uso di file di messaggio, vedere [file di messaggio](message-files.md).

Il numero totale di categorie viene archiviato nel valore **CategoryCount** per l'origine evento.

 

 




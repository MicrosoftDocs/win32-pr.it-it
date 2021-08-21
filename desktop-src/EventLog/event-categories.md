---
description: Le categorie consentono di organizzare gli eventi in modo Visualizzatore eventi filtrarli. Ogni origine evento può definire le proprie categorie numerate e le stringhe di testo a cui sono mappate.
ms.assetid: ddba8066-b6b9-42a6-b49f-cbae8f97ef6d
title: Categorie di eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d68895c1043e12ab8e53e3d6db8cd385d17ccc0175c5610a487682fc1c92c8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151642"
---
# <a name="event-categories"></a>Categorie di eventi

Le categorie consentono di organizzare gli eventi in modo Visualizzatore eventi filtrarli. Ogni [origine evento](event-sources.md) può definire le proprie categorie numerate e le stringhe di testo a cui sono mappate.

Le categorie devono essere numerate consecutivamente, a partire dal numero 1. Le categorie stesse sono definite in un file di messaggio. Ad esempio, usare la sintassi seguente per dichiarare tre categorie di eventi. In Visualizzatore eventi, gli eventi che usano queste categorie avranno Categoria 1, Categoria 2 o Categoria 3 visualizzati nella **colonna** Categoria.

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

Le categorie possono essere archiviate in un file di messaggio separato o in un file contenente messaggi di altri tipi. Se si crea un singolo file di messaggio, assicurarsi che le categorie siano i primi messaggi nel file. Per altre informazioni sulla creazione e sull'uso di file di messaggio, vedere [File di messaggi.](message-files.md)

Il numero totale di categorie viene archiviato nel valore **CategoryCount** per l'origine evento.

 

 




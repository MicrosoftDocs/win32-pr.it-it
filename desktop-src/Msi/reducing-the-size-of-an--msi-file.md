---
description: Gli sviluppatori di pacchetti Windows installer possono notare che i file .msi sono più grandi del previsto dopo modifiche e salvamenti ripetuti.
ms.assetid: d5229ef5-0cb5-4daf-8468-0cb653029c1c
title: Riduzione delle dimensioni di un .msi file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b41cfeb949299ff4d80147fe09437cbfd708a4279bb43189c2528c495eb391
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119534090"
---
# <a name="reducing-the-size-of-an-msi-file"></a>Riduzione delle dimensioni di un .msi file

Gli sviluppatori di pacchetti Windows installer possono notare che i file .msi sono più grandi del previsto dopo modifiche e salvamenti ripetuti. Windows I .msi di installazione sono file compositi che contengono archivi e flussi e presentano alcune delle stesse limitazioni di archiviazione dei file di documento OLE. Se si modifica e si salva lo stesso .msi file più volte, viene creato spazio di archiviazione sprecato nel file. Ciò influisce solo sugli autori .msi file e non ha alcun effetto sugli utenti Windows installer. Gli sviluppatori potrebbero voler rimuovere questo spazio di archiviazione sprecato prima di spedire il file .msi finale.

Per rimuovere lo spazio di archiviazione sprecato e ridurre le dimensioni finali .msi file, sono disponibili le opzioni seguenti.

-   Esportare tutte le tabelle del database in file con estensione idt e quindi importare tali tabelle in un nuovo database. In questo modo si ottiene l'archiviazione più compatta possibile.
-   Usare un'utilità software per compattare lo spazio di archiviazione dei file di documento OLE.

 

 




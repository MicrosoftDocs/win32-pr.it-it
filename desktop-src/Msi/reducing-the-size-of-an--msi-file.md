---
description: Gli sviluppatori di Windows Installer pacchetti possono notare che i file con estensione msi hanno dimensioni maggiori del previsto dopo modifiche e salvataggi ripetuti.
ms.assetid: d5229ef5-0cb5-4daf-8468-0cb653029c1c
title: Riduzione delle dimensioni di un file con estensione msi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b5a19c92f0567fc6081d772279ec2cc0b6cafef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967411"
---
# <a name="reducing-the-size-of-an-msi-file"></a>Riduzione delle dimensioni di un file con estensione msi

Gli sviluppatori di Windows Installer pacchetti possono notare che i file con estensione msi hanno dimensioni maggiori del previsto dopo modifiche e salvataggi ripetuti. Windows Installer file con estensione msi sono file composti che contengono archivi e flussi e presentano alcune delle stesse limitazioni di archiviazione dei file di documento OLE. Se si modifica e si salva lo stesso file con estensione MSI più volte, viene creato uno spazio di archiviazione sprecato nel file. Questa operazione interessa solo gli autori dei file con estensione msi e non ha alcun effetto sugli utenti Windows Installer. Gli sviluppatori potrebbero voler rimuovere lo spazio di archiviazione sprecato prima di spedire il file con estensione msi finale.

Per rimuovere lo spazio di archiviazione sprecato e ridurre la dimensione finale dei file con estensione msi, sono disponibili le opzioni seguenti.

-   Esportare tutte le tabelle del database nei file con estensione IDT e quindi importarli in un nuovo database. Questo consente di ottenere l'archiviazione più compatta possibile.
-   Utilizzare un'utilità software per compattare lo spazio di archiviazione dei file di documento OLE.

 

 




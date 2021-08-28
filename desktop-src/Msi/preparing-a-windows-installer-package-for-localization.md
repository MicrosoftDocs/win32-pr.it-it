---
description: Attenersi a queste linee guida per facilitare la localizzazione dei pacchetti Windows installer.
ms.assetid: f00b44b4-e8ec-46d2-b329-00728a83275b
title: Preparazione di un Windows del programma di installazione per la localizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4e9a1ce06e74197dc8844622861a1f42252deae8b96d3ce57ea852673818de3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129161"
---
# <a name="preparing-a-windows-installer-package-for-localization"></a>Preparazione di un Windows del programma di installazione per la localizzazione

La localizzazione di un pacchetto Windows installer in più lingue può essere notevolmente facilitata eseguendo le operazioni seguenti:

-   Creare un database di installazione di base indipendente dalla tabella codici. Vedere [Creazione di un database con una tabella codici neutra.](creating-a-database-with-a-neutral-code-page.md) La tabella codici del database localizzato può quindi essere impostata importando una tabella di archivio di testo con una tabella codici non neutra nel database di base. Vedere [Impostazione della tabella codici di un database](setting-the-code-page-of-a-database.md).
-   Organizzare i file che richiedono la localizzazione in componenti separati e installarli in directory separate. In questo modo si garantisce che due pacchetti localizzati non installino mai file con nome identico nella stessa directory.

Ad esempio, un'applicazione in tutto il mondo che usa le risorse seguenti può avere tre componenti.



| Componente | Risorsa                   |
|-----------|----------------------------|
| Mondo     | worldwide.exe              |
| Mondo     | voci del Registro di sistema in tutto il mondo |
| Mondo     | collegamento in tutto il mondo         |
| ENG       | engui.dll                  |
| ENG       | readme.txt                 |
| FRA       | fraui.dll                  |
| FRA       | readme.txt                 |



 

I file che devono essere localizzati possono essere installati nei percorsi di directory seguenti:

-   \[ProgramFilesFolder \] \\ World \\worldwide.exe
-   \[ProgramFilesFolder \] \\ World English \\ \\engui.dll
-   \[ProgramFilesFolder \] \\ World English \\ \\readme.txt
-   \[ProgramFilesFolder \] \\ World French \\ \\fraui.dll
-   \[ProgramFilesFolder \] \\ World French \\ \\readme.txt

 

 




---
description: Attenersi a queste linee guida per semplificare la localizzazione dei pacchetti di Windows Installer.
ms.assetid: f00b44b4-e8ec-46d2-b329-00728a83275b
title: Preparazione di un pacchetto di Windows Installer per la localizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa46af5259b880398aa84dc817eb201bd63456eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305631"
---
# <a name="preparing-a-windows-installer-package-for-localization"></a>Preparazione di un pacchetto di Windows Installer per la localizzazione

La localizzazione di un pacchetto di Windows Installer in più lingue può essere molto semplificata seguendo questa procedura:

-   Creare un database di installazione di base indipendente dalla tabella codici. Vedere la [pagina relativa alla creazione di un database con una tabella codici indipendente](creating-a-database-with-a-neutral-code-page.md). La tabella codici del database localizzato può quindi essere impostata importando una tabella di archiviazione di testo con una tabella codici non neutra nel database di base. Vedere [impostazione della tabella codici di un database](setting-the-code-page-of-a-database.md).
-   Organizzare i file che richiedono la localizzazione in componenti separati e installare questi file in directory separate. In questo modo si garantisce che due pacchetti localizzati non installino mai file con nome identico nella stessa directory.

Ad esempio, un'applicazione globale che usa le risorse seguenti può avere tre componenti.



| Componente | Risorsa                   |
|-----------|----------------------------|
| MONDO     | worldwide.exe              |
| MONDO     | voci del registro di sistema nel mondo |
| MONDO     | collegamento globale         |
| ENG       | engui.dll                  |
| ENG       | readme.txt                 |
| FRA       | fraui.dll                  |
| FRA       | readme.txt                 |



 

I file che devono essere localizzati possono essere installati nei seguenti percorsi di directory:

-   \[ProgramFilesFolder \] \\ World \\worldwide.exe
-   \[\] \\ \\engui.dll inglese del mondo ProgramFilesFolder \\
-   \[\] \\ \\readme.txt inglese del mondo ProgramFilesFolder \\
-   \[\] \\ \\fraui.dll francese del mondo ProgramFilesFolder \\
-   \[\] \\ \\readme.txt francese del mondo ProgramFilesFolder \\

 

 




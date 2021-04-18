---
description: Il gruppo di file di tabelle contiene tutte le tabelle di Windows Installer correlate ai file.
ms.assetid: 8f56328e-ed58-41a1-94b6-266e9c117246
title: Gruppo di tabelle file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2667a1b9fe2bd9d2f8260523e2386bf7751dce8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309476"
---
# <a name="file-tables-group"></a>Gruppo di tabelle file

![gruppo di tabelle file](images/filegrp.png)

Per ulteriori informazioni su questo diagramma, vedere la [legenda del diagramma delle relazioni tra entità](entity-relationship-diagram-legend.md).

Uno sviluppatore di pacchetti del programma di installazione deve considerare il popolamento del gruppo di tabelle di file dopo aver suddiviso l'applicazione in [componenti e funzionalità](components-and-features.md) e dopo aver popolato il [gruppo tabelle principali](core-tables-group.md). Il gruppo di tabelle file contiene tutti i file appartenenti all'installazione e la maggior parte di questi file sono elencati nella [tabella file](file-table.md). La [tabella di directory](directory-table.md) non viene mostrata nella figura ma è strettamente correlata al gruppo di tabelle di file. La tabella directory fornisce la struttura di directory dell'installazione.

Il gruppo di file di tabelle contiene tutte le tabelle correlate ai file.

-   La [tabella file](file-table.md) elenca i file appartenenti all'installazione. I file che non sono elencati nella tabella file includono i file su disco, elencati nella tabella media. Poiché ogni file appartiene a un componente, la tabella dei file include una chiave esterna nella tabella dei componenti.
-   La [tabella RemoveFile](removefile-table.md) contiene un elenco di file che devono essere rimossi dall' [azione RemoveFiles](removefiles-action.md).
-   La [tabella dei tipi](font-table.md) di carattere elenca i file dei tipi di carattere da registrare nel sistema.
-   La [tabella SelfReg](selfreg-table.md) elenca i file di modulo dell'installazione che sono autofirmati.
-   La [tabella media](media-table.md) elenca i supporti di origine e i dischi appartenenti all'installazione.
-   La [tabella azione BindImage sul](bindimage-table.md) elenca i file associati alle DLL importate da file eseguibili.
-   La [tabella MoveFile](movefile-table.md) specifica quali file vengono spostati durante l'installazione.
-   La [tabella DuplicateFile](duplicatefile-table.md) specifica quali file vengono duplicati durante l'installazione.
-   La [tabella inifile](inifile-table.md) elenca i file ini e le informazioni che l'applicazione deve impostare nel file.
-   La [tabella RemoveIniFile](removeinifile-table.md) contiene le informazioni che un'applicazione deve eliminare da un file ini.
-   La [tabella Environment](environment-table.md) viene utilizzata per impostare i valori delle variabili di ambiente.
-   Nella [tabella icone](icon-table.md) sono disponibili informazioni sull'icona che vengono copiate in un file come parte dell'annuncio del prodotto.
-   La [tabella FileSFPCatalog](filesfpcatalog-table.md) associa i file specificati ai file del catalogo di protezione dei file di sistema.

    **Windows Vista, Windows Server 2003 e Windows XP:** Non supportato.

-   La [tabella SFPCatalog](sfpcatalog-table.md) contiene cataloghi di protezione dei file di sistema.

    **Windows Vista, Windows Server 2003 e Windows XP:** Non supportato.

-   La [tabella MsiFileHash](msifilehash-table.md) viene utilizzata per archiviare un hash a 128 bit di un file di origine fornito dal pacchetto Windows Installer.

 

 




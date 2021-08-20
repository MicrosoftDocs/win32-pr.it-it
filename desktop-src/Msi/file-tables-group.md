---
description: Il gruppo di file di tabelle contiene tutte le tabelle Windows installer correlate ai file.
ms.assetid: 8f56328e-ed58-41a1-94b6-266e9c117246
title: Gruppo tabelle file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3f8a73aa46b202d184356c14ff12da9ce9ce9880b009418e922b252cc35bc54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142906"
---
# <a name="file-tables-group"></a>Gruppo tabelle file

![gruppo di tabelle file](images/filegrp.png)

Per altre informazioni su questo diagramma, vedere la [legenda del](entity-relationship-diagram-legend.md)diagramma delle relazioni tra entità .

Uno sviluppatore di pacchetti del programma di installazione deve prendere [](components-and-features.md) in considerazione il popolamento del gruppo di tabelle file di tabelle dopo l'interruzione dell'applicazione in componenti e funzionalità e dopo il popolamento del gruppo [di tabelle principali](core-tables-group.md). Il gruppo di tabelle file contiene tutti i file che appartengono all'installazione e la maggior parte di questi file sono elencati nella [tabella File](file-table.md). La [tabella Directory](directory-table.md) non è illustrata nella figura, ma è strettamente correlata al gruppo di tabelle file. La tabella Directory fornisce la struttura di directory dell'installazione.

Il gruppo di file di tabelle contiene tutte le tabelle correlate ai file.

-   Nella [tabella File sono](file-table.md) elencati i file che appartengono all'installazione. I file non elencati nella tabella File includono i file su disco, elencati nella tabella Supporti. Poiché ogni file appartiene a un componente, la tabella File ha una chiave esterna nella tabella Component.
-   La [tabella RemoveFile](removefile-table.md) contiene un elenco di file che devono essere rimossi dall'azione [RemoveFiles](removefiles-action.md).
-   La [tabella Font elenca](font-table.md) i file dei tipi di carattere da registrare con il sistema.
-   La [tabella SelfReg elenca](selfreg-table.md) i file del modulo dell'installazione auto-registrati.
-   Nella [tabella Supporti](media-table.md) sono elencati i supporti di origine e i dischi appartenenti all'installazione.
-   La [tabella BindImage](bindimage-table.md) elenca i file associati alle DLL importate dai file eseguibili.
-   La [tabella MoveFile](movefile-table.md) specifica i file da spostare durante l'installazione.
-   La [tabella DuplicateFile](duplicatefile-table.md) specifica i file duplicati durante l'installazione.
-   La [tabella IniFile](inifile-table.md) elenca i .ini e le informazioni che l'applicazione deve impostare nel file.
-   La [tabella RemoveIniFile](removeinifile-table.md) contiene le informazioni che un'applicazione deve eliminare da .ini file.
-   La [tabella Environment viene](environment-table.md) usata per impostare i valori delle variabili di ambiente.
-   La [tabella Icona fornisce](icon-table.md) informazioni sull'icona copiate in un file come parte dell'annuncio del prodotto.
-   La [tabella FileSFPCatalog](filesfpcatalog-table.md) associa i file specificati ai file del catalogo di protezione file di sistema.

    **Windows Vista, Windows Server 2003 e Windows XP:** Non supportato.

-   La [tabella SFPCatalog contiene](sfpcatalog-table.md) i cataloghi di protezione file di sistema.

    **Windows Vista, Windows Server 2003 e Windows XP:** Non supportato.

-   La [tabella MsiFileHash](msifilehash-table.md) viene usata per archiviare un hash a 128 bit di un file di origine fornito dal pacchetto Windows Installer.

 

 




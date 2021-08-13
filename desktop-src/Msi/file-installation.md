---
description: 'Al termine della determinazione dei costi dei file, il programma di installazione ha tutte le informazioni necessarie per elaborare le due azioni di manipolazione dei file: DuplicateFiles e MoveFiles.'
ms.assetid: 2e6d6eb3-1e71-46e6-a946-d9cc0b209325
title: Installazione di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 005a987a7e61f646f58abd0ec699ce03bd29d85dfa2ddb01e8f693750acda740
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118636699"
---
# <a name="file-installation"></a>Installazione di file

Una [volta completata la determinazione](file-costing.md) dei costi dei file, il programma di installazione ha tutte le informazioni necessarie per elaborare le due azioni di manipolazione dei file: [DuplicateFiles](duplicatefiles-action.md) e [MoveFiles.](movefiles-action.md)

Usare [l'azione DuplicateFiles](duplicatefiles-action.md) per specificare i file che il programma di installazione deve duplicare nella [tabella DuplicateFile](duplicatefile-table.md). Usare [l'azione MoveFiles](movefiles-action.md)per determinare i file da spostare tramite una query sulla [tabella MoveFile](movefile-table.md).

Si noti che il campo Opzioni della [tabella MoveFile](movefile-table.md) specifica se il file originale deve essere eliminato dal percorso corrente. I file spostati o copiati dall'azione MoveFiles non vengono eliminati quando il prodotto viene disinstallato.

[L'azione InstallFiles viene](installfiles-action.md) chiamata dopo il completamento di tutte le altre operazioni di modifica dei file. L'azione InstallFiles elabora la tabella [Media](media-table.md), la tabella [File](file-table.md)e la tabella [Component](component-table.md) per determinare quali file verranno copiati dall'origine alla destinazione.

[L'azione InstallFiles](installfiles-action.md) crea la struttura di directory necessaria per installare tutti i file. Se è necessario installare una cartella vuota in modo esplicito, è possibile chiamare [l'azione CreateFolders](createfolders-action.md) per crearla.

 

 




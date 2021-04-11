---
description: 'Una volta completato il costo del file, il programma di installazione dispone di tutte le informazioni necessarie per elaborare le due azioni di manipolazione dei file: DuplicateFiles e MoveFiles.'
ms.assetid: 2e6d6eb3-1e71-46e6-a946-d9cc0b209325
title: Installazione file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472c58db3dc2e9094a26d57f871359a38930877b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131786"
---
# <a name="file-installation"></a>Installazione file

Una volta completato il [costo del file](file-costing.md) , il programma di installazione dispone di tutte le informazioni necessarie per elaborare le due azioni di manipolazione dei file: [DuplicateFiles](duplicatefiles-action.md) e [MoveFiles](movefiles-action.md).

Usare l' [azione DuplicateFiles](duplicatefiles-action.md) per specificare i file che il programma di installazione deve duplicare nella [tabella DuplicateFile](duplicatefile-table.md). Usare l' [azione MoveFiles](movefiles-action.md)per determinare i file da spostare eseguendo una query sulla [tabella MoveFile](movefile-table.md).

Si noti che il campo Options della [tabella MoveFile](movefile-table.md) specifica se il file originale deve essere eliminato dal percorso corrente. I file che vengono spostati o copiati dall'azione MoveFiles non vengono eliminati quando il prodotto viene disinstallato.

L' [azione InstallFiles](installfiles-action.md) viene chiamata dopo che tutte le altre operazioni di manipolazione dei file sono state completate. L'azione InstallFiles elabora la [tabella dei supporti](media-table.md), la [tabella dei file](file-table.md)e la tabella dei [componenti](component-table.md) per determinare quali file verranno copiati dall'origine alla destinazione.

L' [azione InstallFiles](installfiles-action.md) crea la struttura di directory necessaria per installare tutti i file. Se è necessario installare una cartella vuota in modo esplicito, è possibile chiamare l' [azione CreateFolders](createfolders-action.md) per crearla.

 

 




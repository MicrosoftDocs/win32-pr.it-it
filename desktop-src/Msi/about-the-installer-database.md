---
description: Il database Windows Installer è costituito da molte tabelle intercorrelate che insieme costituiscono un database relazionale delle informazioni necessarie per installare un gruppo di applicazioni.
ms.assetid: 3352dd8f-c082-4c4b-98be-5823c8b28f07
title: Informazioni sul database del programma di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7f0ee2cc326f85d964ac3d845b97751a48fbb91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881178"
---
# <a name="about-the-installer-database"></a>Informazioni sul database del programma di installazione

Il database Windows Installer è costituito da molte tabelle intercorrelate che insieme costituiscono un database relazionale delle informazioni necessarie per installare un gruppo di applicazioni. Poiché il database è relazionale, le tabelle vengono collegate tramite i dati nei valori di chiave primaria ed esterna. Questo fornisce un metodo efficiente per modificare il processo di installazione e significa che gli utenti possono personalizzare più facilmente un'applicazione o un gruppo di applicazioni di grandi dimensioni. Le tabelle di database riflettono il layout generale dell'intero gruppo di applicazioni, tra cui:

-   Funzionalità disponibili
-   Componenti
-   Relazione tra funzionalità e componenti
-   Impostazioni del registro di sistema necessarie
-   Interfaccia utente per l'applicazione

Per creare un database di installazione, è necessario compilare le tabelle con tutte le informazioni sulle applicazioni e il processo di installazione. La creazione manuale di tutte queste tabelle diventa un'attività di grandi dimensioni anche per un'installazione con dimensioni moderate; di conseguenza, alcuni strumenti di terze parti sono disponibili per facilitare la compilazione del database del programma di installazione. Nelle sezioni seguenti vengono descritti i gruppi di tabelle di database correlate.

[Gruppo di tabelle Core](core-tables-group.md)

[Gruppo di tabelle file](file-tables-group.md)

[Gruppo di tabelle del registro di sistema](registry-tables-group.md)

[Gruppo tabelle di sistema](system-tables-group.md)

[Gruppo di tabelle Locator](locator-tables-group.md)

[Gruppo tabelle informazioni sul programma](program-information-tables-group.md)

[Gruppo tabelle procedure di installazione](installation-procedure-tables-group.md)

[Legenda diagramma delle relazioni tra entità](entity-relationship-diagram-legend.md)

[File di archivio di testo](text-archive-files.md)

Per un elenco completo di tutte le tabelle in un database di installazione, vedere [tabelle di database](database-tables.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Versioni rilasciate, strumenti e ridistribuibili](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 




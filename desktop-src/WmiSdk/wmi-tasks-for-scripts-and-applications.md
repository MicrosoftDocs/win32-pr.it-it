---
description: Viene descritto come trovare la classe WMI corretta e le procedure da usare negli script e nelle applicazioni che eseguono attività comuni di amministrazione di computer e di rete.
ms.assetid: fe15b67c-8ae6-4360-a2ee-1eda292dd05a
ms.tgt_platform: multiple
title: Attività WMI per script e applicazioni
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d273db41b832b8141fe13bdf0538b51fb221688949792e214c9f81c1e7b96e69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118553125"
---
# <a name="wmi-tasks-for-scripts-and-applications"></a>Attività WMI per script e applicazioni

Le sezioni seguenti descrivono varie attività di amministrazione di computer e di rete e forniscono collegamenti alla classe o alle classi WMI usate per eseguire tali attività. Per altre informazioni, vedere [Creazione di un'applicazione WMI o di uno script](creating-a-wmi-application-or-script.md). Per altre informazioni sull'uso di WMI, vedere [Altre informazioni](further-information.md). Per altre informazioni sull'uso di WMI, vedere [TechNet ScriptCenter.](https://www.microsoft.com/technet/scriptcenter/default.mspx) Queste risorse potrebbero non essere disponibili in ogni lingua o paese/area geografica.

Per altre informazioni su come fornire dati a WMI, vedere Uso di [WMI](using-wmi.md), che farà riferimento ad argomenti sulla scrittura di un [*provider*](gloss-p.md)WMI.

Le operazioni illustrate negli esempi di script possono essere eseguite dalle applicazioni in C++ o Visual Basic. Per altre informazioni, vedere [Creazione di un'applicazione WMI con C++](creating-a-wmi-application-using-c-.md) e Esempi di applicazioni [C++ WMI](wmi-c---application-examples.md).

Nella tabella seguente sono elencate le categorie di attività.



| Categorie attività                                                               | Descrizione                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Account e domini](wmi-tasks--accounts-and-domains.md)                   | Ottenere informazioni come il dominio del computer o l'utente attualmente connesso. Molte attività correlate al dominio o all'account vengono eseguite in modo ottimale con [gli script ADSI.](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) Per esempi, vedere TechNet ScriptCenter all'indirizzo [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) . |
| [Hardware computer](wmi-tasks--computer-hardware.md)                         | Ottenere informazioni sulla presenza, lo stato o le proprietà dei componenti hardware. Ad esempio, è possibile determinare se un computer è un desktop o un portatile.                                                                                                                                                                                             |
| [Computer Software](wmi-tasks--computer-software.md)                         | Ottenere informazioni quali il software installato dal programma di installazione Windows (MSI) e le versioni del software.                                                                                                                                                                                                                                              |
| [Connessione al servizio WMI](wmi-tasks--connecting-to-the-wmi-service.md) | Per ottenere dati da WMI, nel computer locale o da un computer remoto, è necessario connettersi al servizio WMI connettendosi a uno spazio dei nomi [*specifico.*](gloss-n.md) Nella maggior parte dei casi, usare la connessione [del moniker](creating-a-wmi-script.md) abbreviato o la connessione [**del localizzatore.**](swbemlocator-connectserver.md)    |
| [Date e ore](wmi-tasks--dates-and-times.md)                             | Sono disponibili classi WMI e un oggetto di scripting per analizzare o convertire il [formato datetime CIM.](date-and-time-format.md)                                                                                                                                                                                                                                     |
| [Gestione desktop](wmi-tasks--desktop-management.md)                       | Ottenere dati da desktop remoti o controllarne il controllo. Ad esempio, è possibile determinare se lo screensaver richiede o meno una password. WMI offre anche la possibilità di arrestare un computer remoto.                                                                                                                                                               |
| [Dischi e file system](wmi-tasks--disks-and-file-systems.md)               | Ottenere informazioni sullo stato hardware dell'unità disco, sui volumi logici.                                                                                                                                                                                                                                                                                      |
| [Log eventi](wmi-tasks--event-logs.md)                                       | Ottenere i dati degli eventi dai file di registro eventi nt ed eseguire operazioni come il backup o la cancellazione dei file di log.                                                                                                                                                                                                                                                   |
| [File e cartelle](wmi-tasks--files-and-folders.md)                         | Modificare le proprietà di file o cartelle tramite WMI, inclusa la creazione di una condivisione o la ridenominazione di un file.                                                                                                                                                                                                                                                              |
| [Rete](wmi-tasks--networking.md)                                       | Gestire e ottenere informazioni su connessioni e indirizzi IP o MAC.                                                                                                                                                                                                                                                                                  |
| [Sistemi operativi](wmi-tasks--operating-systems.md)                         | Ottenere informazioni sul sistema operativo, ad esempio la versione, se è attivato o quali hotfix sono installati.                                                                                                                                                                                                                                  |
| [Monitoraggio delle prestazioni](wmi-tasks--performance-monitoring.md)               | Usare le classi WMI che ottengono dati dai contatori delle prestazioni per accedere e aggiornare i dati sulle prestazioni del computer.                                                                                                                                                                                                                                     |
| [Processi](wmi-tasks--processes.md)                                         | Ottenere informazioni, ad esempio l'account con cui è in esecuzione un processo. È possibile eseguire azioni come la creazione di processi.                                                                                                                                                                                                                                 |
| [Stampanti e stampa](wmi-tasks--printers-and-printing.md)                 | Gestire e ottenere dati sulle stampanti, ad esempio trovare o impostare la stampante predefinita.                                                                                                                                                                                                                                                                    |
| [Registro](wmi-tasks--registry.md)                                           | Creare e modificare chiavi e valori del Registro di sistema.                                                                                                                                                                                                                                                                                                               |
| [Attività pianificate](wmi-tasks--scheduled-tasks.md)                             | Creare e ottenere informazioni sulle attività pianificate.                                                                                                                                                                                                                                                                                                         |
| [Services](wmi-tasks--services.md)                                           | Ottenere informazioni sui servizi, inclusi i servizi dipendenti o antecedent.                                                                                                                                                                                                                                                                            |



 

 

 

---
description: Viene descritto come trovare la classe e le procedure WMI corrette da utilizzare negli script e nelle applicazioni che eseguono attività comuni di amministrazione di computer e reti.
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
ms.openlocfilehash: e2a18791f5055a7574b9e130cf10c0cd1246f6eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528597"
---
# <a name="wmi-tasks-for-scripts-and-applications"></a>Attività WMI per script e applicazioni

Le sezioni seguenti descrivono varie attività di amministrazione di computer e di rete e forniscono collegamenti alla classe o alle classi WMI usate per eseguire tali attività. Per ulteriori informazioni, vedere [creazione di un'applicazione o di uno script WMI](creating-a-wmi-application-or-script.md). Per ulteriori informazioni sull'utilizzo di WMI, vedere [ulteriori informazioni](further-information.md). Per ulteriori informazioni sull'utilizzo di WMI, vedere [TechNet ScriptCenter](https://www.microsoft.com/technet/scriptcenter/default.mspx). Queste risorse potrebbero non essere disponibili in tutte le lingue o paesi.

Per ulteriori informazioni su come fornire dati a WMI, vedere [utilizzo di WMI](using-wmi.md), che consente di fare riferimento agli argomenti relativi alla scrittura di un [*provider*](gloss-p.md)WMI.

Le operazioni illustrate negli esempi di script possono essere eseguite da applicazioni in C++ o Visual Basic. Per ulteriori informazioni, vedere la pagina relativa alla [creazione di un'applicazione WMI utilizzando](creating-a-wmi-application-using-c-.md) gli esempi di applicazioni C++ e [WMI c++](wmi-c---application-examples.md).

Nella tabella seguente sono elencate le categorie di attività.



| Categorie attività                                                               | Descrizione                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Account e domini](wmi-tasks--accounts-and-domains.md)                   | Ottenere informazioni come il dominio del computer o l'utente attualmente connesso. Molte attività relative a dominio o account vengono eseguite in modo ottimale con gli script [ADSI](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) . Per esempi, vedere il sito TechNet ScriptCenter all'indirizzo [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) . |
| [Hardware computer](wmi-tasks--computer-hardware.md)                         | Ottenere informazioni sulla presenza, lo stato o le proprietà dei componenti hardware. Ad esempio, è possibile determinare se un computer è un computer desktop o portatile.                                                                                                                                                                                             |
| [Software per computer](wmi-tasks--computer-software.md)                         | Ottenere informazioni quali il software installato dalle versioni del Windows Installer (MSI) e del software.                                                                                                                                                                                                                                              |
| [Connessione al servizio WMI](wmi-tasks--connecting-to-the-wmi-service.md) | Per ottenere dati da WMI, sia nel computer locale che in un computer remoto, è necessario connettersi al servizio WMI connettendosi a uno [*spazio dei nomi*](gloss-n.md)specifico. Nella maggior parte dei casi, usare la connessione del [moniker](creating-a-wmi-script.md) abbreviato o la connessione del [**localizzatore**](swbemlocator-connectserver.md) .    |
| [Date e ore](wmi-tasks--dates-and-times.md)                             | Sono disponibili classi WMI e un oggetto di script per analizzare o convertire il formato [DateTime CIM](date-and-time-format.md) .                                                                                                                                                                                                                                     |
| [Gestione desktop](wmi-tasks--desktop-management.md)                       | Ottenere i dati da o controllare i desktop remoti. Ad esempio, è possibile determinare se lo screensaver richiede una password. WMI offre inoltre la possibilità di arrestare un computer remoto.                                                                                                                                                               |
| [Dischi e file System](wmi-tasks--disks-and-file-systems.md)               | Ottenere informazioni sullo stato dell'hardware dell'unità disco e sui volumi logici.                                                                                                                                                                                                                                                                                      |
| [Log eventi](wmi-tasks--event-logs.md)                                       | Ottenere i dati degli eventi dai file del registro eventi NT ed eseguire operazioni come il backup o la cancellazione dei file di log.                                                                                                                                                                                                                                                   |
| [File e cartelle](wmi-tasks--files-and-folders.md)                         | Modificare le proprietà del file o della cartella tramite WMI, inclusa la creazione di una condivisione o la ridenominazione di un file.                                                                                                                                                                                                                                                              |
| [Funzionalità di rete](wmi-tasks--networking.md)                                       | Consente di gestire e ottenere informazioni sulle connessioni e sugli indirizzi IP o MAC.                                                                                                                                                                                                                                                                                  |
| [Sistemi operativi](wmi-tasks--operating-systems.md)                         | Ottenere informazioni sul sistema operativo, ad esempio la versione, se è attivata o quali hotfix sono installati.                                                                                                                                                                                                                                  |
| [Monitoraggio delle prestazioni](wmi-tasks--performance-monitoring.md)               | Utilizzare le classi WMI che ottengono dati dai contatori delle prestazioni per accedere e aggiornare i dati sulle prestazioni del computer.                                                                                                                                                                                                                                     |
| [Processi](wmi-tasks--processes.md)                                         | Ottenere informazioni, ad esempio l'account con cui viene eseguito un processo. È possibile eseguire azioni come la creazione di processi.                                                                                                                                                                                                                                 |
| [Stampanti e stampa](wmi-tasks--printers-and-printing.md)                 | Gestire e ottenere dati sulle stampanti, ad esempio la ricerca o l'impostazione della stampante predefinita.                                                                                                                                                                                                                                                                    |
| [Registro](wmi-tasks--registry.md)                                           | Creare e modificare le chiavi e i valori del registro di sistema.                                                                                                                                                                                                                                                                                                               |
| [Attività pianificate](wmi-tasks--scheduled-tasks.md)                             | Creare e ottenere informazioni sulle attività pianificate.                                                                                                                                                                                                                                                                                                         |
| [Services](wmi-tasks--services.md)                                           | Ottenere informazioni sui servizi, inclusi i servizi dipendenti o precedenti.                                                                                                                                                                                                                                                                            |



 

 

 

---
description: Nell'infrastruttura WMI, il servizio WMI (Winmgmt) è il componente del sistema operativo che funge da Mediator tra le applicazioni di gestione e i provider di dati WMI. Il repository WMI è un'area di archiviazione per i dati statici correlati a WMI.
ms.assetid: 6ef157be-fb75-4453-bc20-4568a3dc18c0
ms.tgt_platform: multiple
title: Infrastruttura WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4370af9ec062ffa845d54eafda054357a76dc07c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310336"
---
# <a name="wmi-infrastructure"></a>Infrastruttura WMI

Nell'infrastruttura WMI, il servizio WMI (Winmgmt) è il componente del sistema operativo che funge da Mediator tra le applicazioni di gestione e i [*provider*](gloss-p.md)di dati WMI. Il [*repository WMI*](gloss-w.md) è un'area di archiviazione per i dati statici correlati a WMI.

Il servizio WMI viene implementato come processo del servizio all'interno di un processo host del servizio condiviso (SVCHOST). Per altre informazioni, vedere [hosting e sicurezza del provider](provider-hosting-and-security.md).

Il servizio WMI viene avviato quando il primo script o un'applicazione di gestione effettua una chiamata per connettersi a uno spazio dei nomi WMI. A seconda della configurazione, il servizio WMI potrebbe arrestarsi o passare a un profilo di memoria insufficiente quando non viene chiamato da un'applicazione di gestione.

Il servizio WMI interagisce con le applicazioni di gestione tramite l'interfaccia COM. Quando un'applicazione effettua una richiesta tramite l'interfaccia, WMI determina se la richiesta è per i dati statici o dinamici. Se la richiesta prevede dati statici, ad esempio il nome di un oggetto gestito, WMI recupera i dati dal repository. Se la richiesta prevede dati dinamici, ad esempio la quantità di memoria attualmente utilizzata da un oggetto gestito, WMI passa la richiesta a un provider.

I provider registrano il proprio percorso con il servizio WMI, che consente a WMI di instradare le richieste di dati. Un provider registra anche il supporto per operazioni specifiche, ad esempio il recupero dei dati, la modifica, l'eliminazione, l'enumerazione o l'elaborazione delle query. Il servizio WMI utilizza le informazioni di registrazione del provider per soddisfare le richieste dell'applicazione con il provider appropriato. WMI utilizza inoltre le informazioni di registrazione per caricare e scaricare i provider, a seconda delle esigenze. Al termine dell'elaborazione di una richiesta da parte di un provider, il provider restituisce il risultato al servizio WMI. WMI quindi trasmette il risultato all'applicazione tramite l'interfaccia COM. Per ulteriori informazioni, vedere la pagina relativa [alla fornitura di dati a WMI](providing-data-to-wmi.md).

WMI utilizza la [traccia eventi](/windows/desktop/ETW/event-tracing-portal) (ETW) per registrare l'attività del servizio WMI.

Poiché l'infrastruttura gestisce tutto il traffico tra i provider e le applicazioni di gestione, l'infrastruttura fornisce le funzionalità seguenti:

-   Supporto delle notifiche degli eventi

    Per ulteriori informazioni, vedere [monitoraggio degli eventi](monitoring-events.md).

-   Supporto del linguaggio di query

    Per ulteriori informazioni, vedere [esecuzione di query con WQL](querying-with-wql.md).

-   Supporto per la sicurezza

    Per ulteriori informazioni, vedere [gestione della sicurezza WMI](maintaining-wmi-security.md).

-   Creazione di script per l'accesso ai dati dei contatori delle prestazioni

    Per ulteriori informazioni, vedere [monitoraggio dei dati sulle prestazioni](monitoring-performance-data.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Architettura WMI](wmi-architecture.md)
</dt> </dl>

 

 

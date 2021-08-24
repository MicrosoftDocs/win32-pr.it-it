---
description: Nell'infrastruttura WMI, il servizio WMI (Winmgmt) è il componente del sistema operativo che funge da mediatore tra le applicazioni di gestione e i provider di dati WMI. Il repository WMI è un'area di archiviazione per i dati statici correlati a WMI.
ms.assetid: 6ef157be-fb75-4453-bc20-4568a3dc18c0
ms.tgt_platform: multiple
title: Infrastruttura WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2bc4492c7d26f422705863609a2e0ec19af5eb930e0aa80f4fd8bb8c26bea4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757331"
---
# <a name="wmi-infrastructure"></a>Infrastruttura WMI

Nell'infrastruttura WMI, il servizio WMI (Winmgmt) è il componente del sistema operativo che funge da mediatore tra le applicazioni di gestione e i provider [*di*](gloss-p.md)dati WMI. Il [*repository WMI è*](gloss-w.md) un'area di archiviazione per i dati statici correlati a WMI.

Il servizio WMI viene implementato come processo del servizio all'interno di un processo host del servizio condiviso (SVCHOST). Per altre informazioni, vedere [Hosting e sicurezza del provider.](provider-hosting-and-security.md)

Il servizio WMI viene avviato quando il primo script o applicazione di gestione effettua una chiamata per connettersi a uno spazio dei nomi WMI. A seconda dell'installazione, il servizio WMI può arrestarsi o passare a un profilo di memoria insufficiente quando non viene chiamato da un'applicazione di gestione.

Il servizio WMI interagisce con le applicazioni di gestione tramite l'interfaccia COM. Quando un'applicazione effettua una richiesta tramite l'interfaccia , WMI determina se la richiesta è per dati statici o dinamici. Se la richiesta include dati statici, ad esempio il nome di un oggetto gestito, WMI recupera i dati dal repository. Se la richiesta include dati dinamici, ad esempio la quantità di memoria attualmente in uso in un oggetto gestito, WMI passa la richiesta a un provider.

I provider registrano la propria posizione con il servizio WMI, che consente a WMI di instradare le richieste di dati. Un provider registra anche il supporto per operazioni specifiche, ad esempio il recupero, la modifica, l'eliminazione, l'enumerazione o l'elaborazione di query. Il servizio WMI utilizza le informazioni di registrazione del provider per associare le richieste dell'applicazione al provider appropriato. WMI usa inoltre le informazioni di registrazione per caricare e scaricare i provider, se necessario. Quando un provider termina l'elaborazione di una richiesta, il provider restituisce il risultato al servizio WMI. WMI inoltra quindi il risultato all'applicazione tramite l'interfaccia COM. Per altre informazioni, vedere [Fornire dati a WMI.](providing-data-to-wmi.md)

WMI usa [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) per registrare l'attività del servizio WMI.

Poiché l'infrastruttura gestisce tutto il traffico tra i provider e le applicazioni di gestione, l'infrastruttura offre le funzionalità seguenti:

-   Supporto per le notifiche degli eventi

    Per altre informazioni, vedere [Monitoring Events](monitoring-events.md).

-   Supporto del linguaggio di query

    Per altre informazioni, vedere [Esecuzione di query con WQL.](querying-with-wql.md)

-   Supporto per la sicurezza

    Per altre informazioni, vedere [Gestione della sicurezza WMI.](maintaining-wmi-security.md)

-   Scripting dell'accesso ai dati dei contatori delle prestazioni

    Per altre informazioni, vedere Monitoraggio [dei dati sulle prestazioni.](monitoring-performance-data.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Architettura WMI](wmi-architecture.md)
</dt> </dl>

 

 

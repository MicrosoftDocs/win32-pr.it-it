---
description: WMI usa Event Tracing (ETW) e gli eventi possono essere ottenuti tramite l Visualizzatore eventi utente o lo strumento da riga di comando Wevtutil. Per altre informazioni, vedere Traccia dell'attività WMI.
ms.assetid: 315b8355-03b9-40f9-a6c1-29a49f5a2cd8
ms.tgt_platform: multiple
title: File di log WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fff9064dd82484568282f649b3380f544d9ba58a569e36583664806d47b5e9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739428"
---
# <a name="wmi-log-files"></a>File di log WMI

WMI usa [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) e  gli eventi possono essere ottenuti tramite l Visualizzatore eventi intervallo utente o lo strumento da riga di comando Wevtutil. Per altre informazioni, vedere [Traccia dell'attività WMI.](tracing-wmi-activity.md)

-   [Traccia eventi anziché log di testo](#event-tracing-instead-of-text-logs)
-   [File di log WMI](#wmi-log-files)
-   [Argomenti correlati](#related-topics)

## <a name="event-tracing-instead-of-text-logs"></a>Traccia eventi anziché log di testo

L'attività del servizio WMI viene registrata nel file WMITracing.log. Per altre informazioni sull'abilitazione della traccia eventi WMI e sull'accesso al file WMITracing.log, vedere [Tracing WMI Activity](tracing-wmi-activity.md). Windows I provider del modello di driver (WDM) continuano a registrare nel file Wbemprov.log.

## <a name="wmi-log-files"></a>File di log WMI

Il servizio WMI e alcuni provider scrivono file di log di testo per registrare gli eventi.

<dl> <dt>

<span id="WMI_Provider_Log_Files"></span><span id="wmi_provider_log_files"></span><span id="WMI_PROVIDER_LOG_FILES"></span>[File di log del provider WMI](wmi-provider-log-files.md)
</dt> <dd>

I provider WMI possono anche gestire i log. I file di log visualizzati in un sistema dipendono dai provider installati.

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su WMI](wmi-reference.md)
</dt> <dt>

[Traccia dell'attività WMI](tracing-wmi-activity.md)
</dt> <dt>

[Registrazione dell'attività WMI](logging-wmi-activity.md)
</dt> </dl>

 

 

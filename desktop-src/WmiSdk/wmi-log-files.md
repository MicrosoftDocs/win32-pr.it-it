---
description: WMI utilizza traccia eventi (ETW) ed è possibile ottenere gli eventi tramite l'interfaccia utente Visualizzatore eventi o lo strumento da riga di comando wevtutil. Per ulteriori informazioni, vedere traccia dell'attività WMI.
ms.assetid: 315b8355-03b9-40f9-a6c1-29a49f5a2cd8
ms.tgt_platform: multiple
title: File di log WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a51dfe4efbec32e60812980511676f723fd5aee9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309749"
---
# <a name="wmi-log-files"></a>File di log WMI

WMI utilizza [traccia eventi](/windows/desktop/ETW/event-tracing-portal) (ETW) ed è possibile ottenere gli eventi tramite l'interfaccia utente **Visualizzatore eventi** o lo strumento da riga di comando wevtutil. Per ulteriori informazioni, vedere [traccia dell'attività WMI](tracing-wmi-activity.md).

-   [Traccia eventi anziché log di testo](#event-tracing-instead-of-text-logs)
-   [File di log WMI](#wmi-log-files)
-   [Argomenti correlati](#related-topics)

## <a name="event-tracing-instead-of-text-logs"></a>Traccia eventi anziché log di testo

L'attività del servizio WMI viene registrata nel file WMITracing. log. Per ulteriori informazioni sull'abilitazione della traccia eventi WMI e sull'accesso al file WMITracing. log, vedere [traccia dell'attività WMI](tracing-wmi-activity.md). I provider Windows Driver Model (WDM) continuano ad accedere al file Wbemprov. log.

## <a name="wmi-log-files"></a>File di log WMI

Il servizio WMI e alcuni provider scrivono file di log di testo per registrare gli eventi.

<dl> <dt>

<span id="WMI_Provider_Log_Files"></span><span id="wmi_provider_log_files"></span><span id="WMI_PROVIDER_LOG_FILES"></span>[File di log del provider WMI](wmi-provider-log-files.md)
</dt> <dd>

Anche i provider WMI possono gestire i log. I file di log visualizzati in un sistema dipendono dai provider installati.

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su WMI](wmi-reference.md)
</dt> <dt>

[Traccia dell'attività WMI](tracing-wmi-activity.md)
</dt> <dt>

[Registrazione dell'attività WMI](logging-wmi-activity.md)
</dt> </dl>

 

 

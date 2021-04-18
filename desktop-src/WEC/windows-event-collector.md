---
title: Raccolta eventi Windows
description: È possibile sottoscrivere la ricezione e l'archiviazione di eventi in un computer locale (agente di raccolta eventi) che vengono trasmessi da un computer remoto (origine evento).
ms.assetid: 7725e06d-4df1-4b3e-9f2f-2b8bdd805cb6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c4ef9e0cb647236daa55771222f25b7e0e370ef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299894"
---
# <a name="windows-event-collector"></a>Raccolta eventi Windows

È possibile sottoscrivere la ricezione e l'archiviazione di eventi in un computer locale (agente di raccolta eventi) che vengono trasmessi da un computer remoto (origine evento). Le [funzioni dell'agente di raccolta eventi di Windows](windows-event-collector-functions.md) supportano la sottoscrizione di eventi tramite il protocollo WS-Management. Per ulteriori informazioni su WS-Management, vedere [informazioni su gestione remota Windows](/windows/desktop/WinRM/about-windows-remote-management).

## <a name="event-forwarding-and-event-collection-architecture"></a>Architettura dell'invio degli eventi e della raccolta di eventi

La raccolta di eventi consente agli amministratori di ottenere eventi da computer remoti e di archiviarli in un registro eventi locale sul computer dell'agente di raccolta. Il percorso del log di destinazione per gli eventi è una proprietà della sottoscrizione. Tutti i dati dell'evento trasmesso vengono salvati nel registro eventi del computer dell'agente di raccolta (nessuna informazione viene persa). All'evento vengono inoltre aggiunte informazioni aggiuntive correlate all'invio di eventi. Per ulteriori informazioni su come abilitare un computer per la ricezione di eventi raccolti o per l'invio di eventi, vedere [configurare i computer per l'invio e la raccolta di eventi](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748890(v=ws.11)).

## <a name="subscriptions"></a>Sottoscrizioni

Nell'elenco seguente vengono descritti i tipi di sottoscrizioni di eventi:

-   Sottoscrizioni avviate dall'origine: consente di definire una sottoscrizione di eventi in un computer dell'agente di raccolta eventi senza definire i computer dell'origine eventi. È quindi possibile configurare più computer di origine evento remoto (usando un'impostazione di criteri di gruppo) per inviare gli eventi al computer dell'agente di raccolta eventi. Per altre informazioni, vedere [configurazione di una sottoscrizione avviata dall'origine](setting-up-a-source-initiated-subscription.md). Questo tipo di sottoscrizione è utile quando non si è certi o non si desidera specificare tutti i computer di origini eventi che eseguiranno l'invio di eventi.
-   Sottoscrizioni avviate dall'agente di raccolta: consente di creare una sottoscrizione di eventi se si conoscono tutti i computer di origine eventi che inoltreranno gli eventi. È possibile specificare tutte le origini eventi al momento della creazione della sottoscrizione. Per altre informazioni, vedere [creazione di una sottoscrizione avviata dall'agente di raccolta](creating-an-event-collector-subscription.md).

## <a name="windows-event-collector-functions"></a>Funzioni dell'agente di raccolta eventi di Windows

Per ulteriori informazioni ed esempi di codice in cui vengono utilizzate le funzioni dell'agente di raccolta eventi, vedere [using Windows Event Collector](using-windows-event-collector.md).

Per ulteriori informazioni sulle funzioni utilizzate per raccogliere e trasmettere gli eventi, vedere [funzioni dell'agente di raccolta eventi di Windows](windows-event-collector-functions.md).

 

 
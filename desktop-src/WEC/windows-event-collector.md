---
title: Raccolta eventi Windows
description: È possibile sottoscrivere la ricezione e l'archiviazione di eventi in un computer locale (agente di raccolta eventi) che vengono inoltrati da un computer remoto (origine evento).
ms.assetid: 7725e06d-4df1-4b3e-9f2f-2b8bdd805cb6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1efa767ecb80960fc3461380435ea1d44992656d7c67df990574f7155ee976fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997881"
---
# <a name="windows-event-collector"></a>Raccolta eventi Windows

È possibile sottoscrivere la ricezione e l'archiviazione di eventi in un computer locale (agente di raccolta eventi) che vengono inoltrati da un computer remoto (origine evento). Le [Windows dell'agente](windows-event-collector-functions.md) di raccolta eventi supportano la sottoscrizione di eventi tramite il WS-Management eventi. Per altre informazioni su WS-Management, vedere [About Windows Remote Management](/windows/desktop/WinRM/about-windows-remote-management).

## <a name="event-forwarding-and-event-collection-architecture"></a>Architettura dell'inoltro degli eventi e della raccolta di eventi

La raccolta di eventi consente agli amministratori di ottenere gli eventi dai computer remoti e di archiviarli in un registro eventi locale nel computer dell'agente di raccolta. Il percorso del log di destinazione per gli eventi è una proprietà della sottoscrizione. Tutti i dati nell'evento inoltrato vengono salvati nel registro eventi del computer dell'agente di raccolta (nessuna informazione viene persa). All'evento vengono aggiunte anche informazioni aggiuntive relative all'inoltro dell'evento. Per altre informazioni su come consentire a un computer di ricevere eventi raccolti o inoltrare eventi, vedere Configurare i computer per inoltrare [e raccogliere eventi.](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748890(v=ws.11))

## <a name="subscriptions"></a>Sottoscrizioni

Nell'elenco seguente vengono descritti i tipi di sottoscrizioni di eventi:

-   Sottoscrizioni avviate dall'origine: consente di definire una sottoscrizione di eventi in un computer dell'agente di raccolta eventi senza definire i computer di origine eventi. È quindi possibile configurare più computer di origine eventi remoti (usando un'impostazione di Criteri di gruppo) per inoltrare gli eventi al computer dell'agente di raccolta eventi. Per altre informazioni, vedere [Configurazione di una sottoscrizione avviata dall'origine.](setting-up-a-source-initiated-subscription.md) Questo tipo di sottoscrizione è utile quando non si conosce o non si desidera specificare tutte le origini eventi computer che inoltrano gli eventi.
-   Sottoscrizioni avviate dall'agente di raccolta: consente di creare una sottoscrizione di eventi se si conoscono tutti i computer di origine eventi che inoltrano gli eventi. È possibile specificare tutte le origini eventi al momento della creazione della sottoscrizione. Per altre informazioni, vedere [Creazione di una sottoscrizione avviata dall'agente di raccolta](creating-an-event-collector-subscription.md).

## <a name="windows-event-collector-functions"></a>Windows Funzioni dell'agente di raccolta eventi

Per altre informazioni ed esempi di codice che usano le funzioni dell'agente di raccolta eventi, vedere [Using Windows Event Collector](using-windows-event-collector.md).

Per altre informazioni sulle funzioni usate per raccogliere e inoltrare eventi, vedere l'Windows [dell'agente di raccolta eventi](windows-event-collector-functions.md).

 

 
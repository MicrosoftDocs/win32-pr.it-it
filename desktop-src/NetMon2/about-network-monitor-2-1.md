---
description: Network Monitor è un componente di Microsoft Systems Management Server (SMS) usato per rilevare e risolvere i problemi relativi alle LAN, alle WAN e ai collegamenti seriali che eseguono il server di accesso remoto Microsoft (RAS).
ms.assetid: bd273439-daa2-4263-8f12-28ec988beea0
title: Informazioni su Network Monitor 2,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f447f4763e0c73dc0dcac4cf719a0bad4b61f073
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049984"
---
# <a name="about-network-monitor-21"></a>Informazioni su Network Monitor 2,1

Network Monitor è un componente di Microsoft Systems Management Server (SMS) usato per rilevare e risolvere i problemi relativi alle LAN, alle WAN e ai collegamenti seriali che eseguono il server di accesso remoto Microsoft (RAS). Network Monitor fornisce l'analisi dei dati di rete post-acquisizione.

Nell'analisi post-acquisizione il traffico di rete viene salvato in un file di acquisizione proprietario, in modo che i dati acquisiti possano essere analizzati in un secondo momento. In questo caso, l'analisi può essere sotto forma di [*parser*](p.md) di protocollo che scelgono tipi specifici di frame di rete e visualizzano i dati del frame nell'interfaccia utente di Network Monitor; o l'analisi può essere sotto forma di [*esperti*](e.md) che esaminano i dati di rete e visualizzano un report (gli esperti possono anche modificare i dati di rete).

Network Monitor offre i seguenti tipi di funzionalità:

-   Acquisisce i dati di rete in modalità in tempo reale o ritardato.
-   Fornisce funzionalità di filtro durante l'acquisizione dei dati.
-   USA esperti e parser per l'analisi post-acquisizione dettagliata.

Per ulteriori informazioni sulle funzionalità di Network Monitor, vedere:

-   [Architettura di esperti e parser](expert-and-parser-architecture.md)
-   [Esperti](experts.md)
-   [Parser](parsers.md)
-   [Provider di pacchetti di rete](network-packet-providers.md)
-   [BLOB Network Monitor](network-monitor-blobs.md)
-   [Pagina di riferimento evento](event-reference-page.md)
-   [Filtri di acquisizione](capture-filters.md)

**Windows Vista:** Network Monitor 2,1 e versioni precedenti non sono supportati in questa piattaforma.

 

 



